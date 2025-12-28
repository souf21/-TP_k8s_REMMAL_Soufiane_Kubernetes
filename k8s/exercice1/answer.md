Exercice 1 :

I created a file inside of my execercice 1 folder named : welcome-deployment.yaml

I copied the content and I applied my changes image: soufianeremmal/welcome-to-docker:v1

I applied this configuration kubectl apply -f welcome-deployment.yaml on the same folder because my terminal is in the same "répertoire" as well

I used kubectl get pods to see the results

Now welcome-deployment is deleted : kubectl delete deployment welcome-deployment

we basically : - built our docker image - created our Kubernetes deployment yaml - applied the deployment - verified that our pods are created - deleted the deployment to reset the environment
