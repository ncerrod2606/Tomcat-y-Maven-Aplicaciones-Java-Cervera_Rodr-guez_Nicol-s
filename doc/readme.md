# Acceso seguro con Nginx

<p align="left">
<img src="https://img.shields.io/badge/STATUS-FINALIZADO-blue">
</p>

## Índice

1. [Introducción](#introducción)
2. [Instalación de Tomcat](#instalación-de-tomcat)
3. [Configuración de la administración](#configuración-de-la-administración)
4. [Despliegue manual mediante GUI](#despliegue-manual-mediante-gui)
5. [Despliegue con Maven](#despliegue-con-maven)
6. [Tarea](#tarea)
7. [Referencias](#referencias)


---


## Introducción

En esta práctica se realizará la instalación de un servidor web con Tomcat y Maven.

## Instalación de Tomcat

Para instalar Tomcat primero debemos instalar Java, por lo que ejecutamos el siguiente comando:

```
sudo apt install -y openjdk-11-jdk
```

![Instalación de Java](img/cp1.png)

Posteriormente instalamos Tomcat:

```
sudo apt install -y tomcat9
```

![Instalación de Tomcat](img/cp2.png)

Ahora crearemos el grupo de usuarios de Tomcat:

```
sudo groupadd tomcat9
```

![Grupo de usuarios de Tomcat](img/cp3.png)

Creamos el usuario de Tomcat:

```
sudo useradd -s /bin/false -g tomcat9 -d /etc/tomcat9 tomcat9
```

![Usuario de Tomcat](img/cp4.png)

Y arrancamos el servicio de Tomcat:

```
sudo systemctl start tomcat9
```

![Arrancar Tomcat](img/cp5.png)

Para el acceso remoto a Tomcat debemos modificar el archivo de configuración de context.xml:

```
sudo nano /usr/share/tomcat9-admin/host-manager/META-INF/context.xml
```

![Configuración de Tomcat](img/cp6.png)