# K8s

## Nginx Ingress
> kubectl apply -f https://raw.githubusercontent.com/kubernetes/ingress-nginx/controller-v1.1.2/deploy/static/provider/cloud/deploy.yaml

## Dashboard
> kubectl apply -f https://raw.githubusercontent.com/kubernetes/dashboard/v2.5.0/aio/deploy/recommended.yaml

## Get token
> token kubectl -n kubernetes-dashboard get secret $(kubectl -n kubernetes-dashboard get sa/admin-user -o jsonpath="{.secrets[0].name}") -o go-template="{{.data.token | base64decode}}"

## Conceitos

| Conceito | Arquivo |
| ------ | ------ |
| Namespace | www-namespace |
| Deployment | www-deployment |
| Service | www-service |
| Ingress | www-ingress |

## Comandos
``` sh
kubectl apply -f www-namespace.yaml
kubectl apply -f www-deployment.yaml
kubectl apply -f www-service.yaml
kubectl apply -f www-ingress.yaml
```
