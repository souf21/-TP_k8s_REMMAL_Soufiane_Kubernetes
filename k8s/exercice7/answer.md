Erreurs dans le fichier de déploiement :

replicas était mal placé

container → containers

deployment → Deployment

labels:

appli: welcome → app: welcome

image: tristan12/welcome-to-docker:tpexo12 → image: tristan12/welcome-to-docker:v1

Erreurs dans le fichier de service :

Nodeport → NodePort

targetPort: 8080 → targetPort: 3000

nodePort: 31000 manquait

selector:

apply: welcome → app: welcome
