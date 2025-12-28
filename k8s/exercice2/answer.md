Exercice 2

I created a new folder for exercice 2 and duplicated the welcome-deployment.yaml file in order to make these changes

I changed the file to create 3 pods by adding 3 replicas instead of 1

I used kubectl get pods to show me 3 pods created

I changed the deployment image to tristan12/123:latest and when I used the command kubectl get pods it showed me a new error : ErrImagePull

I used this command to show more details about this error :
kubectl describe pod welcome-deployment-7477d9997d-rzxw7

It seems that this command shows all details about our pod including IP address 10.244.0.10

Deployment is deleted now
