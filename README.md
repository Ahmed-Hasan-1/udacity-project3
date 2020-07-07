# refactor-udagram-app-into-microservices-and-deploy
Udacity Cloud Developer Nanodegree Program - project  4


## About Project:
The project aims at 
                    
                    - Dividing the application into smaller services
                    - Containerizing the application, create the Kubernetes resource, and deploy it to a Kubernetes cluster.
                    - Implementation of automatic continuous integration (CI) and continuous delivery (CD) using Travis CI.
                    - Extending the application with deployments and be able to do rolling-updates and rollbacks
## Technical Info:
Project has docker-compose file to run docker containers, each docker container has some services which are : frontend service, rest API user service, and rest API feed service. both user and feed use the same port and reverseproxy control the incoming traffic between them.
Also, the project has kubernete which run each docker dontainer inside pod in cluster.


1- Run docker compose 
docker-compose up

2- Port-forward 
kubectl port-forward service/frontend 8100:8100
kubectl port-forward service/reverseproxy 8080:8080

