# Answers

Nom : Ong
Prénom : Philippe
NB : 6

# 1.
A quoi sert l'A/B testing ?
L'A/B testing permet de tester une nouvelle version sur une partie de la population. Tout le trafic est ainsi partagé entre des utilisateurs ayant une ancienne version et une autre partie ayant la nouvelle.
Comment appliquer de l'A/B testing grâce à Istio ?
On applique une "rule" qui va router les utilisateurs sur une v1 ou v2.

# 2.
Comment simuler un problème de timeout avec Istio ?
On peut créer une "fault injection" pour simuler un long délai
Comment le résoudre ?
On peut augmenter le délai maximal toléré.

# 3.
Qu'est-ce que le canary release ?
Le canary release est le fait de migrer le trafic vers une nouvelle version, mais petit à petit

En quoi est-ce utile ?
Cela permet de tester que notre nouvelle version est bien fonctionnelle et ne pas impacter tous les utilisateurs

Comment l'implémenter dans Istio ?
On établit des "rules" pour router les utilisateurs petit à petit.

# 4.

# 5.
Qu'est-ce qu'un Circuit Breaker ?
Un circuit breaker permet protéger nos applications contre les erreurs, les temps de latence et d'autres effets indésirables, en redirigeant les utilisateurs vers une autre application.

Comment l'implémenter dans un contexte Kubernetes ?
On créee une destination rule.

# 6.
Pourquoi avoir besoin de mirrorer le traffic vers un autre composant ?
Le mirroring permet de protéger la production en créant une copie du service et en redirigeant le trafic vers cette copie. Cela permet de prendre le moins de risque possible pour le déploiement en prod. 

# 7.
Pourquoi bloquer le traffic vers un service ?
Dans le cas où notre service avait un problème, bloquer le trafic permet de ne pas ralentir tous nos autres services.

Comment l'implémenter simplement avec Istio ?
En établissant des "rate limits".

# 8.
Quel est la problématique de tracing distribué ?
Le tracing distribué met en place un système de tracing de nos applications pour suivre son comportement.

Quel est la spécification du tracing distribué et son implémentation dans Istio ?
Un dashboard Jaeger permet de visualiser et gestionner nos tracing.

# 9.
Comment s'appelle l'outil de récupération des métrics ?
Prometheus

# 10.

# 11.
Comment s'appelle l'outil de visualisation des métrics ?
Graphana

# 12.
A quoi sert un servicegraph ?
Un servicegraph permet de visualiser l'ensemble de nos services et leur communication

Quel serait l'utilité dans le quotidien d'un ops ?
Garantir la stabilité de notre système.
