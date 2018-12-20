# Answers

Nom : Monomakhoff 
Prénom : Victor
NB : 1

# 1.
A quoi sert l'A/B testing ?
Observer l'impact d'une upgrade d'une interface sur les utilisateurs par rapport à une autre

Comment appliquer de l'A/B testing grâce à Istio ? Création de deux routes avec des valeurs dont la somme est égale à 100

# 2.
Comment simuler un problème de timeout avec Istio ? Avec un outil de fault injection

Comment le résoudre ? Changer les timeouts ou augmenter la vitesse

# 3.
Qu'est-ce que le canary release ? Faire migrer uniquement une petite partie des utilisateurs sur la nouvelle version

En quoi est-ce utile ? Tester l'upgrade tout en évitant les problèmes majeurs

Comment l'implémenter dans Istio ? mettre la V1 avec un poids nettement supérieur à la V2 (80/20 ou 90/10)

# 4.

# 5.
Qu'est-ce qu'un Circuit Breaker ? Outil redidrigeant les flux de données en cas de dysfonctionnement d'un systeme

Comment l'implémenter dans un contexte Kubernetes ? Opération dans la config de Kubernetes

# 6.
Pourquoi avoir besoin de mirrorer le traffic vers un autre composant ? Pour limiter les risques de mise en production

# 7.
Pourquoi bloquer le traffic vers un service ? Pour éviter l'accumulation des retards si un des services est trop lent

Comment l'implémenter simplement avec Istio ? En cachant le port du service

# 8.
Quel est la problématique de tracing distribué ? Comprendre le comportement d'une application et résoudre des pbs.

Quel est la spécification du tracing distribué et son implémentation dans Istio ? Un dashboard très complet rappelant tous les appels au application du cluster.

# 9.
Comment s'appelle l'outil de récupération des métrics ? Prometheus

# 10.

# 11.
Comment s'appelle l'outil de visualisation des métrics ? Grafana

# 12.
A quoi sert un servicegraph ? Visualisation d'un graphe de traffic des données

Quel serait l'utilité dans le quotidien d'un ops ? Observer en un coup d'oeil le traffic des données.
