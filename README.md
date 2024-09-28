# grr-helm

## Parameters

### MariaDB configuration

| Name                        | Description             | Value  |
| --------------------------- | ----------------------- | ------ |
| `mariadb.enabled`           | Enable MariaDB subchart | `true` |
| `mariadb.externalHost`      | MariaDB external host   | `""`   |
| `mariadb.auth.database`     | MariaDB database        | `""`   |
| `mariadb.auth.rootPassword` | MariaDB root password   | `""`   |
| `mariadb.auth.username`     | MariaDB username        | `""`   |
| `mariadb.auth.password`     | MariaDB password        | `""`   |

### GRR image

| Name               | Description    | Value                                      |
| ------------------ | -------------- | ------------------------------------------ |
| `image.repository` | GRR image name | `registry.plmlab.math.cnrs.fr/anf2024/grr` |
| `image.pullPolicy` | Pull policy    | `IfNotPresent`                             |
| `image.tag`        | GRR image tag  | `chart appVersion`                         |

### GRR application configuration

| Name             | Description     | Value |
| ---------------- | --------------- | ----- |
| `replicaCount`   | Replica count   | `1`   |
| `podAnnotations` | Pod annotations | `{}`  |
| `podLabels`      | Pod Labels      | `{}`  |
| `resources`      | Ressources      | `{}`  |
| `livenessProbe`  | Liveness Probe  | `{}`  |
| `readinessProbe` | Readiness Probe | `{}`  |
| `autoscaling`    | Autoscaling     | `{}`  |

### GRR MariaDB secret

| Name                    | Description           | Value  |
| ----------------------- | --------------------- | ------ |
| `secret.create`         | Create secret         | `true` |
| `secret.existingSecret` | Existing secrret name | `""`   |

### GRR service

| Name           | Description  | Value       |
| -------------- | ------------ | ----------- |
| `service.type` | Service type | `ClusterIP` |
| `service.port` | Service port | `8080`      |

### GRR metrics

| Name              | Description    | Value  |
| ----------------- | -------------- | ------ |
| `metrics.enabled` | Enable metrics | `true` |
| `metrics.port`    | Metrics port   | `9090` |

### GRR ingress

| Name                  | Description         | Value   |
| --------------------- | ------------------- | ------- |
| `ingress.enabled`     | Enable ingress      | `false` |
| `ingress.className`   | Ingress class name  | `""`    |
| `ingress.annotations` | Ingress annotations | `{}`    |
| `ingress.hosts`       | Ingress hosts       | `[]`    |
