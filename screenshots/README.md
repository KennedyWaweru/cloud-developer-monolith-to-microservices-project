# Screenshots
To help review your infrastructure, please include the following screenshots in this directory::

## Deployment Pipeline
* DockerHub showing containers that you have pushed

![dockerhub](docker-hub.png)

* Travis CI showing a successful build and deploy job
![travis ci](travis-ci-success-build.png)

## Kubernetes
* To verify Kubernetes pods are deployed properly
```bash
kubectl get pods
```

![kubectl get pods](kubectl-get-pods.png)
* To verify Kubernetes services are properly set up
```bash
kubectl describe services
```

![public reverseproxy service](kubectl-describe-service-public-reverseproxy.png)

![reverseproxy service](kubectl-describe-service-reverseproxy.png)

![backend feed service](kubectl-describe-services-backend-feed.png)

![backend user service](kubectl-describe-services-backend-user.png)


![frontend service](kubectl-describe-services-public-frontend.png)

![public frontend service](kubectl-describe-services-frontend.png)

![kubernetes service](kubectl-describe-services-kubernetes.png)


* To verify that you have horizontal scaling set against CPU usage
```bash
kubectl describe hpa
```

![horizontal scaling](kubectl describe hpa.png)

* To verify that you have set up logging with a backend application
```bash
kubectl logs {pod_name}
```
![backend-feed pod log](kubectl logs backend-feed.png)

![backend-user pod log](kubectl logs backend-user.png)
