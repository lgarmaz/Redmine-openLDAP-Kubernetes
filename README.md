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
    |-- redmine-data
    |-- plugins
- mysql-pv
    |-- db

  *En este caso he puesto los nombres que he utilizado yo, pero estos nombres e incluso esta estructura puede ser modificada siempre que se referencien bien el los ficheros correspondientes*
  
## Despliegue de los Pods Redmine y MySQL.
Redmine es una aplicación de gestión de proyectos y seguimiento de problemas, mientras que MySQL es una base de datos relacional utilizada por Redmine para almacenar datos.


