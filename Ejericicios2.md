#Ejercicios Tema 2.

##

###Ejericicio 1.

**Instalar alguno de los entornos virutales de node.js (o de cualquier otro lenguaje con el que esté familiarizado) y, con ellos, instalar la última versión existente, la versión minor más actual de la 4.x y lo mismo para la 0.11 o alguna impar (de desarrollo).**

- ***NVM - Node Version Maganer (Gestor de versiones de Node).***


Tal y como su nombre indica, se encarga de controlar diferentes versiones en un mismo ambiente, dejando cada una completamente aislada de las otras. Se puede llevar a cabo lo pedido en este ejercicio gracias a estas prestaciones: tener instaladas Node v0.4 y v.011 ejecutándolas según nuestras necesidades.


![Instalación NVM](http://i345.photobucket.com/albums/p391/maribhez/instalacionNMV_zps5syy2rus.png "Instalación NVM.")

![Comprobación de instalación correcta](http://i345.photobucket.com/albums/p391/maribhez/comprobacionInstalacionCorrecta_zpsdh2jeky5.png "Comprobación de instalación correcta.")

Ahora, después de la instalación del entorno virtual hay que pasar a instalar los lenguajes. Es necesario un paso previo, por supuesto, pues hay que comprobar cuáles son las versiones existentes para saber cuál es la última y proceder a su instalar. Así, ejecutamos el comando **nvm ls-remote**, y vemos que las versiones que vamos a instalar son *"v0.11.16"* y *v4.6.1* con **nvm install version**, siendo *version* la escogida por el usuario.

Después de documentarme para la realización de este ejercicio he visto que añadiendo la opción *-s* a nuestro comando permitimos la personalización posterior de la compilación de nuestro código, siendo por eso por lo que esta opción aparece sólo en una de las instalaciones.

Después de la segunda instalación se quedará esta versión marcada como *versión por defecto*, pero basta ejecutar **"nvm use version"** para marcar *version* como principal.



![Instalación versión v0.11.16](http://i345.photobucket.com/albums/p391/maribhez/instalacion_version0_zpsubmjtrul.png "Instalación versión v0.11.6.")


![Instalación versión v41.6.1](http://i345.photobucket.com/albums/p391/maribhez/instalacionVersion4_zps4lzfdd5m.png "Instalación versión v41.6.1.")


Por supuesto, la instalación de la segunda versión ha tardado bastante más.

###Ejericicio 2.

**Crear una web para calificar las empresas en las que hacen prácticas los alumnos.**

Se ha creado una aplicación básica donde poder crear empresas (añadiendo calificación) y donde poder listar las empresas y calificarlas.



Para crear la empresa se presenta el siguiente formulario:

![Creación empresa](http://i345.photobucket.com/albums/p391/maribhez/creadaEmpresaConCalificacion_zps0kabayhb.png "Creación empresa con respectiva calificación. " )

![Calificar empresa](http://i345.photobucket.com/albums/p391/maribhez/anadeCalificacion_zpsirdqewlr.png "Calificar empresa.")


###Ejercicio 3.

**Ejecutar el programa en diferentes versiones del lenguaje. ¿Funciona en todas ellas?** 

He llevado a cabo la aplicación programando en *Python y usando el framework *Flask*. Además, para almacenar la información he usado *shelve*,  Tal y como se puede ver en las capturas, para pasar del la versión 2.7 a la versión 3 sería necesario cambiar varios aspectos de los implementados para la práctica, pues todo lo que he usado para conseguir su funcionamiento no dispone del mismo soporte en ambas versiones.

![Ejecución en distintas versiones](http://i345.photobucket.com/albums/p391/maribhez/Captura%20de%20pantalla%20de%202016-11-16%2023-59-28_zpsbbu9gglx.png "Ejecución en diferentes versiones de Python")



###Ejercicio 4.

**Crear una descripción del módulo usando **package.json**. En caso de que se trate de otro lenguaje, usar el método correspondiente.**

El comando que he tenido que ejecutar para crear una descripción del módulo ha sido: *pip freeze > nombre.txt*.

Tal y como se muestra en la siguiente captura, de esta forma cuáles son las dependencias, aportando tanto el nombre como la versión necesaria. Si luego deseamos instalar todos de una vez sólo hay que usar el comando *pip install -r nombre.txt*, siendo nombre.txt el nombre que le habíamos dado al fichero creado en el comando anterior.

![Dependencias Python](http://i345.photobucket.com/albums/p391/maribhez/Captura%20de%20pantalla%20de%202016-11-16%2023-51-03_zpsyr4wguzy.png "Dependencias.")


###Ejercicio 5.


Automatizar con grunt, gulp u otra herramienta de gestión de tareas en Node la generación de documentación de la libreeria que se cree usando docco u otro sistema similar de generación de documentación. Previamente, por supuesto, habrá que documentar tal librería.

Para generar la documentación he usado *Sphinx*, herramienta de Python para tal efecto.


![Instalacion](http://i345.photobucket.com/albums/p391/maribhez/instalacion_zps51rgivqc.png "Instalación Sphinx.")

Después de instalar el segundo paso será crear las carpetas correspondientes y necesarias para la documentación con el comando *sphinx-quickstart*.

![Quickstart_1](http://i345.photobucket.com/albums/p391/maribhez/quickstart1_zpsntzvd20v.png "Quickstart")

![Quickstart_2](http://i345.photobucket.com/albums/p391/maribhez/quickstart2_zpsmilsumcy.png "Quickstart")

Ahora, como último paso, se genera la documentación html introduciendo nada más que *make html*.

![Make html](http://i345.photobucket.com/albums/p391/maribhez/makeHTML_zpsd2fvoi63.png "Make html")


Ahora, después de esto ya podemos ver nuestra documentación en *build/html*, a falta de incluir la información de nuestra aplicacíón que creamos conveniente .

![Documentacion](http://i345.photobucket.com/albums/p391/maribhez/documentacionFinal_zps9ncmnr39.png "Documentacion")


###Ejercicio 6.


**Para la aplicación que se está haciendo, escribir una serie de aserciones y probar qu efectivamente no fallan. Añadir tests para una nueva funcionalidad, probar que falla y escribir el código para que no lo haga (vamos, lo que viene siendo un TDD).**

El test que he llevado a cabo ha sido algo básico de probar a insertar una empresa con su correspondiente calificación en la base de datos usada, ya que esa es una de las funcionalidades implementadas que engloba lo principal de la dicha aplicación.


Aquí muestro la terminal comprobando que dicho test funciona, mientras que el código aparecerá almacenado en el repositorio de dicha aplicación. 

![Test](http://i345.photobucket.com/albums/p391/maribhez/testCrearEmpresa_zpsf30l0dsm.png "Test Python")


###Ejericicio 7.


**Convertir los tests unitarios anteriores con assert a programas de test y ejecutarlos desde mocha, usando descriptores de test y del grupo de test de forma correcta. Si hasta ahora no has subido el código que has venido realizando a GitHub, es el momento de hacerlo, porque lo vas a necesitar un poco más adelante.**

Esto es algo que ya había llevado a cabo en el ejericicio anterior, pues lo que realicé fue pensando en llevar a cabo su ejecución mediante librerías y aplicaciones de test creadas para tal efecto.El ejericico 6 lo basé en *pytest*, pero existen otros, como por ejemplo el conocido como *nose*.

###Ejercicio 8. 

**Haced los dos primeros pasos antes de pasar al tercero.**

El primer paso es, por supuesto, registrarnos e iniciar sesión con la cuenta de GitHub. 

![Registro](http://i345.photobucket.com/albums/p391/maribhez/Registro-1_zpsm1kl8xqh.png "Registro en Travis CI")

Después, y tras dejar que Travis genere la configuración inicial hemos de seleccionar que el repositorio que queremos añadir es el repositorio correspondiente al proyecto que llevamos desarrollando durante todos estos ejercicios. 
![Seleccion](http://i345.photobucket.com/albums/p391/maribhez/seleccionTravis_zpsg1hobrsy.png "Seleccion Repositorio")


Por último, el archivo de configuración; archivo que Travis ejecutará para comprobar si los tests terminan de forma correcta o no, de la misma forma que en los anteriores ejercicios lo comprobábamos manualmente ejecutando desde la terminal.






















