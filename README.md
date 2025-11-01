## Hashicorp-Vault-k8s

Create the vault namespace:

```bash
kubectl create namespace vault
```

Add the HashiCorp Helm repository

```bash
helm repo add hashicorp https://helm.releases.hashicorp.com
```

Install HashiCorp Vault using Helm:

```bash
helm repo add hashicorp https://helm.releases.hashicorp.com
helm install vault hashicorp/vault \
  --set="server.dev.enabled=true" \
  --set="ui.enabled=true" \
  --set="ui.serviceType=NodePort" \
  --namespace vault
```


