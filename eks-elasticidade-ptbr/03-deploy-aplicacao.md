# Deploy da Aplicação

## Deployment

```yaml
apiVersion: apps/v1
kind: Deployment
metadata:
  name: hanoi-app
spec:
  replicas: 1
  selector:
    matchLabels:
      app: hanoi
  template:
    metadata:
      labels:
        app: hanoi
    spec:
      containers:
      - name: hanoi
        image: nginx
        resources:
          requests:
            cpu: "200m"
          limits:
            cpu: "500m"
```

```bash
kubectl apply -f deployment.yaml
```

---

## Service

```yaml
apiVersion: v1
kind: Service
metadata:
  name: hanoi-service
spec:
  type: LoadBalancer
  selector:
    app: hanoi
  ports:
    - port: 80
      targetPort: 80
```

```bash
kubectl apply -f service.yaml
```
