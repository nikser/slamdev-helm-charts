# weblate

![Version: 0.0.7](https://img.shields.io/badge/Version-0.0.7-informational?style=flat-square) ![Type: application](https://img.shields.io/badge/Type-application-informational?style=flat-square) ![AppVersion: 3.11.3-1](https://img.shields.io/badge/AppVersion-3.11.3--1-informational?style=flat-square)

Helm chart to deploy [weblate](https://hub.docker.com/r/weblate/weblate/).

**Homepage:** <https://github.com/slamdev/helm-charts/tree/master/charts/weblate>

## Maintainers

| Name | Email | Url |
| ---- | ------ | --- |
| slamdev | valentin.fedoskin@gmail.com |  |

## Values

| Key | Type | Default | Description |
|-----|------|---------|-------------|
| affinity | object | `{}` | affinity for scheduler pod assignment |
| chownDataVolumeAs | string | `"1000:1000"` | specifies an owner of data volume |
| env | list | `[]` | environment variables for the container |
| envFrom | list | `[]` | environment variable sources for the container |
| fullnameOverride | string | `""` | full name of the chart. |
| image.pullPolicy | string | `"IfNotPresent"` | image pull policy |
| image.repository | string | `"weblate/weblate"` | image repository |
| image.tag | string | `""` | image tag (chart's appVersion value will be used if not set) |
| imagePullSecrets | list | `[]` | image pull secret for private images |
| ingress.annotations | object | `{}` | ingress annotations |
| ingress.enabled | bool | `false` | enables Ingress for weblate |
| ingress.hosts | list | `[]` | ingress accepted hostnames |
| ingress.tls | list | `[]` | ingress TLS configuration |
| livenessProbe.httpGet.path | string | `"/healthz/"` | path for liveness probe |
| livenessProbe.httpGet.port | string | `"http"` | port for liveness probe |
| livenessProbe.initialDelaySeconds | int | `45` |  |
| nameOverride | string | `""` | override name of the chart |
| nodeSelector | object | `{}` | node for scheduler pod assignment |
| podSecurityContext | object | `{}` | specifies security settings for a pod |
| readinessProbe.httpGet.path | string | `"/healthz/"` | path for readiness probe |
| readinessProbe.httpGet.port | string | `"http"` | port for readiness probe |
| readinessProbe.initialDelaySeconds | int | `45` |  |
| resources | object | `{}` | custom resource configuration |
| securityContext | object | `{}` | specifies security settings for a container |
| service.annotations | object | `{}` | service annotations |
| service.port | int | `80` | service port |
| service.type | string | `"ClusterIP"` | service type |
| serviceAccount.annotations | object | `{}` | annotations to add to the service account |
| serviceAccount.create | bool | `false` | specifies whether a service account should be created |
| serviceAccount.name | string | `nil` | the name of the service account to use; if not set and create is true, a name is generated using the fullname template |
| tolerations | list | `[]` | tolerations for scheduler pod assignment |
| volumeClaimTemplates | list | `[]` | volume claim templates |
| volumeMounts | list | `[]` | additional volume mounts |
| volumes | list | `[{"emptyDir":{},"name":"data"}]` | volumes |
