Exercice 6:

I have made some changes to my welcome-to-docker image and replaced it in exercice6 folder

I ran this command to build my image docker build -t soufianeremmal/welcome-to-docker:v2 .

I pushed the image using : docker push soufianeremmal/welcome-to-docker:v2

I copied welcome-deployment.yaml from exercice 5 and changed image

I applied deployment : kubectl apply -f welcome-deployment.yaml

I created a new service : kubectl apply -f welcome-service.yaml

And then I opened my project : kubectl port-forward svc/welcome-svc 3003:8080

These are advantages and disadvantages of Kubernetes

Advantages

Scalable: Kuberentes can automatically scale application and create new pods if needed
High availability : if a pod craches it recreates it to keep app available
updates: you can deploy new versions without downtime

Disadvantages
Complex: it require some skills to work with kubernetes
restart: you always need to start when minikube when you turn off your machine
not ideal for simple apps: for small apps with very little containers, Kubernetes may be too heavy

Kubernetes is the best solution of deployment for large and scalable projects but for small projects, docker will do the work
