# Commands related to Azure Container Service (AKS)

## Enable AKS preview for subscription

```bash

az provider show -n Microsoft.ContainerService

```

## Monitor state of registration

```bash

az provider show -n Microsoft.ContainerService

```

## Create Resource Group 

```bash

az group create \
--name k8sResourceGroup \
--location "East US"

```

## Create AKS cluster

```bash

az aks create \
--resource-group k8sResourceGroup \
--name coreDemoAKSCluster \
--node-count 2

```

## Connect to AKS cluster

```bash

az aks get-credentials --resource-group k8sResourceGroup \
--name coreDemoAKSCluster

```

## Verify connection to cluster

```bash

kubectl get nodes

```

## Browse AKS cluster dashboard

```bash

az aks browse --resource-group k8sResourceGroup \
--name coreDemoAKSCluster

```

## Delete resource group

```bash

az group delete --name k8sResourceGroup --yes --no-wait

```