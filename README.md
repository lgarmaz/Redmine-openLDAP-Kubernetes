# Redmine-openLDAP-Kubernetes
Despliegue de pods en Kubernetes (Minikube) para hacer funcionar un servidor de Redmine con autenticación a través de OpenLDAP
En este proyecto, desplegamos cuatro aplicaciones en Kubernetes: Redmine, MySQL, OpenLDAP y una UI para éste Protocolo ligero de acceso a directorios. 
Vamos a dividir este léeme en varias secciones explicando como llevar a cabo el proceso paso por paso.

## Requisitos previos

- Tener un clúster de Kubernetes configurado y acceso a él a través de `kubectl`.
- Tener Minikube instalado.
- Tener `kubectl` instalado.
- Crear tres carpetas que nos servirán como volúmenes persistentes locales con la siguiente estructura:
    - redmine-pv
        - redmine-data
        - plugins
    - mysql-pv
        - db

  **En este caso he puesto los nombres que he utilizado yo, pero estos nombres e incluso esta estructura puede ser modificada siempre que se referencien bien el los ficheros correspondientes**
  
## Despliegue de los Pods Redmine y MySQL.
Redmine es una aplicación de gestión de proyectos y seguimiento de problemas, mientras que MySQL es una base de datos relacional utilizada por Redmine para almacenar datos.
Para desplegar los pods correspondientes a estas dos aplicaciones, hay que descargar o crear los siguientes archivos: 
- `redmine-mysql-deployment.yaml`
- `mysql-pv.yaml`
- `redmine-pv-data.yaml`
- `redmine-pv-plugins.yaml`
- `service.yaml`

Una vez descargados o creados (en este último caso, pegando el contenido de los ficheros presentes en este repositorio con el mismo nombre), los ubicamos todos en una misma carpeta y lo desplegamos utilizando `kubectl apply -f .` .
Si todos los pods están en estado "running", significa que se han desplegado correctamente.
Para realizar la comprobación, utilizamos el comando `minikube ip` para averiguar la ip del nodo y escribimos dicha ip en el buscador junto con el puerto 32000 (`ip:32000`) que es el puerto utilizado poir redmine. Si nos lleva hasta la WebUI de esta aplicación, todo está correcto.


