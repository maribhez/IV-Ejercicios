#Ejercicios 6.

## Ejercicio 1.

**Instalar chef en la máquina virtual que vayamos a usar.**

He usado para la instalación el comando indicado en el [guion](http://jj.github.io/IV/documentos/temas/Gestion_de_configuraciones "guion") de la asignatura.

El comando usado ha sido el siguiente:

~~~
curl -L https://www.opscode.com/chef/install.sh | bash
~~~

Para mostrar que la instalación se ha llevado a cabo sin problema ninguno muestro aquí la captura donde podemos comprobar que **chef** ha sido instalado.

![chefinstalado](http://i345.photobucket.com/albums/p391/maribhez/chef_zpsi0jlfjoo.png "chefinstalado")

## Ejercicio 4.

**Instalar una máquina virtual Debian usando vagrant y conectar con ella.**


Para empezar ejercicio ha sido necesario tan solo el comando **vagrant init debial/jessie64**, consiguiendo con ello el archivo *Vagranfile* que permite crear la máquina virtual.

Dicho archivo se crea con la configuración básica:

![Vagrant](http://i345.photobucket.com/albums/p391/maribhez/vagrantdebian_zpsafzhky5l.png "Vagrant")

Haciendo uso de *vagrant ssh* accedemos a la máquina recién creada.

![SSH](http://i345.photobucket.com/albums/p391/maribhez/ssh_zpsgfcrox5m.png "SSH")

A modo de resumen, los comandos necesarios han sido:
~~~
vagrant init debian/jessie64
vagrant up
vagrant ssh
~~~

## Ejercicio 5.

**Crear un script para provisionar 'nginx' o cualquier otro servidor web que pueda ser útil para alguna otra práctica. **
