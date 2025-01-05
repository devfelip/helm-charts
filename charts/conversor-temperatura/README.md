# Conversor Temperatura
App para converter a temperatura

## Installing the Chart
```
helm repo add conversor-temp https://devfelip.github.io/qrcode-generator/charts
helm repo update
helm install conversor-temp qrcode-generator/qrcode-generator --set application.ingress.hosts[0]=conversor-temp.domain.com
```
## Uninstalling the Chart

```
helm uninstall conversor-temp
```

## GitHub Project
https://github.com/devfelip/conversor-temp


| Chave | Tipo | Valor Padrão | Descrição |
|----------|----------|----------|----------|
| application.replicas | int | 1 | Número de réplicas do aplicativo. |
| application.image.name | string | felipecs8/conversor-temperatura | Nome da imagem Docker. |
| application.image.tag | string | v1 | Tag da imagem Docker. |
| application.service.type | string | ClusterIP | Tipo de serviço Kubernetes (ClusterIP, NodePort, LoadBalancer). |
| application.ingress.enabled | bool | true | Habilita o recurso de Ingress. |
| application.ingress.hosts | array | ["conversor-temp.127.0.0.1.nip.io"] | Lista de hosts para o Ingress. |