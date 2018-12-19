# Answers

Nom : Vuong
Prénom : Lisa
NB : 3

# 1.
A quoi sert l'A/B testing ? 
L'A/B testing sert à tester 2 versions diffèrentes par 2 parties des utilisateurs.

Comment appliquer de l'A/B testing grâce à Istio ?
On l'applique en ajoutant une "rule" dans le .yaml. On sépare les utilisateurs en 2 parties pour chaque version.

# 2.
Comment simuler un problème de timeout avec Istio ?
On peut set un délai "timeout" fixe.

Comment le résoudre ?

# 3.
Qu'est-ce que le canary release ?
Le canary release consiste à rediriger une petite partie des flux vers la nouvelle version.

En quoi est-ce utile ?
Cela permet de tester une nouvelle version tout en réduisant le risque de bugs et d'effets secondaires sur tout le reste de la prod.

Comment l'implémenter dans Istio ?
On l'implémente en ajoutant une "rule"

# 4.

# 5.
Qu'est-ce qu'un Circuit Breaker ?
Un Circuit Breaker est système de sécurité qui interrompt l'accès à un service lorsque celui ci met trop de trop à répondre.

Comment l'implémenter dans un contexte Kubernetes ?

# 6.
Pourquoi avoir besoin de mirrorer le traffic vers un autre composant ?
Pour protéger la production des éventuels bugs.

# 7.
Pourquoi bloquer le traffic vers un service ?
pour ne pas accumuler de retards et ne pas ralentir les autres services.

Comment l'implémenter simplement avec Istio ?

# 8.
Quel est la problématique de tracing distribué ?

Quel est la spécification du tracing distribué et son implémentation dans Istio ?

# 9.
Comment s'appelle l'outil de récupération des métrics ?

# 10.

# 11.
Comment s'appelle l'outil de visualisation des métrics ?

# 12.
A quoi sert un servicegraph ?

Quel serait l'utilité dans le quotidien d'un ops ?
