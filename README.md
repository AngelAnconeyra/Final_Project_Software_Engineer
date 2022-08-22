# Estilos de Programacion usados

## Code Golf
Un estilo de programacion Code Golf se utiliza en los archivos de la carpeta backend/blueprints de la aplicacion ya que cuentan con metodos de pocas lineas, que dependiendo de la complejidad de la peticion JSON a la API pueden ser mas largas.

![alt text](Imagenes/code_golf.PNG "Title")

Captura de pantalla del archivo backend/blueprints/evento_blueprint.py

## Pipeline
Este estilo con programacion orientado a objetos es usado en las clases de backend/models ya que estas clases contienen funciones que retornan datos que no son compartidos entre otras funciones de la misma clase.

![alt text](Imagenes/pipeline.PNG "Title")

Captura de pantalla del archivo backend/models/usuario.py

# Practicas de Codigo Legible
Algunas de las practicas de codigo legible utilizadas son:

## Comentarios y Documentacion
El codigo esta bien comentado y documentado en las partes importantes y en las que no se pueden sobreentender a simple vista. Ademas se ha evitado el uso de comentarios obvios e innecesarios.

![alt text](Imagenes/comentarios.PNG "Title")

Captura de pantalla del archivo backend/infrstructure/asistente_repository.py

## Indentacion Consistente
La indentacion es constante en los archivos .py (Y de todas maneras el lenguaje obliga a tenerla) con indentaciones de 4 espacios blancos, representada normalmente con la tecla Tab del teclado

![alt text](Imagenes/indentacion.PNG "Title")

Captura de pantalla del archivo backend/infrastructure/asistente_repository.py

## Organizacion de Archivos y Carpetas
Los archivos de la aplicacion estan organizados en las carpetas backend y frontend, en backend ira la parte relevante para la API y la conexion a la base de datos como la infraestructura, los modelos y blueprints o rutas de la aplicacion, el frontend contara con las plantillas que serviran para representar datos dinamicos obtenidos de la API, ademas se encuentran tambien los archivos estaticos (imagenes, codigo css o js)

![alt text](Imagenes/estructura.PNG "Title")

Captura de pantalla de organizacion de carpetas en VS Code

# Longitud de lineas limitada
Al ser las lineas horizontales largas una mala practica se ha optado por hacer algunas reducciones de lineas, como por ejemplo guardando informacion en variables temporales, y si no es posible aun asi de reducirlas, de la forma como se ve en la siguiente imagen.

![alt text](Imagenes/lineas.PNG "Title")

Captura de pantalla del archivo backend/infrastructure/ponente.py

# Principios SOLID

## Single Resposibilty (S)
Cada archivo y clase presenta solo una funcionalidad, no mezcladas con otras. Por ejemplo, los repositorios realizan las peticiones directas a la base de datos, los blueprints, retornan datos en formato json a la API, y las clases de modelos representan a las entidades.

Diferencia entre Evento para su repositorio, modelo y blueprint

![alt text](Imagenes/single_responsibility.PNG)

![alt text](Imagenes/single_responsibility2.PNG)

![alt text](Imagenes/single_responsibility3.PNG)

Capturas de pantalla de los archivos backend/models/evento.py, backend/infrastructure/evento_repository.py y backend/blueprints/evento_blueprint.py

## Open / Closed (O)
Al usar modelos como una representacion de las entidades en los archivos de backend, se pueden anadir funcionalidades sin tener que modificar la base de datos.

![alt text](Imagenes/openclosed.PNG)

Captura de pantalla del archivo backend/models/evento

## Dependency Inversion (D)
Si se realiza un cambio a una subclass, la clase superior no debe verse afectada por tal cambio, como podemos ver en las clases del modelo de Usuarios y Name, Usuario depende de Name, pero los cambios que se hagan a Usuario, no debera afectar el comportamiento de Name.

![alt text](Imagenes/dependencyinversion.PNG "Dependency Inversion")

Captura de pantalla del archivo backend/models/usuario.py
