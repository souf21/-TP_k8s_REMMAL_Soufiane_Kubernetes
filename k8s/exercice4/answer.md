exercice 4

I have created a new folder and copied my deployment file inside and added a new file welcome-service.yaml

I added the yaml content from GitHub repo

this will help us access to our pods outside of our cluster

we applied configuration to our service using kubectl apply -f welcome-service.yaml

we checked that our service was created

I applied this code to connect to this service and open our application :
kubectl port-forward svc/welcome-svc 8080:8080

I chose 8080 as my local port, when I opened the link localhost:8080 my app worked

I deleted the service: kubectl delete service welcome-svc
