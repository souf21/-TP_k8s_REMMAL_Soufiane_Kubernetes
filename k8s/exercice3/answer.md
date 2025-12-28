Exercice 3

I copied the same welcome-deployment.yaml on the new folder created for exercice 3

now I changed the image to tristan12/welcome-to-docker:v1

I applied the deployment and checked my pods, 1 pod was created

I removed this pod using this command : kubectl delete pod welcome-deployment-865dd4c959-sjdj8

When I ran the command kubectl get pods it still showed me the pod created but with different name, that's because Kubernetes creates pods automatically when they are removed or deleted as long as we are specifying how many pods to be created in welcome-deployment.yaml

After changing the image to tristan12/welcome-to-docker:latest and applying the deployment

our old pod from v1 was replaced by a new pod with the name : welcome-deployment-865dd4c959-s5k25

Kubernetes terminates the pods and recreates new ones when you change the image
