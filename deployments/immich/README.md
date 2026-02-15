First install the dependencies like normal

```
k apply -k .
```

Then install the immich helm chart like this:
```
bash -c '. .env.immich && helm install --create-namespace --namespace immich immich oci://ghcr.io/immich-app/immich-charts/immich -f values.yaml --set server.controllers.main.containers.main.env.DB_PASSWORD=$DB_PASSWORD'
```

assuming .env.immich contains

```
DB_PASSWORD=somepassword_here
```
