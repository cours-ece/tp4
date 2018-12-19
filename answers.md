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

Comment le résoudre ?

# 3.
Qu'est-ce que le canary release ?
Le canary release permet de faire tester la version ultérieure à celle utilisée par la majorité des utiisateurs
En quoi est-ce utile ?
L'utilité est de tester une nouvelle version d'une application sans être certain de son fonctionnement en production. On réduit ainsi le risque de bugs et de rollback en production.  
Comment l'implémenter dans Istio ?


# 4.

# 5.
Qu'est-ce qu'un Circuit Breaker ?
Un Circuit Breaker est un interrupteur qui bloque l'accès à un service en particulier lorsqu'il met trop de temps à répondre à cause d'erreurs.
Comment l'implémenter dans un contexte Kubernetes ?

# 6.
Pourquoi avoir besoin de mirrorer le traffic vers un autre composant ?

# 7.
Pourquoi bloquer le traffic vers un service ?
Si un service met trop de temps à répondre, les services qui en dépendent vont être également ralentis, on évite ainsi d'accumuler les retards.
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
