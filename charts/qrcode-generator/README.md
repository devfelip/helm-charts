# QRCode.js
Generate QR Codes in a simplified way

## Installing the Chart
```
helm repo add felipetech https://devfelip.github.io/helm-charts/felipetech
helm repo update
helm upgrade --install qrcode-generator felipetech/qrcode-generator --set application.ingress.hosts[0]=qrcode.domain.com
```

## Uninstalling the Chart

```
helm uninstall qrcode-generator
```

## GitHub Project
https://github.com/devfelip/qrcode-generator


| Chave | Tipo | Valor Padrão | Descrição |
|----------|----------|----------|----------|
| application.replicas | int | 1 | Número de réplicas do aplicativo. |
| application.image.name | string | felipecs8/qrcode-generator | Nome da imagem Docker. |
| application.image.tag | string | v1 | Tag da imagem Docker. |
| application.service.type | string | ClusterIP | Tipo de serviço Kubernetes (ClusterIP, NodePort, LoadBalancer). |
| application.ingress.enabled | bool | true | Habilita o recurso de Ingress. |
| application.ingress.hosts | array | ["qrcode.127.0.0.1.nip.io"] | Lista de hosts para o Ingress. |