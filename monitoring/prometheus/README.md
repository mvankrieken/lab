# Before

Add grafana.kubernetes.local to /ect/hosts for localhost

# Repo
```sh
helm repo add prometheus-community https://prometheus-community.github.io/helm-charts
```

# Install
```sh
helm install prometheus-community prometheus-community/prometheus --values values.yaml --namespace monitoring --create-namespace
```
# Upgrade
```sh
helm upgrade rometheus-community prometheus-community/prometheus --values values.yaml --namespace monitoring --create-namespace
```