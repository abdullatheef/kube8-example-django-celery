## About
This repo contains a to-do app, where items can add, list and delete. Also a simple register/signin. Python 3.12, django 5.x, RabbitmQ, Postgres, nginx are the stacks used. This application can run in 3 types of setup

- Straight forward running each application
- docker compose
- kubernetes

### Straight forward running each application

```
./run.sh
```

verify : http://localhost:8010

### docker compose

```
docker-compose up --build
```

verify : http://localhost


### Kubernetes

```
cd kube
kubectl apply -f .
```

In a minikube, 

```
kubectl port-forward pod/<nginx> -n todo-app  8010:80
kubectl port-forward pod/<django> -n todo-app  8000:8000
```
verify : http://localhost:8010


If any issues to start the containers, just kill the containers and automtically restarts.
