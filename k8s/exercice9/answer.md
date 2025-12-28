Exercice 9 :

I created a new folder for exercice 9 where I created my deployment file with the tristan12/welcome-to-docker:typexo4 image

I updated the image using : >kubectl set image deployments/welcome-deployment welcome=soufianeremmal/welcome-to-docker:v2

I checked the updated with kubectl rollout status deployments/welcome-deployment

rollout undo is the command to revert changes and put back the old image

Advantages of using set image:

this can be done smoothly while deployment is still available
you can undo changes directly from commands

Disadvantages

Kubernetes doesn't have version tracking for updating images using set image
