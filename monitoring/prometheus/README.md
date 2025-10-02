# Install
```sh
helm install prometheus-community prometheus-community/prometheus --values values.yaml --namespace monitoring --create-namespace
```
# Upgrade
```sh
helm upgrade rometheus-community prometheus-community/prometheus --values values.yaml --namespace monitoring --create-namespace
```