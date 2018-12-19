# Answers

Nom : PIOVESAN 
Prénom : Clément
NB : 2

# 1.
A quoi sert l'A/B testing ?
A quoi sert l'A/B testing ? Il permet de pouvoir tester l'impacte d'une montée de version sur une population d'utilisateur donnée. Un utilisateur aura par exemple la nouvelle version et un autre l'ancienne.
Comment appliquer de l'A/B testing grâce à Istio ?
Avec Istio on peut créer deux routes différentes pour deux versions. On donne alors à chaque route un poind allant de 0 à 100. Le total des deux poids doit correspondre à 100. (Ce sont des pourcents) route:

labels: version: v1 weight: 50
labels: version: v3 weight: 50

# 2.
Comment simuler un problème de timeout avec Istio ?
Nous utilisons un outil qui permet de faire du fault injection. 
Comment le résoudre ?
Il faut changer les timeout dans la configuration d'une ou plusieurs des applications. Ou alors faire en sorte que l'applicaiton en question tourne plus rapidement (optimisation de code etc.)

# 3.
Qu'est-ce que le canary release ?
C'est une technique permettant de réduire le risque lors d'une montée en version. On reroute uniquement quelques utilisateurs sur la nouvelle version pour la tester et éviter de la surcharger.
En quoi est-ce utile ?
Cela permet de tester une nouvelle version petit à petit et de faire passer la version uniquement lorsqu'on est satisfait et qu'on est sur qu'elle peut etre soutenue.
Comment l'implémenter dans Istio ?
On utilise le meme sytème que l'A/B Testing

route:
destination: host: website subset: version-2 weight: 5
destination: host: website subset: version-1 weight: 95

# 4.

# 5.
Qu'est-ce qu'un Circuit Breaker ?
Un Circuit Breaker est un outil qui permet de rediriger des flux de données si un service tombe ou est trop lent. Cela permet de limiter l'impact d'application tournant pas ou mal. 
Comment l'implémenter dans un contexte Kubernetes ?
Cela s'apparente à un ensemble de règles implémentées dans la configuration de Kubernetes. 

# 6.
Pourquoi avoir besoin de mirrorer le traffic vers un autre composant ?
Cela permet des modifications sur la production en prenant le moins de risques possible. On aura alors une copie du trafic mais qui est situé sur un "request path" non critique pour le serveur.

# 7.
Pourquoi bloquer le traffic vers un service ?
 Si un service met trop de temps à répondre, les services qui en dépendent vont être également ralentis, on évite ainsi d'accumuler les retards.
Comment l'implémenter simplement avec Istio ?
On utilise le rate limit qui permet de limiter dynamiquement le trafic vers un service. istioctl create -f ratelimit-handler.yaml le handler va permettre de configurer le nombre maximum de requêtes par seconde istioctl create -f ratelimit-rule.yaml Le rule permet de fixer le quota memoire (memquota) qui va activer le rate limit.

# 8.
Quel est la problématique de tracing distribué ?
La problématique est autour de la compréhension du comportement d'une application et comment résoudre des problèmes. 
Quel est la spécification du tracing distribué et son implémentation dans Istio ?
Istio trace tous les appels à toutes les applications du cluster et les montre sur un dashboard. 

# 9.
Comment s'appelle l'outil de récupération des métrics ?
Prometheus

# 10.

# 11.
Comment s'appelle l'outil de visualisation des métrics ?
Grafana

# 12.
A quoi sert un servicegraph ?
Un servicegraph est une représentation schématique de l'ensemble des services ainsi que les appels qui se font entre eux.
Quel serait l'utilité dans le quotidien d'un ops ?
Le servicegraph permet de visualiser très simplement l'ensemble des services d'une application.
