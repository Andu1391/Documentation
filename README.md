# Documentation

# Kubectl Practice: 

#1 - Run a single kubectl command to see all kubernetes resources that can be placed in a namespace

kubectl api-resources --namespaced=true
 
#2 - Run a single kubectl command to see CPU and Memory utilization for the cluster nodes

kubectl top nodes
 
#3 - Run a single kubectl command to deploy a single pod with the nginx image

kubectl run podname --image=nginx
 
#4 - Run a single kubectl command to create a deployment with 3 pod replicas and the nginx image

kubectl create deploy deployname --replicas=3 --image=nginx
 
#5 - Run a single kubectl command which returns a list of all the pods from the kube-system namespace

kubectl get pods -n kube-system
 
#6 - Run a single kubectl command which returns all resources from all namespaces

kubectl get all -A

#7 Go to your Kubernetes cluster environment and using kubectl write a command which counts all pods in the entire cluster and outputs a single line numerical value.
 

Semi-sorted out.

kubectl get pods -A | wc -l

 
#8 Go to your Kubernetes cluster environment and write a kubectl command that shows only a specific pod's container image.
 

Sorted out

kubectl get pods -o=jsonpath='{.items[0].spec.containers[*].image}'
