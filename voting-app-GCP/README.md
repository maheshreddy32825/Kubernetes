# Setting up Voting Application on GCP
## 1. Create kubernetes cluster on GCP ##
```
Login to GCP https://console.cloud.google.com
select the kubernetes engine
create kubernetes cluster
name: voting-app
region: use default
select all default settings

```
## 2. Connect to cluster and clone the voting app code
```
connect using shell
# To check the created nodes
kubectl get nodes
git clone url
# To create postgres,redis,result,voting,worker
kubectl create -f .
# To verify deployments and service
kubectl get deployments,svc   
```

## 3. Verify
```
                         
```

## 4. create pod and service for postgres
```
kubectl create -f postgres-pod.yaml
kubectl create -f postgres-service.yaml
# To verify pod and service
kubectl get pods,svc                           
```

## 5. create pod and services for worker app
```
kubectl create -f worker-app-pod.yaml
# To verify pod and service
kubectl get pods,svc                           
```

## 6. create pod and services for result app
```
kubectl create -f result-app-pod.yaml
kubectl create -f result-app-service.yaml
# To verify pod and service
kubectl get pods,svc
# URL for result app                            
minikube service result-service --url
```

# Setting up Voting Application on Minikube with Deployments

## 1. login to minikube ##
```
# To check for running pods
kubectl get pods
git clone https://github.com/maheshreddy32825/Kubernetes/tree/main/voting-app
cd voting-app
ls -la
```
## 2. create pod and services for voting app
```
kubectl create -f voting-app-deploy.yaml
kubectl create -f voting-app-service.yaml
# To verify pod and service
kubectl get pods,svc
# URL for voting app                         
minikube service voting-service --url          
```

## 3. create pod and service for redis
```
kubectl create -f redi-deploy.yaml
kubectl create -f redi-service.yaml
# To verify pod and service
kubectl get pods,svc                           
```

## 4. create pod and service for postgres
```
kubectl create -f postgres-deploy.yaml
kubectl create -f postgres-service.yaml
# To verify pod and service
kubectl get pods,svc                           
```

## 5. create pod and services for worker app
```
kubectl create -f worker-app-deploy.yaml
# To verify pod and service
kubectl get pods,svc                           
```

## 6. create pod and services for result app
```
kubectl create -f result-app-deploy.yaml
kubectl create -f result-app-service.yaml
# To verify pod and service
kubectl get pods,svc
# URL for result app                            
minikube service result-service --url
```