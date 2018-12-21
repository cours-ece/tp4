# Answers

Nom : TABEL
Prénom : Eugénie
NB : 6

# 1.
A quoi sert l'A/B testing ?

L’A/B testing est une procédure permettant de mesurer l’impact d’un changement de version d’une variable sur l’atteinte d’un objectif. Ainsi, un test A/B permet de tester 2 versions de la variable. Une partie A des utilisateurs utilise une ancienne version et une autre partie B utilise une nouvelle version.


Comment appliquer de l'A/B testing grâce à Istio ?
Istio permet de faire du traffic routing. 
On utilise un routeur constitué deux routes, chacune menant vers une version différente (A ou B).

# 2.
Comment simuler un problème de timeout avec Istio ?
On utilise un outil de simulation appelé "fault injection".

Comment le résoudre ?
En configurant les timeouts afin d'augmenter les délais ou bien en augmentant les performances (vitesse d'éwécution) de l'application en cours

# 3.
Qu'est-ce que le canary release ?
Le canary Release est un pattern qui permet de mettre une petite tranche de population sur la version N + 1. 
La tranche restante restera temporairement sur la version N. 

En quoi est-ce utile ?
Cette technique permet de vérifier que la nouvelle version fonctionne bien et de limiter l'impact sur la population des utilisateurs

Comment l'implémenter dans Istio ?
Comme pour l'A/B testing. La v1 va avoir un poids de 90 et la v2 de 10 par exemple.


# 4.

# 5.
Qu'est-ce qu'un Circuit Breaker ?
Un outil de sécurité qui permet de protéger les applications contre les erreurs, les temps de latence et d'autres effets indésirables, en redirigeant les utilisateurs vers une autre application.

Comment l'implémenter dans un contexte Kubernetes ?
En créant une destination dans la configuration de Kubernetes.

# 6.
Pourquoi avoir besoin de mirrorer le traffic vers un autre composant ?
Car cela permet de sécuriser l'application en prod en créant une copie du service vers laquelle sera redirigée le trafic. 
Ainsi le risque lors du déploiement en production d'une l'application est réduit.


# 7.
Pourquoi bloquer le traffic vers un service ?
Pour limiter l'impact d'un service défectueux sur d'autres services qui dépendent de lui (ralentissement)

Comment l'implémenter simplement avec Istio ?
Grâce aux rate limits.

# 8.
Quel est la problématique de tracing distribué ?
Etudier et comprendre le comportement d'une application et résoudre ses problèmes.

Quel est la spécification du tracing distribué et son implémentation dans Istio ?
Jeager permet de visualiser toutes les reqûetes sur un dashboard.

# 9.
Comment s'appelle l'outil de récupération des métrics ?
Prometheus

# 10.

# 11.
Comment s'appelle l'outil de visualisation des métrics ?
Grafana

# 12.
A quoi sert un servicegraph ?
C'est une visualisation de l'ensemble des services et de la communication entre eux.

Quel serait l'utilité dans le quotidien d'un ops ?
Garantir la stabilité de notre système.

