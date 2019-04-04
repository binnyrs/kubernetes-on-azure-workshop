# Deploying Kubernetes on Azure


## Register EnableNetworkPolicy 

`az feature register --name EnableNetworkPolicy --namespace Microsoft.ContainerService`

Check to see if it is registered   
`az feature list -o table --query "[?contains(name, 'Microsoft.ContainerService/EnableNetworkPolicy')].{Name:name,State:properties.state}"`  

Refresh the Microsoft.ContainerService  
`az provider register --namespace Microsoft.ContainerService`  

## Create a resource group
`az group create --name k8s --location eastus`

## Create your cluster
To create your cluster please use the script [here](install.sh)

