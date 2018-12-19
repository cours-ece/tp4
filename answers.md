# Answers

Nom : Texier 
Prénom : Hadrien
NB : 2

# 1.
A quoi sert l'A/B testing ?
Il permet de pouvoir tester l'impacte d'une montée de version sur une population d'utilisateur
donnée. Un utilisateur aura par exemple la nouvelle version et un autre l'ancienne.

Comment appliquer de l'A/B testing grâce à Istio ?
Avec Istio on peut créer deux routes différentes pour deux versions. On donne alors à chaque route un poind allant de 0 à 100. Le total des deux poids doit correspondre à 100.
(Ce sont des pourcents)
route:
  - labels:
      version: v1
    weight: 50
  - labels:
      version: v3
    weight: 50

# 2.
Comment simuler un problème de timeout avec Istio ?

Comment le résoudre ?

# 3.
Qu'est-ce que le canary release ?
C'est une technique permettant de réduire le risque lors d'une montée en version. On reroute 
uniquement quelques utilisateurs sur la nouvelle version pour la tester et éviter de la surcharger.

En quoi est-ce utile ?
Cela permet de tester une nouvelle version petit à petit et de faire passer la version uniquement
lorsqu'on est satisfait et qu'on est sur qu'elle peut etre soutenue.

Comment l'implémenter dans Istio ?
On utilise le meme sytème que l'A/B Testing
- route:
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

Comment l'implémenter dans un contexte Kubernetes ?

# 6.
Pourquoi avoir besoin de mirrorer le traffic vers un autre composant ?
Cela permet des modifications sur la production en prenant le moins de risques possible.
On aura alors une copie du trafic mais qui est situé sur un "request path" non critique pour
le serveur.

# 7.
Pourquoi bloquer le traffic vers un service ?

Comment l'implémenter simplement avec Istio ?

# 8.
Quel est la problématique de tracing distribué ?

Quel est la spécification du tracing distribué et son implémentation dans Istio ?

# 9.
Comment s'appelle l'outil de récupération des métrics ?
Promotheus

# 10.

# 11.
Comment s'appelle l'outil de visualisation des métrics ?
Graphana

# 12.
A quoi sert un servicegraph ?

Quel serait l'utilité dans le quotidien d'un ops ?
