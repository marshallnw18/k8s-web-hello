# Kubernetes: Web Hello Demonstration
This project is a quick demonstration of core Kubernetes concepts using a Node.js web application and Minikube. 

## The Application
The web app packaged with this project is built with node.js and just provides a quick "Hello, world!" message along with the accompanying name of the Kubernetes pod that is hosting it. That app is then packaged into a container using the provided Dockerfile. The resulting Docker image is then pushed to a container registry where it can be accessed by k8s. 

## Running the application
To run the application, first clone the repository:

`git clone https://github.com/marshallnw18/k8s-web-hello.git`

Then start Minikube and navigate to the k8s-web-hello directory. Once inside the directory, run:

`kubectl apply -f app-config/`

This will automatically create a Kubernetes deployment of 5 web application ReplicaSets and a load balanced service that will allow you to access the web application. To access the service with Minikube, run:

`minikube service k8s-web-hello`
