Running the Application

Navigate to Project Directory: Ensure you're in the directory containing your Kubernetes configuration files

Deploy Resources: Run the following commands in the terminal to deploy your application resources:

kubectl get pod
kubectl apply -f mongo-config.yaml
kubectl apply -f mongo-secret.yaml
kubectl apply -f mongo.yaml
kubectl apply -f webapp.yaml

Accessing the Application

Install Minikube (if necessary): If you haven't already, install Minikube following the official documentation: https://minikube.sigs.k8s.io/docs/start/

Get Minikube IP Address: Run the following command to retrieve the IP address of your Minikube cluster:

minikube ip

This will display the IP address of your Minikube VM.

Access the Application: Open a web browser and navigate to http://<IP_ADDRESS>:30100, replacing <IP_ADDRESS> with the IP address you obtained in the previous step. The port number (30100 in this case) should be retrieved from the nodePort value in your webapp.yaml file.

