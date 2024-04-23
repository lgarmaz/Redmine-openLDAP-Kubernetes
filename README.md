# Redmine-openLDAP-Kubernetes
Despliegue de pods en Kubernetes (Minikube) para hacer funcionar un servidor de Redmine con autenticación a través de OpenLDAP
En este proyecto, desplegamos cuatro aplicaciones en Kubernetes: Redmine, MySQL, OpenLDAP y una UI para éste Protocolo ligero de acceso a directorios. 
Vamos a dividir este léeme en varias secciones explicando como llevar a cabo el proceso paso por paso.

## Requisitos previos

- Tener un clúster de Kubernetes configurado y acceso a él a través de `kubectl`.
- Tener Minikube instalado.
- Tener `kubectl` instalado.

## Despliegue de los Pods Redmine y MySQL.
Redmine es una aplicación de gestión de proyectos y seguimiento de problemas, mientras que MySQL es una base de datos relacional utilizada por Redmine para almacenar datos.


