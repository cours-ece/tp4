# Answers

Nom : TRBOVIC
Prénom : Alexandre
NB : 7

# 1.
A quoi sert l'A/B testing ? On test deux modèle de machine learning pour voir lequel présente le meilleur taux de conversion.

Comment appliquer de l'A/B testing grâce à Istio ?

# 2.
Comment simuler un problème de timeout avec Istio ?

Comment le résoudre ?

# 3.
Qu'est-ce que le canary release ? Lorsque l'on veut mettre en prod un nouveau service, on redirige une partie du flux des visiteurs vers le nouveau service (environ 5%) et si le service génère des erreurs 4XX ou 5XX alors on peut rediriger le flux vers l'ancien service

En quoi est-ce utile ? A tester 1 nouveau service et limiter au maximum les effets secondaires du nouveau service.

Comment l'implémenter dans Istio ?

# 4.

# 5.
Qu'est-ce qu'un Circuit Breaker ? Une sécurité qui se déclenche lorsqu'un appele à un micro service met trop de temps à répondre. Lorsque des erreurs sont détectées, le circuit breaker bloque l'accès au service et la page demandée par l'utilisateur pourra quand même être affichée sans le service en question.

Comment l'implémenter dans un contexte Kubernetes ?

# 6.
Pourquoi avoir besoin de mirrorer le traffic vers un autre composant ? Pour effectuer du loadbalancing ?

# 7.
Pourquoi bloquer le traffic vers un service ? pour eviter que les retard s'accumulent, si d'autres services en dépendent ils vont eux aussi être ralenti.

Comment l'implémenter simplement avec Istio ?

# 8.
Quel est la problématique de tracing distribué ?

Quel est la spécification du tracing distribué et son implémentation dans Istio ?

# 9.
Comment s'appelle l'outil de récupération des métrics ? Jeager 

# 10.

# 11.
Comment s'appelle l'outil de visualisation des métrics ? Jeager

# 12.
A quoi sert un servicegraph ?

Quel serait l'utilité dans le quotidien d'un ops ? Pour otpimiser les tâches qui sont peut-etre inutilement longues aujourd'hui : une requête SQL qui prend 800ms pourrait être réduite à 5ms ?
