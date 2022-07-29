# Despliegue Plataforma K8s

Este repositorio contiene todo lo necesario para el despliegue de la arquitectura RPA:
Actualmente, el despliegue de la arquitectura está compuesto de:

- Orquestador (backend)
- Postgres
- Cassandra
- Rabbitmq

En futuros despliegues dispondremos de:

- CDN
- Dashboard

# Instalación


````
```
helm repo add rpa-hercules https://raw.githubusercontent.com/hercules-rpa/despliegue-k8s/main
helm repo update
helm install rpa rpa-hercules/rpa-plataform -n rpa-hercules
```
````
# Desisntalación

````
```
helm uninstall rpa -n rpa-hercules
```
````
