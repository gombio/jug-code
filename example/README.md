kubectl expose deployment example-nginx --type=LoadBalancer --name=example-service

kubectl describe service example-service

kubectl get service example-service -o yaml
