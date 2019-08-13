# dbaskakov_platform
dbaskakov Platform repository

# Homework 4 (kubernetes-volumes)


```
curl -Lo ./kind-darwin-amd64 https://github.com/kubernetes-sigs/kind/releases/download/v0.4.0/kind-darwin-amd64
chmod +x ./kind-darwin-amd64
mv ./kind-darwin-amd64 /usr/local/bin/kind

kind create cluster
export KUBECONFIG="$(kind get kubeconfig-path --name="kind")"


kubectl get statefulsets
kubectl get pods
kubectl get pvc
kubectl get pv

```

# Homework 3 (kubernetes-networks)

```
iptables --list -nv -t nat

kubectl apply -f

metallb -- https://raw.githubusercontent.com/google/metallb/v0.8.0/manifests/metallb.yaml

minikube cant start with IPVS now =\

kubectl apply -f https://raw.githubusercontent.com/kubernetes/ingress-nginx/master/deploy/static/mandatory.yaml

minikube addons enable ingress

curl -H 'canary: true' http://canary.softpro.site/
```

# Homework 2 (kubernetes-security)
```
kubectl get clusterroles | grep -v system:


kubectl auth can-i get deployments --as system:serviceaccount:prometheus:carol
kubectl auth can-i list pods --as system:serviceaccount:prometheus:carol -n prometheus
```

# Homework 1 (kubernetes-intro)

```
Создали nginx-pod , в который запихнули страничку с помощью initContainer

docker run --rm --name=web -d -p 8000:8000 impel1o/web-pod:v0.1
```