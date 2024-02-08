# k8s-test-app

Sample app running on k8s

## Usage

Please replace `${repository}` below and in [`k8s/deploy.yml`](k8s/deploy.yaml)

```bash
docker build -t k8s-test:latest .
docker tag k8s-test:latest ${repository}/k8s-test:latest
docker push ${repository}/k8s-go-app:latest
kubectl apply -f k8s/deploy.yml -f k8s/service.yml
```

```bash
curl localhost:8080
```

## Requirements

* Docker
* kubectl
