# Sistema de información de inventario y registro de incidentes


## Planteamiento del problema

El proceso de inventario de equipos de cómputo se realiza, llenando de manera manual unos formatos impresos que posteriormente es recopilada en un archivo físico y digital (Excel) de todos los equipos con las que cuenta la Universidad, no se puede garantizar que dicho archivo Excel brinde los datos suficientes y necesarios para conocer el estado de estos equipos.
No hay registro adecuado de los componentes de un gabinete como el responsable, la ubicación, número de serie etc. ademas se necesita registrar eventos que sucedan con estos, como un desperfecto, reparacion o mantenimiento.


## Objetivos
Se pretende desarrollar un sistema de Control de Inventario de bienes de los cuales es responsable la OTI (Gabinetes y componentes internos como switch...), centrada en solucionar y mitigar la mayor cantidad de amenazas como perdida, imperfecto en las que pueda estar incurriendo los componentes internos del gabinete en la Universidad Nacional del Altiplano en su control de inventario, permitiendo lograr un alto nivel de satisfacción, integridad de la información y mejorar considerablemente en el tiempo de generar los reportes de manera oportuna y precisa.
El sistema sera una aplicacion web.

Además de llevar un seguimiento del funcionamiento de estos equipos. Registrar enventos como mantenimiento, reparacion, etc.



---
## Alcance. 

Para este proyecto solo se tendrá en cuenta los gabinetes y aquellos equipos que contenga este, como un switch, …



## Metodología y materiales Herramientas
Programación extrema XP y Scrum, según el texto “Scrum y xp desde las Trincheras” de XP se tomara la programación en pares, para el backend y frontend, 2 para cada uno.

estas dos metodologías se pueden usar en conjunto tomando algunas premisas de cada una, ambos son metodologías agiles e iterativas.

Para la parte del diseño de … la interfaz se utilizaran las métricas de Material Design( son guias de diseño que ayudaran a que el web site se vea bien), utilizando los colores del logo del la OTI azul y celeste

![Paleta de colores](img/palette.png)

Para mejorar la parte del desarrollo por el lado del BackEnd se utilizara Python con flask y por el lado del FrontEnd Vue.js con vuetify, vue router, 
Herramientas 
Webstorn IDE para desarrollo web con vue
PyCharn IDE para Python
O se puede utilizar el IDE Visual Studio 



En el backend se utilizara un ORM, 
en python hay varios, 4-5 ORMs
peewee, Pony ORM, SQLAlchemy, y SQLObject ademas esta el ORM de Django, pero este esta estrechamente ligado al framework Django, y tratar de desacoplarlo y hacer algunos hacks para integrarlo con flask puede tomar algo de tiempo, el ORM facilatara el mapear los objetos de la aplicacion en la base de datos MySql.

Para este caso se utilizara peewee,porque al parecer es un orm estable, tiene soporte para MYSQL(https://www.youtube.com/watch?v=vy3xUB5nCbo)



El backEnd, Python con flask ide Pycharn

El frontEnd, Node JS con Vuejs ide WebStorn

Con el sistema de control de versiones git, usando su plataforma web GitHub.


### Bibliotecas para Flask

Por supuesto, hay muchas y muy buenas. Las siguientes son las más detacables.

flask-restful: Sencilla forma de realizar un API Rest.

flask-restplus: Ampliación del anterior. Entre otras herramientas, tiene un generador de documentación.

flask-restless: Preparado para trabajar con SQLalchemy.



ITIL…se tomara en cuenta la parte de ….



#### Tipo de sistema 
Sistemas de automatización de oficinas y sistemas de trabajo de conocimiento
Sistemas de información administrativa
Sistemas de soporte de decisiones 
Sistemas de soporte para ejecutivos



## Requerimientos



#### TODO
Tomar requerimientos.... 
* Registro de equipos de red(inventariado)
* Registro de incidencias de los equipos de red
* Reporte… del estado de los equipos ,,,,(mostrar datos estadísticos de los sucesos con los equipos)


### Casos de Uso( diagrama)



* Funcionales. -Cosas que se pueden hacer con el sistema
    * Registrar ...
* No funcionales. -Características y/o restricciones en la implementación o estándares de calidad




#### TODO
Actores

---

#### Nombre del caso de uso: Login 

* Actor(es): Jefe o personal

* Descripción: El personal de la OTI del area de redes o el jefe de la OTI, ingresa su usuario y contraseña para acceder al sistema.

* Flujo principal:
    1. El usuario entra al home de la aplicacion web.
    2. Clickea el boton de Login.
    3. aplicacion web muestra el formulario de login.
    4. *Selecciona el tipo de usuario Jefe , trabajador(revisar)*
    5. El usuario ingresa su usuario y pass.
    6. El sistema verifica sus credenciales.
    7. Si sus credenciales son correctas, dependiendo del tipo de cuenta se le dara acceso al sistema.

* Flujo alternativo:
    Flujo alternativo para el punto 6, en caso sus credenciales sean incorrectas.

    1. El formulario mostrara un msg de error de credenciales.
    2. El formulario volvera a pedir su user y pass
    3. Continua con el paso 6
    

* Precondicion: El usuario(jefe o personal) debe tener una cuenta.

* Post condicion:
El usuario logeado, puede acceder a los datos del sistema de acuerdo a sus permisos si es jefe o personal.


---


Caso de uso: 
Admin de usuarios

    En el sistema los jefes podran, crear credenciales para el personal.



### Referencias

    Packt Publishing
    Flask By Example


    O’Reilly Media
    Flask web development

    O’Reilly Media
    Python Cookbook

    HTTPS

    Flask doc
    VueJs doc
    Vuetify doc


    Login
    https://vuetifyjs.com/en/examples/layouts/centered

    Site
    https://vuetifyjs.com/en/examples/layouts/googleContacts


    Example layouts
    https://vuetifyjs.com/en/framework/pre-made-layouts



## Diagramas


## Doc


Se utilizara el azul por ser los colores representativos de la OTI que estan en el logo. 

Para el backend se creara una api rest, esto permitira a la aplicacion ser escalable, de forma que si posteriormente se quiere crear una aplicacion mobil o desktop solo tendra que consulta a la API REST, asi podra comunicarse con otros sistemas que necesiten los datos de este sistema.


Con esos datos en formato json,(datos )  se puede leer esos datos y crear un vista HTML, crear una app android, un UI para IOS.


REFERENCIA from
programador web valencia

## Diseño de la API Rest

### Tabla de rutas para realizar un API Rest
---
#### Ruta	Método	Funcionalidad

* /signup	                    POST	Registro
* /auth/login	                POST	Inicio de sesión
* /auth/logout	            GET	Cerrar sesión

---
* /equipos                            Lista los equipos.
* /equipos/equipo_001                 Obtiene detalles del equipo.
* /equipos/equipo_001/incidentes      Obtieene la lista de incidentes con el equipo.

---
* /equipo	                GET	Lista todas las equipos
* /equipo	                POST	Crea una nueva equipo
* /equipo/45	            GET	Obtiene la equipo
* /equipo/45	            PUT	Actualiza la equipo
* /equipo/45	            DELETE	Borra la equipo
* /equipo/45/libros	    GET	Lista todos los libros de la equipo
* /equipo/45/libros/21	GET	Obtiene el libro de la equipo
* /equipo/45/libros/21	PUT	Actualiza el libro de la equipo
* /equipo/45/libros/21	DELETE	Borra el libro de la equipo

---




## TODO
---
Una campanita de notificaciones, la indicara la cantidad de equipos en estado malo.


Realizar un diagrama de despliege ... o del funcionamiento del programa.


Diagrama de Servicio rest


diagrama de consumo de ApiRest con VueJs u otro framework Web



gabiente

telefonos

antenas


marca de equipo
descripcion del equipo

tipo de gabiente
des del gabinete


swith
descripcion

PDU alimentador de gabiente
tipos
desc
cantidad de tomos




Adaptador analogico
tipo marca
desc
estado


patch panel
tipo marca
desc
estado
cantidad de tomos
puertos
numero de serie


marcas 


---
mantemineto
reparacion
dar de baja



Omitir
ordenador de cable

encargado 

lo que contenga cada gabinete


---


caso de uso

DB

interfaz

lista de responsables

historial de personas por las que paso el equipo


historial incidentes con los equipos

quien registro
como lo soluciono



---

EL uso que se le dara al software…
Como se va a usar, donde(lugar), en que situaciones



Conocer la infraestructura donde se va a desplegar




#### Otros Diagramas
* Diagrama de secuencia, clases, despliegue, ER…
* Cronograma de actividades (diagrama de gant)
* Mockup del sitio web …
* Costos… se omite



#### Etapas
* Análisis
* Diseño
* Planificacion
* Implementaion
* Despliege
* Mantenimiento
