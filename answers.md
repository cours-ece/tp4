# Answers

Nom : GAIDIER
Prénom : Clément
NB : 4

# 1.
A quoi sert l'A/B testing ?
L'A/B testing permet de tester un upgrade de version sur une population d'utilisateurs donnée. 
Comment appliquer de l'A/B testing grâce à Istio ?
Istio permet de faire du traffic routing. On cré deux routes différentes pour deux versions. Chaque route à un poid allant de 0 à 100. La somme des 2 routes doit avoir un poids de 100.
# 2.
Comment simuler un problème de timeout avec Istio ?
On peut simuler le timeout avec l'outil de fault injection
Comment le résoudre ?
On peut le résoudre en changeant le timeout dans la configuration des applications ou alors en optimisant le code.
# 3.
Qu'est-ce que le canary release ?
Le canary release permet de confronter la nouvelle upgrade à une population restreinte alors que le reste de la population restera sur la version non upgrade
En quoi est-ce utile ?
C'est utile dans le sens qu'on peut tester une nouvelle version et de la déployer à l'ensemble de la population lorsqu'on est sûr que la version est stable et satisfait la population. Cela permet donc de réduire les risques.
Comment l'implémenter dans Istio ?
Comme pour l'A/B testing mais on utilise un poids faible pour la nouvelle version. Par exemple un poids de 5 pour la nouvelle version sur la route 1 et un poids de 95 sur la version non upgrade sur la route 2.
# 4.

# 5.
Qu'est-ce qu'un Circuit Breaker ?
C'est un outil qui redirige les flux de données en cas de disfonctionnement (down ou ralentissement) d'un service.
Comment l'implémenter dans un contexte Kubernetes ?
Un ensemble de règles dans la configuration de Kubernetes.
# 6.
Pourquoi avoir besoin de mirrorer le traffic vers un autre composant ?
Afin de limiter les risques d'une version déffectueuse
# 7.
Pourquoi bloquer le traffic vers un service ?
Afin d'éviter de ralentir les autres services
Comment l'implémenter simplement avec Istio ?
En implémentant des rate limits
# 8.
Quel est la problématique de tracing distribué ?
Comprendre le comportement d'une application afin de résoudre plus rapidement les problèmes
Quel est la spécification du tracing distribué et son implémentation dans Istio ?
Tous les appels des applications du cluster sont afficher sur un dashboard
# 9.
Comment s'appelle l'outil de récupération des métrics ?
Prometheus
# 10.

# 11.
Comment s'appelle l'outil de visualisation des métrics ?
Grafana
# 12.
A quoi sert un servicegraph ?
Permet de contrôler le traffic des données dans un graph
Quel serait l'utilité dans le quotidien d'un ops ?
Visualiser l'ensemble des services et agir au plus vite en cas de problèmes
