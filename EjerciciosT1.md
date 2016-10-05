# Ejercicios Tema 1. 

*****

## Ejercicio 1. 

 *Consultar en el catálogo de una tienda de informática el precio de un ordenador tipo servidor y calcular su coste de amortización a cuatro y siete años.*
 

1. Tras una búsqueda realizada por varios catálagos he seleccionado el siguiente ordenador: **HP ProLiant ML310e G8 XE E3-1220**, cuyo precio es **769 €**.  

    [HP ProLiant ML310e G8 XE E3-1220](http://es.tinypic.com/r/5161ci.jpg "HP ProLiant ML310e G8 XE")

2. 
*a)* De acuerdo a lo establecido, el coste de amortización a cuatro años se calcula de la siguiente forma: 

*Nota:* Lo máximo a amortizar de forma anual es el 25%, por lo que para los **4 años** ese sería el porcentaje exacto a pagar. 


| Año | Porcentaje |   Total   |
| ----| ---------  | --------- |
|  1  |     25%    |  192.25 € |
|  2  |     25%    |  192.25 € |
|  3  |     25%    |  192.25 € |
|  4  |     25%    |  192.25 € |

*b)* Para la amortización a 7 años existe la posibilidad de realizar un porcentaje exacto en todos los pagos o ir degradándolo gradualmente. 

 - Opción 1. *Porcentaje exacto*, que aunque no es algo exacto ronda el 15%. 
 
| Año | Porcentaje |   Total   |
| ----| ---------  | --------- |
| 1   |    15%     |  115,35 € |
| 2   |    15%     |  115,35 € |
| 3   |    15%     |  115,35 € |
| 4   |    15%     |  115,35 € |
| 5   |    15%     |  115,35 € |
| 6   |    15%     |  115,35 € |
| 7   |    15%     |  115,35 € |

- Opción 2. *Porcentaje degradado*,  
- 
| Año | Porcentaje |   Total   |
| ----| ---------  | --------- |
| 1   |    25%     |  192,25 € |
| 2   |    25%     |  192,25 € |
| 3   |    15%     |  115,35 € |
| 4   |    15%     |  115,35 € |
| 5   |    10%     |    76,9 € |
| 6   |     5%     |   38,45 € |
| 7   |     5%     |   38,45 € |

*****

## Ejercicio 2. 

*Usando las tablas de precios de servicios de alojamiento en Internet y de proveedores de servicios en la nube, comparar el coste durante un año de ordenador con un procesador estándar (escogerlo de forma que sea el mismo tipo de procesador en los dos vendedores) y con el resto de las características similares (tamaño de disco duro equivalente a transferencia de disco duro) en el caso de que la infraestructura comprada se usa sólo el 1% o el 10% del tiempo.*


**** 

## Ejercicio 3. 

*¿Qué tipo de virtualización usarías en cada caso? Comentar en el foro.*

La solución a este apartado se encuentra en el siguiente enlace: https://github.com/JJ/IV16-17/issues/1

*Crear un programa simple en cualquier lenguaje interpretado para Linux, empaquetarlo con CDE y probarlo en diferentes distribuciones.*

El código utilizado es el siguiente. 
 	
```
#!/usr/bin/env python
# -*- coding: utf-8 -*-

n = 1
while n <= 30: 
    print n,
    n += 1
 ```
Los pasos a seguir para la realización de este ejercicio es: 

1. Instalación de cde mediante el siguiente comando: "**sudo apt-get install cde**".

2.  Ejecutamos la orden "**cde python prueba.py**", siendo *prueba.py* el nombre del código mostrado anteriormente, dejando todo empaquetado para su posterior acceso. 

3.  Accedemos al directorio: "**/Escritorio/cde-package/cde-root/home/mmar**."

4. La orden para ejecutar es la siguiente: "**/python .cde prueba.py**".

****

## Ejercicio 4

*Comprobar si el procesador o procesadores instalados tienen estos flags. ¿Qué modelo de procesador es? ¿Qué aparece como salida de esa orden?*

Para comprobar si el procesador tiene instalados los flags en cuestión el comando a introducir es el siguiente:
```
egrep '^flags.*(vmx|svm)' /proc/cpuinfo
 ``` 
 Habiendo obtenido como salida lo mostrado en la siguiente imagen: 
 
[Imagen Comprobación de Flags.](http://i345.photobucket.com/albums/p391/maribhez/salida4_zpslp5gwghq.png "Salida del comando.")

Por otro lado, el modelo de procesador del ordenador desde el que realizo los ejercicios es el siguiente: 

[Imagen Modelo Procesador.](http://i345.photobucket.com/albums/p391/maribhez/modeloProcesador_zpsz4dcmoqy.png "Modelo del Procesador.")

*****


## Ejercicio 5

- *Comprobar si el núcleo instalado en tu ordenador contiene este módulo del kernel usando la orden kvm-ok.*

**KWV** es una infraestructura de Linux encargada de gestionar la aplicación de memoria de invitado al anfitrión, crear los dispositivos virtuales de entrada salida y presentar la salida de video del invitado al anfitrión. 

Así, la salida del comando que comprueba la existencia de dicho módulo es la siguiente: 

[Existencia KVM.](http://i345.photobucket.com/albums/p391/maribhez/kvm_zpsmhbhtk2t.png "KVM.")

Podemos ver de forma clara que sí disponemos de dicho módulo. 

- *Instalar un hipervisor para gestionar máquinas virtuales, que más adelante se podrá usar en pruebas y ejercicios.*

Este ordendador ya tiene instalado **VirtualBox*, por lo que no es necesario realizar ninguna operación adicional en este apartado. 







