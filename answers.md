# Answers

Nom : PIOVESAN 
Prénom : Clément
NB : 2

# 1.
A quoi sert l'A/B testing ?

Comment appliquer de l'A/B testing grâce à Istio ?

# 2.
Comment simuler un problème de timeout avec Istio ?
Nous utilisons un outil qui permet de faire du fault injection. 
Comment le résoudre ?
Il faut changer les timleout dans la configuration d'une ou plusieurs des applications. Ou alors faire en sorte que l'applicaiton en question tourne plus rapidement (optimisation de code etc.)

# 3.
Qu'est-ce que le canary release ?

En quoi est-ce utile ?

Comment l'implémenter dans Istio ?

# 4.

# 5.
Qu'est-ce qu'un Circuit Breaker ?
Un Circuit Breaker est un outil qui permet de rediriger des flux de données si un service tombe ou est trop lent. Cela permet de limiter l'impact d'application tournant pas ou mal. 
Comment l'implémenter dans un contexte Kubernetes ?
Cela s'apparente à un ensemble de règles implémentées dans la configuration de Kubernetes. 

# 6.
Pourquoi avoir besoin de mirrorer le traffic vers un autre composant ?

# 7.
Pourquoi bloquer le traffic vers un service ?

Comment l'implémenter simplement avec Istio ?

# 8.
Quel est la problématique de tracing distribué ?
La problématique est autour de la compréhension du comportement d'une application et comment résoudre des problèmes. 
Quel est la spécification du tracing distribué et son implémentation dans Istio ?
Istio trace tous les appels à toutes les applications du cluster et les montre sur un dashboard. 

# 9.
Comment s'appelle l'outil de récupération des métrics ?

# 10.

# 11.
Comment s'appelle l'outil de visualisation des métrics ?

# 12.
A quoi sert un servicegraph ?

Quel serait l'utilité dans le quotidien d'un ops ?
