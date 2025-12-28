Exercice 8:

For now I created 3 files : deployment, service and configmap and applied them

When I ran >kubectl apply -f logging-configmap.yaml, Kubernetes created my ConfigMap

However later I noticed that my pods are not updated automatically, I had to deleted so it can be created with new config

The configuration below loads all data from configmap and places each key inside the container
envFrom:

- configMapRef:
  name: data-configmap

if ConfigMap had multiple keys, all the keus will become environment variables automatically

We use ConfigMap in order to avoid rebuilding Docker Image from scratch
