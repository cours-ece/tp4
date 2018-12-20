# Answers

Nom : Asmar	
Prénom : Estelle
NB : 6
# 1.
A quoi sert l'A/B testing ?
On va tester deux modèles de Machine Learning pour voir lequel présente le meilleur taux de conversion.


Comment appliquer de l'A/B testing grâce à Istio ?
Istio permet de faire du traffic routing. 
On va donc pouvoir renseigner deux routes auxquelles on donne 2 poids (dont la somme vaut 100).

# 2.
Comment simuler un problème de timeout avec Istio ?
Simulation d'un long delai avec l'outil  injection.

Comment le résoudre ?
En augmentant le délai maximal accepté.

# 3.
Qu'est-ce que le canary release ?
Le canary Release est un pattern qui permet de mettre une petite tranche de population sur la version N + 1 ; la tranche restante restera temporairement sur la version N. 

En quoi est-ce utile ?
Cela permet de tester si tout va bien avant de déployer sur l’ensemble des utilisateurs.

Comment l'implémenter dans Istio ?
Comme pour l'A/B testing. La v1 va avoir un poids de 90 et la v2 de 10 par exemple.

# 4.

# 5.
Qu'est-ce qu'un Circuit Breaker ?
Un circuit breaker permet de protéger les applications contre les erreurs, les temps de latence et d'autres effets indésirables, en redirigeant les utilisateurs vers une autre application.

Comment l'implémenter dans un contexte Kubernetes ?
Opération config de Kubernetes.

# 6.
Pourquoi avoir besoin de mirrorer le traffic vers un autre composant ?
Afin de limiter les conséquences d'une nouvelle version déffectueuse.

# 7.
Pourquoi bloquer le traffic vers un service ?
Afin d'éviter le ralentissement des autres services.

Comment l'implémenter simplement avec Istio ?
En utilisant les "rates limits".

# 8.
Quel est la problématique de tracing distribué ?
Comprendre le comportement d'une application et résoudre ses problèmes.

Quel est la spécification du tracing distribué et son implémentation dans Istio ?
Un dashboard récapitule tous les appels aux applications du cluster.

# 9.
Comment s'appelle l'outil de récupération des métrics ?
L'outil de récupération des métrics est Prometheus. 

# 10.

# 11.
Comment s'appelle l'outil de visualisation des métrics ?
L'outil de visualisation des métrics est Grafana.

# 12.
A quoi sert un servicegraph ?
Surveiller le traffic de données entre les services.

Quelle serait l'utilité dans le quotidien d'un ops ?
Garantir la stabilité de notre système.


