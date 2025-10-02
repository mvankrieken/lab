# Before

Add argocd.kubernetes.local to /ect/hosts for localhost

# Install
```sh
helm install argo-cd  argo-cd/argo-cd --values values.yaml --namespace argocd --create-namespace
```
# Upgrade
```sh
helm upgrade argo-cd  argo-cd/argo-cd --values values.yaml --namespace argocd --create-namespace
```
# Password
```sh
kubectl -n argocd get secret argocd-initial-admin-secret -o jsonpath="{.data.password}" | base64 -d
```
# Ingress
```sh
kubectl apply -f ingress.yaml -n argocd
```