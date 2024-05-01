## 1. login to minikube ##
```
kubectl get pods -- to see any running pods
git clone url
cd voting-app
ls -la
```
## 2. create pod and services for voting app
```
kubectl create -f voting-app-pod.yaml
kubectl create -f voting-app-service.yaml
kubectl get pods,svc                           -- it will list pod and service
minikube service voting-service --url          ----- this will provide URL for voting to access
```

## 3. create pod and service for redis
```
kubectl create -f redi-pod.yaml
kubectl create -f redi-service.yaml
kubectl get pods,svc                           -- it will list pod and service
```

## 4. create pod and service for postgres
```
kubectl create -f postgres-pod.yaml
kubectl create -f postgres-service.yaml
kubectl get pods,svc                           -- it will list pod and service
```

## 5. create pod and services for worker app
```
kubectl create -f worker-app-pod.yaml
kubectl get pods,svc                           -- it will list pod and service
```

## 6. create pod and services for result app
```
kubectl create -f result-app-pod.yaml
kubectl create -f result-app-service.yaml
kubectl get pods,svc                           -- it will list pod and service
minikube service result-service --url          ----- this will provide URL for voting to access
```
