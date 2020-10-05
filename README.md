# hello-python
Very simple hello world python Flask application.

https://kubernetes.io/blog/2019/07/23/get-started-with-kubernetes-using-python/

## Instructions
### Run app locally
```
pip install -r requirements.txt
python main.py
```

### Run With Docker
```
docker build -f Dockerfile -t hello-python:latest .
docker run -p 5001:5000 hello-python
```

### Run with Kubernetes
Verify kubectl is configured:
`kubectl version`

Windows or Mac: Configure to use Docker for Desktop context
```
kubectl config use-context docker-for-desktop
kubectl get nodes
```

Send YAML config file to Kubernetes
```
kubectl apply -f deployment.yaml
```

See pods running
`kubectl get pods`

Load page at http://localhost:6000/
