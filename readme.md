test


helm install --debug --dry-run test demoapp

helm template demoapp

helm install --namespace=temp --set env=temp --set tlsEnabled=false --set persistence.enabled=false --set hostName="testdemo.192.168.1.150.nip.io" test-demo-app demoapp

helm uninstall --namespace=temp test-demo-app