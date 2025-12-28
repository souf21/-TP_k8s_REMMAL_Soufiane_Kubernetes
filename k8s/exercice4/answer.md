Exercice 4
J’ai créé un nouveau dossier et j’y ai copié mon fichier de déploiement, puis j’ai ajouté un nouveau fichier welcome-service.yaml.

J’ai ajouté le contenu YAML depuis le dépôt GitHub.

Ce service nous permet d’accéder à nos pods depuis l’extérieur du cluster.

Nous avons appliqué la configuration du service avec :
kubectl apply -f welcome-service.yaml

Nous avons vérifié que le service avait bien été créé.

J’ai ensuite utilisé cette commande pour me connecter au service et ouvrir l’application :
kubectl port-forward svc/welcome-svc 8080:8080

J’ai choisi 8080 comme port local, et en ouvrant le lien localhost:8080, mon application fonctionnait.

Enfin, j’ai supprimé le service avec :
kubectl delete service welcome-svc
