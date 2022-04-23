# K8s

## Nginx Ingress
> kubectl apply -f https://raw.githubusercontent.com/kubernetes/ingress-nginx/controller-v1.1.2/deploy/static/provider/cloud/deploy.yaml

# Dashboard
> kubectl apply -f https://raw.githubusercontent.com/kubernetes/dashboard/v2.5.0/aio/deploy/recommended.yaml

# Get token
> token kubectl -n kubernetes-dashboard get secret $(kubectl -n kubernetes-dashboard get sa/admin-user -o jsonpath="{.secrets[0].name}") -o go-template="{{.data.token | base64decode}}"

## Conceitos

| Conceito | Arquivo |
| ------ | ------ |
| Deployment | www-deployment |
| Sevice | www-service |
| Ingress | www-ingress |

## Comandos
``` sh
kubectl appky -f www-deployment.yaml
kubectl appky -f www-service.yaml
kubectl appky -f www-ingress.yaml
```
