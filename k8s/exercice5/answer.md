Exercice 5
J’ai créé un nouveau dossier que j’ai nommé exercice 5.

J’ai ajouté les fichiers de déploiement pour welcome-docker et gsa avec leurs images respectives.

J’ai créé des services afin de pouvoir ouvrir nos applications.

Étapes pour qu’un service couvre un déploiement :

créer les bons labels, car Kubernetes suit automatiquement les labels

créer un service avec un selector correspondant aux labels définis dans le fichier de déploiement

le service nous fournit une IP et un port stables pour accéder à notre application

Un service peut couvrir plusieurs pods, ce qui est très utile : lorsque les mêmes requêtes sont distribuées sur tous les pods, même si un pod tombe en panne ou cesse de fonctionner, les autres pods continuent de tourner.
Ainsi, l’application reste toujours disponible.
