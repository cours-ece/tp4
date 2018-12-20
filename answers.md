# Answers

Nom : Benguigui
Prénom : Thomas
NB : 3

# 1.
A quoi sert l'A/B testing ?
L'A/B testing  sert à tester une MAJ sur une partie des utilisateurs. C'est généralement utilisé dans le cadre de tests d'UI. Une partie des utilisateurs aura la nouvelle version, et le reste l'ancienne.


Comment appliquer de l'A/B testing grâce à Istio ?
Avec Istio on peut créer des "routes" différentes pour plusieurs versions. Chaque route a un poids différent, et le total doit être 100.

# 2.
Comment simuler un problème de timeout avec Istio ?
Il faut utiliser un outil de fault injection.


Comment le résoudre ?
On peut :
- changer le timeout dans les applications
- optimiser les processus pour ne pas atteindre cette limite


# 3.
Qu'est-ce que le canary release ? En quoi est-ce utile ?
Le canary release est une stratégie de release qui permet de tester une grosse MAJ sur une partie de la population d'utilisateurs. Ca permet de corriger les bugs avant de release la MAJ pour tous les utilisateurs.


Comment l'implémenter dans Istio ?
On l'implémente de la même manière que pour l'AB testing dans Istio.

# 4.

# 5.
Qu'est-ce qu'un Circuit Breaker ?
C'est un outil de redirection de flux de services.


Comment l'implémenter dans un contexte Kubernetes ?
On peut le configurer comme des règles dans Kubernetes.

# 6.
Pourquoi avoir besoin de mirrorer le traffic vers un autre composant ?
Pour modifier un serveur de production en ne prenant pas de risques pour les utilisateurs actuels.

# 7.
Pourquoi bloquer le traffic vers un service ?
Pour ne pas trop ralentir les autres services qui utilisent ce service.

Comment l'implémenter simplement avec Istio ?
On utilise le rate limit qui limite dynamiquement le trafic vers un service.
- istioctl create -f ratelimit-handler.yaml le handler pour le nombre maximum de requêtes par seconde
- istioctl create -f ratelimit-rule.yaml fixer le quota memoire qui va activer le rate limit.

# 8.
Quel est la problématique de tracing distribué ?
Le but est de comprendre le comportement d'une application pour l'optimiser et résoudre les problèmes potentiels

Quel est la spécification du tracing distribué et son implémentation dans Istio ?
Istio a un dashboard qui permet de surveiller tous les appels de toutes les applications.

# 9.
Comment s'appelle l'outil de récupération des métrics ?
Prometheus

# 10.

# 11.
Comment s'appelle l'outil de visualisation des métrics ?
Grafana

# 12.
A quoi sert un servicegraph ?
C'est une représentation de tous les services et des leurs appels.


Quel serait l'utilité dans le quotidien d'un ops ?
On peut surveiller facilement tous les services d'une application
