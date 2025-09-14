# Commands
```
minikube status
minikube dashboard

kubectl apply -f pod.yaml
kubectl port-forward pod/hello-pod 8080:5678
curl http://localhost:8080

kubectl scale deployment hello-deployment --replicas=5
kubectl get pods -l app=hello


kubectl get svc hello-service
kubectl run test-client --rm -it --image=busybox:1.36 -- sh
# Inside client pod:
wget -qO- http://hello-service

# NodePort Minikube Check
minikube service hello-nodeport --url

# LoadBalancer Minikube Check
kubectl apply -f lb.yaml
minikube tunnel
kubectl get svc hello-loadbalancer

kubectl get pvc
kubectl get pv

# Enable Minikube Ingress Addon
minikube addons enable ingress

Update /etc/hosts on your machine

Get Minikube IP:
minikube ip

Edit /etc/hosts (Linux/macOS) or C:\Windows\System32\drivers\etc\hosts (Windows):

<MINIKUBE_IP> hello.test

Now open:
http://hello.test

curl http://hello.test

