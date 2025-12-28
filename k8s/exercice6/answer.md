Exercice 6 :
J’ai apporté quelques modifications à mon image welcome-to-docker et je l’ai remplacée dans le dossier exercice6.

J’ai exécuté cette commande pour construire mon image :
docker build -t soufianeremmal/welcome-to-docker:v2 .

J’ai poussé l’image avec :
docker push soufianeremmal/welcome-to-docker:v2

J’ai copié le fichier welcome-deployment.yaml depuis l’exercice 5 et j’ai changé l’image.

J’ai appliqué le déploiement avec :
kubectl apply -f welcome-deployment.yaml

J’ai créé un nouveau service :
kubectl apply -f welcome-service.yaml

Ensuite, j’ai ouvert mon projet avec :
kubectl port-forward svc/welcome-svc 3003:8080

Voici les avantages et inconvénients de Kubernetes :
Avantages
Scalable : Kubernetes peut automatiquement scaler l’application et créer de nouveaux pods si nécessaire.

Haute disponibilité : si un pod plante, Kubernetes le recrée pour garder l’application disponible.

Mises à jour : on peut déployer de nouvelles versions sans interruption de service.

Inconvénients
Complexité : il faut certaines compétences pour travailler avec Kubernetes.

Redémarrage : il faut relancer Minikube à chaque fois que la machine est éteinte.

Pas idéal pour les petites applications : pour des projets simples avec très peu de conteneurs, Kubernetes peut être trop lourd.

Kubernetes est la meilleure solution de déploiement pour les projets larges et évolutifs, mais pour les petits projets, Docker suffit largement.
