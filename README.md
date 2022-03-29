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

kind create cluster

kubectl apply -f k8s/service.yaml  

kubectl port-forward svc/goserver-service 9000:80

```