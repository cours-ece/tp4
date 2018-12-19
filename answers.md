# Answers

Nom : Ly
Prénom : Hervé
NB : 2

# 1.
A quoi sert l'A/B testing ?
L'A/B testing permet de tester un changement de version, en testant plusieurs versions différentes en séparant les utilisateurs en 2 populations.

Comment appliquer de l'A/B testing grâce à Istio ?
On applique l'A/B testing avec Istio en indiquant une règle de route dans le fichier .yaml
Ex : pour 50% version v1 et 50% version v2
route:
  - labels:
      version: v1
    weight: 50
  - labels:
      version: v2
    weight: 50

# 2.
Comment simuler un problème de timeout avec Istio ?
On utilise un outil permettant du falt injection.

Comment le résoudre ?
On change le timeout dans la configuration des applications concernées, ou on travaille sur le code afin de permettre à l'application de tourner plus rapidement.

# 3.
Qu'est-ce que le canary release ?
Le canary release permet de faire tester la version ultérieure à celle utilisée par la majorité des utiisateurs

En quoi est-ce utile ?
L'utilité est de tester une nouvelle version d'une application sans être certain de son fonctionnement en production. On réduit ainsi le risque de bugs et de rollback en production.

Comment l'implémenter dans Istio ?
route:
  - destination:
      host: website  
      subset: version-2
      weight: 5
  - destination:
      host: website
      subset: version-1
      weight: 95

# 4.

# 5.
Qu'est-ce qu'un Circuit Breaker ?
Un Circuit Breaker est un interrupteur qui bloque l'accès à un service en particulier lorsqu'il met trop de temps à répondre à cause d'erreurs.

Comment l'implémenter dans un contexte Kubernetes ?
Il s'agit d'un ensemble de règles dans la configuration de Kubernetes.

# 6.
Pourquoi avoir besoin de mirrorer le traffic vers un autre composant ?
Ca permet de modifier la production en limitant les risques. On effectue une copie du trafic qui est située sur un "request path" moins critique pour le serveur.

# 7.
Pourquoi bloquer le trafic vers un service ?
Si un service met trop de temps à répondre, les services qui en dépendent vont être également ralentis, on évite ainsi d'accumuler les retards.

Comment l'implémenter simplement avec Istio ?
On utilise le rate limit qui permet de limiter dynamiquement le trafic vers un service.
istioctl create -f ratelimit-handler.yaml
le handler va permettre de configurer le nombre maximum de requêtes par seconde
istioctl create -f ratelimit-rule.yaml
Le rule permet de fixer le quota memoire (memquota) qui va activer le rate limit.

# 8.
Quel est la problématique de tracing distribué ?
Il s'agit de comprendre le comportement d'une application et savoir comment résoudre des problèmes.

Quel est la spécification du tracing distribué et son implémentation dans Istio ?
Istio trace les appels de chaque application du cluster et les affiche sur un dashboard.

# 9.
Comment s'appelle l'outil de récupération des métrics ?
Prometheus

# 10.

# 11.
Comment s'appelle l'outil de visualisation des métrics ?
Grafana

# 12.
A quoi sert un servicegraph ?
Un servicegraph est une représentation schématique de l'ensemble des services ainsi que les appels qui se font entre eux.
Quel serait l'utilité dans le quotidien d'un ops ?
Le servicegraph permet de visualiser très simplement l'ensemble des services d'une application.
