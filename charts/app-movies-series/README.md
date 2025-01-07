# Conversor Temperatura
App for create list movies and series

## Installing the Chart
```
helm repo add felipetech https://devfelip.github.io/helm-charts/felipetech
helm repo update
helm upgrade --install app-movies-series felipetech/app-movies-series --set application.ingress.hosts[0]=movies.domain.com
```

## Uninstalling the Chart
```
helm uninstall app-movies-series
```

## Global Parameters
| Chave | Tipo | Valor Padrão | Descrição |
|----------|----------|----------|----------|
| application.replicas | int | 1 | Número de réplicas do aplicativo. |
| application.image.name | string | felipecs8/app-movies-series | Nome da imagem Docker. |
| application.image.tag | string | v1 | Tag da imagem Docker. |
| application.service.type | string | ClusterIP | Tipo de serviço Kubernetes (ClusterIP, NodePort, LoadBalancer). |
| application.ingress.enabled | bool | true | Habilita o recurso de Ingress. |
| application.ingress.hosts | array | ["movies.127.0.0.1.nip.io"] | Lista de hosts para o Ingress. |

## GitHub Project
https://github.com/devfelip/app-movies-series