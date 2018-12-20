# Answers

Nom : Tagliero
Prénom : Hugo
NB : 4

# 1.
A quoi sert l'A/B testing ?
à tester un changement de version

Comment appliquer de l'A/B testing grâce à Istio ?
En indiquant une règle de route dans le fichier .yaml.

# 2.
Comment simuler un problème de timeout avec Istio ?
Avec un outil de falt injection.

Comment le résoudre ?
On doit modifier le timeout dans la configuration des applications concernées.

# 3.
Qu'est-ce que le canary release ?
C'est faire tester la version suivante (non actuelle) aux utilisateurs

En quoi est-ce utile ?
Cela sert à tester l'application pour éviter les bugs potentiels lors de la sortie de la version

Comment l'implémenter dans Istio ?
////

# 4.

# 5.
Qu'est-ce qu'un Circuit Breaker ?
Un moyen de rendre un service inaccessible s'il met trop de temps à répondre (en cas de bug ou d'erreurs)

Comment l'implémenter dans un contexte Kubernetes ?
il faut configurer des règles dans kurbernetes

# 6.
Pourquoi avoir besoin de mirrorer le traffic vers un autre composant ?
Afin de modifier la production tout en limitant les risques. On fait une copie du trafic située sur un "request path" moins critique pour le serveur.

# 7.
Pourquoi bloquer le traffic vers un service ?
 Afin d'éviter d'accumuler les retards. En effet, si un service met trop de temps à répondre, les autres services dépendant de celui-ci seront ralentis.

Comment l'implémenter simplement avec Istio ?
En employant le "rate limit" qui permet de limiter dynamiquement le trafic vers un service.

# 8.
Quel est la problématique de tracing distribué ?
C'est la compréhension du comportement d'une application et savoir par quel moyen résoudre les problèmes.

Quel est la spécification du tracing distribué et son implémentation dans Istio ?
Istio trace les appels de chacune des applications du cluster et les affiche sur un dashboard.

# 9.
Comment s'appelle l'outil de récupération des métrics ?
Prometheus

# 10.

# 11.
Comment s'appelle l'outil de visualisation des métrics ?
Grafana

# 12.
A quoi sert un servicegraph ?
Un servicegraph est une représentation schématique de l'ensemble des services et des appels qui se font entre ceux-ci.

Quel serait l'utilité dans le quotidien d'un ops ?
Il permet de visualiser d'une manière très simple l'ensemble des services d'une application.
