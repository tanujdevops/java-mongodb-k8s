# Java application with MongoDB on Kubernetes
This guide will walk you through deploying a Java application with MongoDB on a Kubernetes cluster.

### Prerequisites
Before getting started, you'll need to have the following installed:
```
Kubernetes
Minikube
Docker
kubectl
Postman
```
### Steps
Clone this repository to your local machine.
Open a terminal window and navigate to the project directory.
Start Minikube with the following command:
```
minikube start
```
Set the Docker environment variables with the following command:
```
eval $(minikube docker-env)
```
Apply the Kubernetes configuration files with the following command:
```
kubectl apply -f kubernetes/
```
Wait for the pods and services to be created by running the following command:
```
kubectl get pods,services
```
In Postman, make a GET request to the following URL:
```
http://<NODE_IP>:<NODE_PORT>/<API_ENDPOINT>
```
Replace <NODE_IP> and <NODE_PORT> with the IP and port of the serverapi service, and <API_ENDPOINT> with the endpoint of your Java application.

You should see the response from your Java application in the Postman window.
To stop the Minikube cluster, run the following command:
```
minikube stop
```
### Conclusion
In this guide, we've walked through deploying a Java application with MongoDB on a Kubernetes cluster. We've covered how to build Docker images, apply Kubernetes configuration files, and test the application using Postman. With this knowledge, you can now deploy your own Java applications on Kubernetes.
