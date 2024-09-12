# ArgoCD playground

## Installation
kind create cluster

kubectl create ns argocd
kubectl apply -n argocd -f https://raw.githubusercontent.com/argoproj/argo-cd/master/manifests/install.yaml

## Dashboard UI
`argocd admin dashboard -n argocd`
or
`kubectl port-forward svc/argocd-server -n argocd 8080:443`

## Configuration
kubectl apply -f argocd/argocd-cm.yaml
kubectl apply -f argocd/argocd-cmd-params-cm.yaml

## Application
kubectl apply -f application.yaml

## App of apps
kubectl apply -f app-of-apps/app-of-apps-guestbook.yaml