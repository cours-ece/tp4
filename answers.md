# Answers

Nom : Pasternak
Prénom : Claire
NB : 3

# 1.
A quoi sert l'A/B testing ? L'A/B testing consiste à tester plusieurs hypothèses en même temps

Comment appliquer de l'A/B testing grâce à Istio ? Il faut indiquer plusieurs routes dans le yaml qui correspondent chacune à une version. 
Exemple : 
  - labels:
      version: 1
      weight: 50
  - labels:
      version: 2
      weight: 50

# 2.
Comment simuler un problème de timeout avec Istio ? Mettre un delay avec une fault injection.

Comment le résoudre ? Le changer dans les configurations des applications.

# 3.
Qu'est-ce que le canary release ? Il s'agit de tester une nouvelle version d'une application sur une petite partie des utilisateurs d'abord

En quoi est-ce utile ? Cela permet de ne pas impacter l'ensemble des utilisateurs en cas de problème sur la nouvelle version et de tester les nouvelles fonctionnalités

Comment l'implémenter dans Istio ? Comme pour l'A/B testing, il faut indiquer plusieurs routes dans le yaml qui correspondent chacune à une version. 

# 4.

# 5.
Qu'est-ce qu'un Circuit Breaker ? Le Circuit Breaker permet d'interrompre ou de rediriger l'utilisateur vers une autre page si l'application a des erreurs.

Comment l'implémenter dans un contexte Kubernetes ? Il faut indiquer des "destination rules" dans Kubernetes.

# 6.
Pourquoi avoir besoin de mirrorer le traffic vers un autre composant ? Pour limiter les risques lorsqu'on modifie la production.

# 7.
Pourquoi bloquer le traffic vers un service ? Afin de ne pas impacter les services qui sont liés à ce service en cas de problème de temps de réponse.

Comment l'implémenter simplement avec Istio ? Il faut utiliser une rate limit.

# 8.
Quel est la problématique de tracing distribué ? Il faut comprendre les comportements de l'application et comment résoudre les problèmes.

Quel est la spécification du tracing distribué et son implémentation dans Istio ? Istio permet de tracer les appels aux applications.

# 9.
Comment s'appelle l'outil de récupération des métrics ? Promotheus

# 10.

# 11.
Comment s'appelle l'outil de visualisation des métrics ? Grafana

# 12.
A quoi sert un servicegraph ? Il permet de voir les services ainsi que les appels de ces services.

Quel serait l'utilité dans le quotidien d'un ops ? Pouvoir détecter un problème facilement.
