Exercice 3
J’ai copié le même fichier welcome-deployment.yaml dans le nouveau dossier créé pour l’exercice 3.

Ensuite, j’ai changé l’image vers tristan12/welcome-to-docker:v1.

J’ai appliqué le déploiement et vérifié mes pods : 1 pod a été créé.

J’ai supprimé ce pod avec la commande :
kubectl delete pod welcome-deployment-865dd4c959-sjdj8

Lorsque j’ai relancé la commande kubectl get pods, un pod apparaissait toujours, mais avec un nom différent.
C’est normal : Kubernetes recrée automatiquement les pods lorsqu’ils sont supprimés, tant que le fichier welcome-deployment.yaml spécifie combien de pods doivent être présents.

Après avoir changé l’image vers tristan12/welcome-to-docker:latest et réappliqué le déploiement,

l’ancien pod utilisant la version v1 a été remplacé par un nouveau pod nommé :
welcome-deployment-865dd4c959-s5k25

Kubernetes termine les anciens pods et en recrée de nouveaux lorsque l’image est modifiée.
