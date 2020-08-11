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
### locally using docker 

```
docker-compose up
```
### or from kubernetes cluster
```
kubectl port-forward service/frontend 8100:8100
```
```
 kubectl port-forward service/reverseproxy 8080:8080
 ```
###  connect app with travis ci and it will build and run all od them

## Output
### travis ci
![pass travis ci ](https://github.com/sabreensalama/Refactor-Udagram-App-into-Microservices-and-deploy/blob/master/output/travis-passed.png)
### all running pods
![all pods ](https://github.com/sabreensalama/Refactor-Udagram-App-into-Microservices-and-deploy/blob/master/output/running-pods.png)
### docker hub images 
![docker images](https://github.com/sabreensalama/Refactor-Udagram-App-into-Microservices-and-deploy/blob/master/output/docker-hub.png)
### frontend 
![frontend ](https://github.com/sabreensalama/Refactor-Udagram-App-into-Microservices-and-deploy/blob/master/output/front-end.png)



