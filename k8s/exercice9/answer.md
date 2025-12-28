Exercice 9 :
J’ai créé un nouveau dossier pour l’exercice 9 où j’ai créé mon fichier de déploiement avec l’image tristan12/welcome-to-docker:typexo4.

J’ai mis à jour l’image en utilisant :
kubectl set image deployments/welcome-deployment welcome=soufianeremmal/welcome-to-docker:v2

J’ai vérifié la mise à jour avec :
kubectl rollout status deployments/welcome-deployment

rollout undo est la commande qui permet d’annuler les changements et de remettre l’ancienne image.

Avantages de l’utilisation de set image :
cela peut être fait de manière fluide pendant que le déploiement reste disponible

on peut annuler les changements directement via les commandes

Inconvénients :
Kubernetes n’a pas de suivi de versions spécifique pour les mises à jour d’images faites avec set image
