Exercice 5

I created a new folder and named it exercice 5

I added deployment files for both welcome-docker and gsa with their images

I created services in order to open our apps

steps for a service to cover a deployment

- create correct labels because kubernetes tracks labels automatically
- create a service with selector matching the labels in the deployment file created
- the service will hand us a stable ip and port where we can open our app

a service can cover multiple pods, it is useful because when the same requests are distributed on all pods, even if a pod crashed or stopped working, other pods will still be running, therefore the application will always be available
