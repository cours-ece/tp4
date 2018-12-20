# Answers

Nom : Bouhi
Prénom : Jeremy
NB : 5

# 1.
A quoi sert l'A/B testing ?
L'AB testing sert à prendre des décisions plus facilement. La technique consiste à soumetttre deux solutions en changeant 1 seul paramètre, et donc on garde le paramèter qui a le plus de succès.

Comment appliquer de l'A/B testing grâce à Istio ?
Grâce à Istio, on peut déterminer quelle est la meilleure route à suivre en spécifiant la règle dans le .yaml

# 2.
Comment simuler un problème de timeout avec Istio ?
falt injection

Comment le résoudre ?
En changeant le timeout

# 3.
Qu'est-ce que le canary release ?
faire en sorte qu'une partie des utilisateurs aient accès la nouvelle version

En quoi est-ce utile ?
on peut tester sur une partie des utilisateurs et donc en cas de bugs, cette seule partie sera impactée

Comment l'implémenter dans Istio ?

# 4.

# 5.
Qu'est-ce qu'un Circuit Breaker ?
C'est ce qui permet de stopper un service dès que son tiemout est passé

Comment l'implémenter dans un contexte Kubernetes ?

# 6.
Pourquoi avoir besoin de mirrorer le traffic vers un autre composant ?
Pour toujours avoir un service accessible en cas de problème

# 7.
Pourquoi bloquer le traffic vers un service ?
Parce que ça ferait ralentir la solution globale

Comment l'implémenter simplement avec Istio ?

# 8.
Quel est la problématique de tracing distribué ?

Quel est la spécification du tracing distribué et son implémentation dans Istio ?

# 9.
Comment s'appelle l'outil de récupération des métrics ?
Prometheus

# 10.

# 11.
Comment s'appelle l'outil de visualisation des métrics ?
Grafana

# 12.
A quoi sert un servicegraph ?
A avoir visualisation globale des différents services actifs. 

Quel serait l'utilité dans le quotidien d'un ops ?
Pouvoir prévenir des éventuelles crash, Pouvoir rapidement remettre la prod en place en sachant rapidement d'où vient le problème
