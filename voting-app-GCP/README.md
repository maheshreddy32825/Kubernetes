# Setting up Voting Application on Cloud

## 1. Create kubernetes cluster on GCP ##
```
Login to GCP https://console.cloud.google.com
select the kubernetes engine
create kubernetes cluster
name: voting-app
region: use default
select all default settings

```
## 2. Connect to cluster and deploy app
```
connect using shell
# To check the created nodes
kubectl get nodes
git clone url https://github.com/maheshreddy32825/Kubernetes.git
# To create postgres,redis,result,voting,worker
kubectl create -f .
# To verify deployments and service
kubectl get deployments,svc   
```

## 3. Verify app
```
. Once all the service pod are up and also wait for load balance
. From services & ingress section copy the external Ip of both load balancers to access the voting and result app
                         
```