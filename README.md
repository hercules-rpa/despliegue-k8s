# Despliegue Plataforma K8s

Este repositorio contiene todo lo necesario para el despliegue de la arquitectura RPA:
Actualmente, el despliegue de la arquitectura está compuesto de:

- Orquestador (backend)
- Postgres
- Cassandra
- Rabbitmq
- CDN
- Dashboard

# Instalar repositorio Helm



```
helm repo add rpa-hercules https://raw.githubusercontent.com/hercules-rpa/despliegue-k8s/main
helm update repo
```


# Instalar la plataforma RPA

Para la correcta instalación se recomienda ver los valores que se desean modificar con el comando:

```
helm show values rpa-plataform/rpa-plataform
```

Un ejemplo de instalación modificando los storageClass e indicando que se desea instalar postgres

```
 helm install rpa rpa-plataform/rpa-plataform  --set cassandra.volumeClaim.storageClassName=openebs-hostpath --set postgres.volumeClaim.storageClassName=openebs-hostpath --set cdn.volumeClaim.storageClassName=openebs-hostpath  --set postgres.install=true -n rpa-hercules
```

