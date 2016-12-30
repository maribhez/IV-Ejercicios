# Ejercicios Tema 4. 

# Virtualización *ligera* usando contenedores. 


## Ejercicio 1.
 

**Instala LXC en tu versión de Linux favorita. Normalmente la versión en desarrollo, disponible tanto en GitHub como en el sitio web está bastante más avanzada; para evitar problemas sobre todo con las herramientas que vamos a ver más adelante, conviene que te instales la última versión y si es posible una igual o mayor a la 1.0.**

Para la instalación de *LXC* ha sido introducir el siguiente comando: *sudo apt-get install lxc*, y podemos comprar la versión que ha sido instalada sin más que introducir *lxc-start --version*.
 

![Instalacion](http://i345.photobucket.com/albums/p391/maribhez/Captura%20de%20pantalla%20de%202016-12-29%2011-48-09_zpsrzgbengm.png "Instalacion")

![Instalacion](
http://i345.photobucket.com/albums/p391/maribhez/Captura%20de%20pantalla%20de%202016-12-29%2011-49-19_zpszljczbge.png "Version LXC")

## Ejercicio 2. 

**Comprobar qué interfaces puente se han creado y explicarlos.**

Una vez creado el primer contenedor podemos comprobar que aparece en la lista de contenedores con su estado actual usando el comando *sudo lxc-list*.

![Cajas](http://i345.photobucket.com/albums/p391/maribhez/Captura_zps9vhbp0n4.png "Cajas")

El nombe de dicha caja es **una-caja**,  y una vez hemos accedido a ella nos queda el prompt de la siguiente forma: *ubuntu@una-caja*, donde *ubuntu* es el sistema operativo con el que creamos dicha caja. 

Para conocer las interfaces que hay dentro de una máquina usamos *ifconfig -a*, obteniendo lo mostrado en la siguiente captura. 

![Interfaces](http://i345.photobucket.com/albums/p391/maribhez/Captura2_zpsbhvhhzed.png "Interfaces")

Si salimos fuera de dicha máquina y ejecutamos el mismo comando vemos más interfaces creadas con la creación de la propia máquina. 

##Ejercicios 3.

### Ejercicio 3.1. 

**Crear y ejecutar un contenedor basado en Debian.**

Para crear un contenedor basado en debian se usa *sudo lxc-create -n nombreContenedor -t debian*.

![Debian](http://i345.photobucket.com/albums/p391/maribhez/Captura%20de%20pantalla%20de%202016-12-29%2018-48-41_zpsbsuvyghr.png "Debian")

Después de esto, para ejecutarlo se usan los siguietnes comandos, introduciendo posteriormente los datos acceso de nuestra máquina: 

>sudo lxc-start -n nombreContenedor -d

>sudo lxc-console -n nombreContenedor


### Ejercicio 3.2. 

**Crear y ejecutar un contenedor basado en otra distribución, tal como *Fedora*.**

***Nota*: En general, crear un contenedor basado en tu distribución y otro basado en otra que no sea la tuya. Fedora, al parecer, tiene problemas si estás en Ubuntu 13.04 o superior, así que en tal caso usa cualquier otra distro. Por ejemplo, Óscar Zafra ha logrado instalar Gentoo usando un script descargado desde su sitio, como indica en este comentario en el issue.**
 
He creado un contenedor basado en Fedora sin más que introducir ***-t fedora*** donde antes habíamos indicado ***-t debian***.

![Fedora](http://i345.photobucket.com/albums/p391/maribhez/Captura%20de%20pantalla%20de%202016-12-29%2019-08-47_zps6fcflyax.png "Fedora")

Este cotenedor se ejecuta de la misma forma que la anterior. 

##Ejercicios 4. 


### Ejercicio 4.1. 


**Instalar lxc-webpanel y usarlo para arrancar, parar y visualizar las máquinas virtuales que se tengan instaladas.**


Para instalar *lxc-webpanel* introducimos **wget https://lxc-webpanel.github.io/tools/install.sh -O - | bash** y para acceder a él entramos a **http://localhost:5000/ en nuestro navegador. 

Una vez accedemos al navegador nos aparece este canal, mostrando los tres contenedores creados anteriormente además de la información referente a la máquina anfitriona. 

![Panel](http://i345.photobucket.com/albums/p391/maribhez/Captura%20de%20pantalla%20de%202016-12-29%2019-44-38_zpsrc2zw54r.png "Panel") 

Se puede arrancar el contendedor de forma extremadamente sencilla, y es que sólo es necesario darle a un botón. En la siguiente captura se muestra el contenedor de Debian arrancado (color verde). 

![Arranque](http://i345.photobucket.com/albums/p391/maribhez/4-2_zps8ucvwxjj.png "Arranque")

Después de esto, podemos parar la máquina y acceder a la configuración específica de un contenedor, y en este caso yo he limitado la memoria básica y la memoria con intercambio. 


![Limitación](http://i345.photobucket.com/albums/p391/maribhez/4-3_zpsbna0iqet.png "Limitacion")




## Ejercicio 6. 

**Instalar docker.**

Después de comprobar que tenemos instalados los certificados necesarios y añadir a nuestro sistema otro repositorio adicional introducimos el comando *sudo apt-get install docker-engine* y queda instalado docker en nuestro sistema. 


![Instalacion Docker](http://i345.photobucket.com/albums/p391/maribhez/Captura_zpsogbxjccr.png "Instalacion Docker") 


## Ejercicios 7. 

### Ejercicio 7.1. 

**Instalar a partir de docker una imagen alternativa de Ubuntu y alguna adicional, por ejemplo de CentOS.**

Para instalarlo es necesario el comando *sudo docker pull < distribucion >*.

Así, para instalar Ubuntu: 

![Ubuntu Docker](http://i345.photobucket.com/albums/p391/maribhez/Captura_zpsv7wpal8x.png "Ubuntu Docker")

Y para instalar CentOS:

![Ubuntu CentOS](http://i345.photobucket.com/albums/p391/maribhez/Captura2_zpsanqw1lwd.png "Ubuntu CentOS")

###Ejercicio 7.2.

**Buscar e instalar una imagen que incluya MongoDB.**

Para buscar las imágenes que incluyen mongo hay que usar *sudo docker search mongo*.

![Búsqueda](http://i345.photobucket.com/albums/p391/maribhez/Captura3_zpsjccpyouv.png "Búsqueda")

Y para instarlar he escogido la primera opción de todas las que se presentan. Por lo tanto, queda de la siguiente manera: 

![Mongo](http://i345.photobucket.com/albums/p391/maribhez/Captura4_zpsoanrhykx.png "Mongo")


## Ejercicio 8. 

**Crear un usuario propio e instalar nginx en el contenedor creado de esta forma.**

Arrancamos Ubuntu con *sudo docker run -i -t ubuntu /bin/bash* y creamos un usuario con *adduser nombre*.

![Ubuntu](http://i345.photobucket.com/albums/p391/maribhez/Captura_zpsp53skr8s.png "Ubuntu")

Además, hemos de añadir al usuario recien creado al grupo **sudo** para poder instalar sin problemas *nginx* posteriormente. 

Accedemos después al usuario con *login usuario_docker* y procedemos a instalar *nginx* (usando sudo apt-get install -y nginx) y lanzamos el servicio.

![Lanzar nginx](http://i345.photobucket.com/albums/p391/maribhez/Captura2_11_zpsqoexhvtn.png "Lanzar nginx")



Ahora instalamos **curl** para comprobar asi el correcto funcionamiento de **nginx**. 

![Curl](http://i345.photobucket.com/albums/p391/maribhez/Captura2_2_zpsnjmb18eg.png "Curl")

Lanzamos **curl localhost** y así queda demostrado. 

![Localhost](http://i345.photobucket.com/albums/p391/maribhez/Captura3_zpslogsdzey.png "Localhost")

## Ejercicio 9. 


**Crea a partir del contenedor anterior una imagen persistente con commit.**

Nos hace falta para esto el identificador del contenedor a la que le vamos a hacer *commit*, y es por eso que usamos *sudo docker ps -a*. 

![ID](http://i345.photobucket.com/albums/p391/maribhez/Captura_zpsmdusbd3d.png "ID")

Y así, buscando con *sudo docker inspect* el identificador completo podemos hacer el commit finalmente. 
![Commit](http://i345.photobucket.com/albums/p391/maribhez/Captur2a_zpsdt8sxoxm.png "Commit")