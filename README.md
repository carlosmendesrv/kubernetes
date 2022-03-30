### Ver nodes
kubectl get nodes

### Delete cluster
kind delete clusters kind

### Create Cluster
kind create cluster --config=k8s/kind.yaml --name=fullcycle

### Run Server GO
go run server.go    

### RUN Docker

#### Build
docker build -t carlosmendesrv/hello-go .

#### Generate image
docker run --rm -p 80:80 carlosmendesrv/hello-go 

#### Push
docker push carlosmendesrv/hello-go

### RUN Project

```
### Starting cluster
kind create cluster

### Loading dependences

kubectl apply -f k8s/services.yaml
kubectl apply -f k8s/confimap-family.yaml
kubectl apply -f k8s/deployment.yaml

kubectl port-forward svc/goserver-service 9000:80
```