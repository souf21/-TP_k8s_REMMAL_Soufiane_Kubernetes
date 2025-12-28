Exercice 7:

Errors for deployment file:
replicas was missplaced

    container -> containers

    deployment -> Deployment

    labels:
        appli: welcome  -> app: welcome

    image: tristan12/welcome-to-docker:tpexo12 -> image: tristan12/welcome-to-docker:v1

Errors for service file:
Nodeport -> NodePort
targetPort: 8080 -> targetPort: 3000
nodePort: 31000 was missing

    selector:
    	  apply: welcome -> app: welcome
