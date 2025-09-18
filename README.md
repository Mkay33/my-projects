This is my new project

Another thing here
#### 1. Application setup

This is simple nodejs app starts on port 3000 and logs 1 line into elastic search which is running in a minikube cluster
Elastic endpoint configured in Pino is the es service name in Mnikube.

##### to prepare the app for startup, installing all the dependencies

npm install

##### to start the application

npm start or node app/server.js

##### to build the image from Dockerfile

docker build -t nodejs-app:1.0 .
###### to start the built docker image
docker run nodejs-app:1.0

#### 2. Deploy on Minikube
(pre-requisite elastic search setup in Minikube)

##### build the uptodate image INSIDE MINIKUBE (this way docker won't have to pull the image from repo, it will be the one existing locally)
Set docker remote to Minikube's docker
