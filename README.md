# ArgoCD playground

## Installation

kubectl create ns argocd
kubectl apply -n argocd -f https://raw.githubusercontent.com/argoproj/argo-cd/master/manifests/install.yaml
argocd admin dashboard -n argocd

## Application
kubectl apply -f application.yaml