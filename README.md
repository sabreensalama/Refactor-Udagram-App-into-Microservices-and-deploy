# Refactor-Udagram-App-into-Microservices-and-deploy

## Steps
1. Divide the application into smaller services
2. Containerize the application, create the Kubernetes resource, and deploy it to a Kubernetes cluster.
3. Implement automatic continuous integration (CI) and continuous delivery (CD) using Travis CI
4. Extend the application with deployments and be able to do rolling-updates and rollbacks

## Files
1. udacity-c3-deployment: contain 2 folders, one for docker files and the other for kubernetes deployment with it's services

2. udacity-c3-frontend: it is an ionic microservice for frontend
3. udacity-c3-restapi-feed:  a backend microservice to post new images
4. udacity-c3-restapi-user:  a backend microservice to login/logout

## run the microservices
1. locally

```
docker-compose up
```
2. in kubernetes cluster
```
kubectl port-forward service/frontend 8100:8100
```
```
 kubectl port-forward service/reverseproxy 8080:8080
 ```


## Output