# Answers

Nom : Kourganoff
Prénom : Adrien 
NB : 7

# 1.
A quoi sert l'A/B testing ? A voir l'impact d'une upgrade de version sur une population d'utilisateurs.

Comment appliquer de l'A/B testing grâce à Istio ? On crée deux routes avec 2 versions qui ont un poids entre 0 et 100. La somme des 2 routes doit avoir un poids de 100.

# 2.
Comment simuler un problème de timeout avec Istio ? Avec un outil de fault injection.

Comment le résoudre ? En changeant les timeouts dans les configs des applications ou en optimisant leur vitesse. 

# 3.
Qu'est-ce que le canary release ? Technique consistant, lors d'une update, à faire migrer uniquement une partie des utilisateurs vers la nouvelle version. 

En quoi est-ce utile ? Cela permet de tester l'update, d'éviter la surcharge et donc de réduire les risques.

Comment l'implémenter dans Istio ? Comme pour l'A/B testing. La v1 va avoir un poids de 90 et la v2 de 10 par exemple.

# 4.

# 5.
Qu'est-ce qu'un Circuit Breaker ? Un outil redirigeant les fluxs de données en cas de disfonctionnement (rallentissement important ou arrêt) d'un service.

Comment l'implémenter dans un contexte Kubernetes ? Opération dans la config de Kubernetes.

# 6.
Pourquoi avoir besoin de mirrorer le traffic vers un autre composant ? Pour limiter les risques en production lors d'une modification.

# 7.
Pourquoi bloquer le traffic vers un service ? Pour éviter d'accumuler des retards si un des services est trop lent.

Comment l'implémenter simplement avec Istio ? En n'exposant pas le port de ce service.

# 8.
Quel est la problématique de tracing distribué ? Comprendre le comportement d'une appli et résoudre des problèmes.

Quel est la spécification du tracing distribué et son implémentation dans Istio ? Un dashboard récapitule tous les appels aux applcations du cluster.

# 9.
Comment s'appelle l'outil de récupération des métrics ? Prometheus

# 10.

# 11.
Comment s'appelle l'outil de visualisation des métrics ? Grafana

# 12.
A quoi sert un servicegraph ? La visualisation dans un graphe du traffic des données.

Quel serait l'utilité dans le quotidien d'un ops ? A voir simplement et clairement le détail de son réseau et du traffic des données. Facilite la tache s'il doit l'expliquer à d'autres personnes.
