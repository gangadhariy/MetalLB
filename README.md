# MetalLB Configuration
## First you need to install metallb in your cluster run the following command
```
kubectl apply -f https://raw.githubusercontent.com/metallb/metallb/main/config/manifests/metallb-native.yaml
```
## Now check the pods running or not
```
kubectl get pods -n metallb-system
```
## make sure all pods are running
## Now Apply ip.yaml
```
kubectl apply -f ip.yaml
```
```
kubectl get ipaddresspool -n metallb-system
```
```
kubectl get l2advertisement -n metallb-system
```
## If everything working fine test Loadbalancer by deploying simple app and expose it with LoadBalancer
```
kubectl apply -f nginx.yaml
```
