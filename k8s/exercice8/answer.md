Exercice 8 :
Pour l’instant, j’ai créé 3 fichiers : le deployment, le service et le configmap, puis je les ai appliqués.

Lorsque j’ai exécuté kubectl apply -f logging-configmap.yaml, Kubernetes a créé mon ConfigMap.

Cependant, j’ai remarqué plus tard que mes pods ne se mettaient pas automatiquement à jour.
J’ai dû les supprimer pour qu’ils soient recréés avec la nouvelle configuration.

La configuration ci‑dessous charge toutes les données du ConfigMap et place chaque clé dans le conteneur :
envFrom: - configMapRef:
name: data-configmap

Si le ConfigMap contient plusieurs clés, toutes ces clés deviennent automatiquement des variables d’environnement.

Nous utilisons un ConfigMap afin d’éviter de reconstruire l’image Docker depuis zéro.
