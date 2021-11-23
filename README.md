# devops-database

Clone or download the yaml files

Apply configurations sequentially

$ kubectl apply -f mongodb-secret.yaml

$ minikube apply -f mongodb-deploy.yaml

At this time, the mongo db database is ready to connect.

$ kubectl -- get pod -o wide

IP = mongo-deployment pod IP

$ kubectl -- get svc

PORT = mongodb-service port

The db service can be accessed at IP:PORT

--Extra--
Install mongo-express client already connected to the DB

$ kubectl apply -f mongo-configmap.yaml

$ kubectl apply -f mongo-express-deploy.yaml

$ minikube service mongo-express-service

A browser will open with the DB client ready to use
