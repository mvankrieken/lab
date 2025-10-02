# Local agent
Pipelines

# Before
Make sure image tag is same as in yaml templates for agents

# Build image
```sh
./build-image.sh
```
# Install namespace
```sh
kubectl apply -f deployment/agent-namespace.yaml
```
# Install build agent
```sh
kubectl apply -f deployment/agent-deployment-build.yaml
```

# Install customer agent
```sh
kubectl apply -f deployment/agent-deployment-customer.yaml
```

# Provide secrets
Need to be a template for example

```yaml
apiVersion: v1
kind: Secret
metadata:
  name: azdevops
  namespace: az-devops
type: Opaque
data:
  AZP_TOKEN: <base64 encoded>
  AZP_URL: <base64 encoded>
```

and then


```sh
kubectl apply -f deployment/agent-secret.yaml
```