# testhub-helm
Helm chart repo for TestHub

# Usage

Create a `values.yaml` file:

```
ingress:  
  frontend:
    annotations: 
      # kubernetes.io/ingress.class: nginx
      # kubernetes.io/tls-acme: "true"
    host: testhub-frontend.local    
  api:
    host: testhub-api.local    
    
volume:
  size: 1Gi
```

Add testhub helm repo and install chart

```
helm repo add testhub https://testhub-io.github.io/testhub-helm
helm repo update
helm install testhub testhub/testhub -n test-hub -f values.yaml
```
