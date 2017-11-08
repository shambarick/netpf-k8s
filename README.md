Create the `netpf` namespace

```
kubectl create namespace netpf
```

Deploy zipcode

```
curl -L -s https://github.com/shambarick/netpf-k8s/raw/master/zipcode-deployment.yaml | kubectl apply -f -
curl -L -s https://github.com/shambarick/netpf-k8s/raw/master/zipcode-svc.yaml | kubectl apply -f -
```

Deploy organism

```
curl -L -s https://github.com/shambarick/netpf-k8s/raw/master/organism-deployment.yaml | kubectl apply -f -
curl -L -s https://github.com/shambarick/netpf-k8s/raw/master/organism-svc.yaml | kubectl apply -f -

```

Deploy news

```
curl -L -s https://github.com/shambarick/netpf-k8s/raw/master/news-deployment.yaml | kubectl apply -f -
curl -L -s https://github.com/shambarick/netpf-k8s/raw/master/news-svc.yaml | kubectl apply -f -
```

Deploy procedure

```
curl -L -s https://github.com/shambarick/netpf-k8s/raw/master/procedure-deployment.yaml | kubectl apply -f -
curl -L -s https://github.com/shambarick/netpf-k8s/raw/master/procedure-svc.yaml | kubectl apply -f -
```

Create a PersistentVolume (Requires Kubernetes 1.8 and not tested yet)

```
kubectl label nodes node5 db=true
mkdir -p /data/organism-db
chmod 777 -R /data/
```
