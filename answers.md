# Answers

Nom : Leroux
Prénom : Célestin
NB : 5

# 1.
A quoi sert l'A/B testing ?  c'est une tactique d'adaptation et d'optimisation consistant à tester deux versions auprès des utilisateurs.

Comment appliquer de l'A/B testing grâce à Istio ? On pourrait créer deux routes avec 2 versions qui ont un poids entre 0 et 100 et la somme des 2 routes devrait avoir un poids de 100.

# 2.
Comment simuler un problème de timeout avec Istio ? Avec une technique de fault injection.

Comment le résoudre ?

# 3.
Qu'est-ce que le canary release ? il intervient lors de la mise en production d'un nouveau service : on redirige une partie des visiteurs vers le nouveau service et si le service génère des erreurs 4XX ou 5XX alors on peut rediriger le flux de visiteurs vers l'ancien service ! 

En quoi est-ce utile ? Cela permet de voir l'efficience du nouveau service et de minimiser les risques.

Comment l'implémenter dans Istio ? On peut le résoudre en changeant le timeout dans la configuration des applications ou en optimisant le code.

# 4.

# 5.
Qu'est-ce qu'un Circuit Breaker ? C'est un outil qui redirige les flux de données en cas de de down ou de ralentissement d'un service.

Comment l'implémenter dans un contexte Kubernetes ?  En configurant des règles dans la configuration de Kubernetes.

# 6.
Pourquoi avoir besoin de mirrorer le traffic vers un autre composant ?
 Pour ne pas obtenir une version défectueuse


# 7.
Pourquoi bloquer le traffic vers un service ? Pour ne pas accumuler les retards. Si un service met trop de temps à répondre, les autres services dépendant de celui-ci seront ralentis.

Comment l'implémenter simplement avec Istio ? avec "rate limit"
# 8.
Quel est la problématique de tracing distribué ? Problème de omportement d'une application et savoir par quel moyen résoudre les problèmes.

Quel est la spécification du tracing distribué et son implémentation dans Istio ? il trace les appels de chacune des applications du cluster et les affiche sur un dashboard.

# 9.
Comment s'appelle l'outil de récupération des métrics ? Prometheus

# 10.

# 11.
Comment s'appelle l'outil de visualisation des métrics ? Grafana

# 12.
A quoi sert un servicegraph ? représentation schématique de l'ensemble des services et des appels qui se font entre ceux-ci.

Quel serait l'utilité dans le quotidien d'un ops ? ce serait de visualiser d'une manière très simple l'ensemble des services d'une application.
