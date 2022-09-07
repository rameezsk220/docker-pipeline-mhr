Kubernetes
----------
Steps to install chocolatey in windows10
-------------------------------
Step1
Get-ExecutionPolicy

Step2)
Set-ExecutionPolicy AllSigned


Step3)

Set-ExecutionPolicy Bypass -Scope Process -Force; [System.Net.ServicePointManager]::SecurityProtocol = [System.Net.ServicePointManager]::SecurityProtocol -bor 3072; iex ((New-Object System.Net.WebClient).DownloadString('https://community.chocolatey.org/install.ps1’))

Create EKS cluster in AWS
--------------------------
Step1) Install eksctl in windows 10
choco install -y eksctl

Step2) Install kubectl cli windows 10
choco install -y kubernetes-cli

Step3) create EKS cluster in aws form local desktop
eksctl create cluster \
--version 1.21 \
--region us-east-1 \
--node-type t2.mciro \
--nodes 3 \
--name my-demo-cluster 

ste4) after you work delete cluster( it is not in free tier)



kubectl get nodes  # to list the nodes in the cluster

kubectl run mhr-nginx --image=nginx # create pod through command line
kubectl describe pod mhr-nginx  # to describe pod

kubectl exec -it <container name> /bin/bash  # for login the container
