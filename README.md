## Desafio 3 - Imersão Full Cycle 3

Criação do cluster via Kind
```sh
kind create cluster
```

Backend:
```sh
kubectl apply -f k8s/backend-configmap.yaml
kubectl apply -f k8s/backend-deployment.yaml
kubectl apply -f k8s/backend-service.yaml
kubectl port-forward service/backend-service 3000:3000
```

Frontend:
```sh
kubectl apply -f k8s/frontend-configmap.yaml
kubectl apply -f k8s/frontend-deployment.yaml
kubectl apply -f k8s/frontend-service.yaml
kubectl port-forward service/frontend-service 3001:3001
```
