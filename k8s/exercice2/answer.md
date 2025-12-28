Exercice 2
J’ai créé un nouveau dossier pour l’exercice 2 et j’ai dupliqué le fichier welcome-deployment.yaml afin d’y apporter les modifications nécessaires.

J’ai modifié le fichier pour créer 3 pods en ajoutant 3 replicas au lieu de 1.

J’ai utilisé kubectl get pods pour vérifier que 3 pods avaient bien été créés.

J’ai ensuite changé l’image du déploiement vers tristan12/123:latest, et lorsque j’ai utilisé la commande kubectl get pods, un nouvel avertissement est apparu : ErrImagePull.

J’ai utilisé cette commande pour obtenir plus de détails sur l’erreur :
kubectl describe pod welcome-deployment-7477d9997d-rzxw7

Il semble que cette commande affiche toutes les informations concernant notre pod, y compris son adresse IP 10.244.0.10.

Le déploiement a ensuite été supprimé.
