# Answers

Nom : Auger
Prénom : Simon
NB : 5

# 1.
A quoi sert l'A/B testing ?
L'A/B testing permet de tester des hypothèses d'optimsation de pages avec 
des variantes de pages.

Comment appliquer de l'A/B testing grâce à Istio ?
Istio permet de faire du traffic routing. On va donc pouvoir renseigner deux 
routes aux quelles on donne 2 poids (dont la somme vaut 100).

# 2.
Comment simuler un problème de timeout avec Istio ?
Outil de fault injection

Comment le résoudre ?
On change le délai accepté
# 3.
Qu'est-ce que le canary release ?
Ce pattern permet de confronter la version N+1 à une population restreinte 
d’utilisateurs, tandis que la majorité des utilisateurs 
ont accès à la version N.

En quoi est-ce utile ?
Permet de tester une nouvelle version à ses emlployés d'abord par exemple avant 
la release pour le grand public. C'est la solution mise en place par Facebook 
pour tester ses nouvelles features.
Comment l'implémenter dans Istio ?
On met un poids faible pour la nouvelle version.
# 4.

# 5.
Qu'est-ce qu'un Circuit Breaker ?
C'est  pattern permettant de désactiver l’envoi de requêtes au service appelé 
et de renvoyer plus rapidement un fallback.

Comment l'implémenter dans un contexte Kubernetes ?
Config de kubernetes
# 6.
Pourquoi avoir besoin de mirrorer le traffic vers un autre composant ?
Pour limiter les conséquences d'une nouvelle version déffectueuse
# 7.
Pourquoi bloquer le traffic vers un service ?
Eviter de ralentir les autres services.
Comment l'implémenter simplement avec Istio ?
On met en place des rate limits
# 8.
Quel est la problématique de tracing distribué ?
Tracer le flux d'une requête à travers les limites de service, 
ce qui est important dans un environnement à services multiples 
dans lequel une requête transite généralement par plusieurs services

Quel est la spécification du tracing distribué et son implémentation dans Istio ?
On a un dashboard pour suivre ce flux.
# 9.
Comment s'appelle l'outil de récupération des métrics ?
Prometheus
# 10.

# 11.
Comment s'appelle l'outil de visualisation des métrics ?
Grafana
# 12.
A quoi sert un servicegraph ?
Surveiller le traffic de données entre les services.
Quel serait l'utilité dans le quotidien d'un ops ?
Suivre son système et pouvoir agir rapidement dans le cas de problèmes.
