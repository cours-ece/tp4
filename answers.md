# Answers

Nom : Marchand
Prénom : Adrien
NB : 3

# 1.
A quoi sert l'A/B testing ? L'A/B testing permet, en séparant les utilisateurs en 2 versions différentes, de tester un changement de version.

Comment appliquer de l'A/B testing grâce à Istio ? En indiquant une règle de route dans le fichier .yaml.

# 2.
Comment simuler un problème de timeout avec Istio ? Avec un outil permettant du falt injection.

Comment le résoudre ? On travaille sur le code afin de rendre l'application plus rapide ou on modifie le timeout dans la configuration des applications concernées.

# 3.
Qu'est-ce que le canary release ?  Le canary release c'est le fait de faire tester la version suivante à celle utilisée actuellement par la majorité des utilisateurs.

En quoi est-ce utile ?  C'est de pouvoir tester une nouvelle version d'une application sans pour autant être persuadé de son fonctionnement en production, les risques de bugs et de rollback en production sont ainsi réduits.

Comment l'implémenter dans Istio ? route:

destination: host: website
subset: version-2 weight: 5
destination: host: website subset: version-1 weight: 95

# 4.

# 5.
Qu'est-ce qu'un Circuit Breaker ? C'est un interrupteur qui empêche d'accéder à un service en particulier dès que celui-ci met trop de temps à répondre à cause d'erreurs.

Comment l'implémenter dans un contexte Kubernetes ?  Ce sont des règles à préciser dans la configuration de Kubernetes.

# 6.
Pourquoi avoir besoin de mirrorer le traffic vers un autre composant ? Afin de modifier la production tout en limitant les risques. On fait une copie du trafic située sur un "request path" moins critique pour le serveur.

# 7.
Pourquoi bloquer le traffic vers un service ? Afin d'éviter d'accumuler les retards. En effet, si un service met trop de temps à répondre, les autres services dépendant de celui-ci seront ralentis.

Comment l'implémenter simplement avec Istio ? En employant le "rate limit" qui permet de limiter dynamiquement le trafic vers un service.

- istioctl create -f ratelimit-handler.yaml, le handler va nous permettre de configurer le nombre maximum de requêtes par seconde. 
- istioctl create -f ratelimit-rule.yaml, le rule va nous permettre de fixer le quota memoire (memquota) en activant le rate limit.

# 8.
Quel est la problématique de tracing distribué ? C'est la compréhension du comportement d'une application et savoir par quel moyen résoudre les problèmes.

Quel est la spécification du tracing distribué et son implémentation dans Istio ? Istio va tracer les appels de chacune des applications du cluster et les afficher sur un dashboard.

# 9.
Comment s'appelle l'outil de récupération des métrics ? Promotheus

# 10.

# 11.
Comment s'appelle l'outil de visualisation des métrics ? Grafana

# 12.
A quoi sert un servicegraph ? Un servicegraph est une représentation schématique de l'ensemble des services et des appels qui se font entre ceux-ci.

Quel serait l'utilité dans le quotidien d'un ops ? L'utilité du servicegraph serait de pouvoir visualiser d'une manière très simple l'ensemble des services d'une application.
