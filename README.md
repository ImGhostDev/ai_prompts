# Репозиторій MyApp

Цей репозиторій містить маніфести YAML для розгортання та налаштування додатку MyApp у Kubernetes.

## Файли YAML

| NAME                     | PROMPT                                                                                                          | DESCRIPTION           | EXAMPLE                                  |
|--------------------------|-----------------------------------------------------------------------------------------------------------------|-----------------------|------------------------------------------|
| app.yaml                 | "create app.yml"                                                                                                | Опис додатку MyApp    | [app.yaml](yaml/app.yaml)                |
| app-livenessProbe.yaml   | create app for image nginx with livenessProbe in namespace demo                                                 | Liveness Probe        | [app-livenessProbe.yaml](yaml/app-livenessProbe.yaml)   |
| app-readinessProbe.yaml  | create pod for gcr.io/k8s-k3s/demo:v2.0.0 with liveness and readiness probe                                                                                                                | Readiness Probe       | [app-readinessProbe.yaml](yaml/app-readinessProbe.yaml) |
| app-volumeMounts.yaml    | create pod for gcr.io/kuar-demo/kuard-amd64:1 with liveness and readiness probe, mount volume data with hostPath /var/lib/app                                                                                                                | Volume Mounts         | [app-volumeMounts.yaml](yaml/app-volumeMounts.yaml)     |
| app-cronjob.yaml         | create CronJob which will print Hello world for  each 5 min                                                     | CronJob               | [app-cronjob.yaml](yaml/app-cronjob.yaml)               |
| app-job.yaml             | створити  job для синхронізації даних з Google Cloud Storage до Google Compute Engine Persistent Disk за допомогою gsutil | Job                   | [app-job.yaml](yaml/app-job.yaml)                       |
| app-multicontainer.yaml  | create multicontainer for nginx and debian which will add current date to file index.html                       | Мультиконтейнерний Pod | [app-multicontainer.yaml](yaml/app-multicontainer.yaml) |
| app-resources.yaml       | create pod for gcr.io/k8s-k3s/demo:v2.0.0 with liveness and readiness probe and limit resourses to 100m cpu and 256Mi memory                                                                                                                | Ресурси контейнера    | [app-resources.yaml](yaml/app-resources.yaml)           |
| app-secret-env.yaml      | create pod for container redis with env secret_username and secret_password from secretkeyref                                                                                                                | Секрети та змінні середовища | [app-secret-env.yaml](yaml/app-secret-env.yaml)     |

