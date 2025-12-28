Exercice 1 :
J’ai créé un fichier dans mon dossier exercice 1 nommé : welcome-deployment.yaml.

J’ai copié le contenu et j’ai appliqué mes modifications sur l’image : soufianeremmal/welcome-to-docker:v1.

J’ai appliqué cette configuration avec kubectl apply -f welcome-deployment.yaml dans le même dossier, puisque mon terminal se trouvait déjà dans le même répertoire.

J’ai utilisé kubectl get pods pour voir les résultats.

Ensuite, j’ai supprimé le déploiement welcome-deployment avec :
kubectl delete deployment welcome-deployment.

En résumé, nous avons :

construit notre image Docker

créé notre fichier YAML de déploiement Kubernetes

appliqué le déploiement

vérifié que les pods ont bien été créés

supprimé le déploiement pour réinitialiser l’environnement
