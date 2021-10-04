# Movie Talk infrastructure

## Dry run install
``` bash
helm install --namespace=temp --debug --dry-run --generate-name movietalk
```

## Debug templates

``` bash
helm template movietalk
```

## To install instance via helm (in memory persistance , i.e. erased after pods deleted)
``` bash
kubectl create ns temp

helm install --namespace=temp --set env=temp --set tlsEnabled=false --set persistence.enabled=false --set hostName="temp.192.168.1.150.nip.io" test-demo-app movietalk

# uninstall
helm uninstall --namespace=temp test-demo-app
```