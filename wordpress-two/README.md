siege -c 10 http://35.....

kubectl edit deployment wordpress-two

kubectl delete pod wordpress-two-1590106577-lb3db


# ADD
spec:
  template:
    metadata:
      labels:
        app: wordpress-two
    spec:
      containers:
      - name: wordpress
      #XXX
      readinessProbe:
        httpGet:
          path: /
          port: 80

kubectl delete pod wordpress-two-1590106577-lb3db

kubect create -f wordpress-twp/wp-autoscaler.yaml

kubectl get hpa

<waiting>  => nie ma resources


spec:
  replicas: 1
  template:
    spec:
      containers:
      - name: wordpress-two      
        resources:
          requests:
            cpu: 500m
