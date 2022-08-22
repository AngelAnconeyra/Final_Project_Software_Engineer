# Estilos de Programacion usados

## Code Golf
Un estilo de programacion Code Golf se utiliza en los archivos de la carpeta backend/blueprints de la aplicacion ya que cuentan con metodos de pocas lineas, que dependiendo de la complejidad de la peticion JSON a la API pueden ser mas largas.

## Pipeline
Este estilo con programacion orientado a objetos es usado en las clases de backend/models ya que estas clases contienen funciones que retornan datos que no son compartidos entre otras funciones de la misma clase.

## Persistent Tables
Los archivos de repositorio de la parte de infraestructura utilizan el estilo de programacion de persistent tables ya que al establecer una conexion directa con la base de datos asociada, cuentan con lineas de queries para la extraccion y modificacion de la Base de Datos.

## Indentacion Consistente
La indentacion es constante en los archivos .py (Y de todas maneras el lenguaje obliga a tenerla) con indentaciones de 4 espacios blancos, representada normalmente con la tecla Tab del teclado

## Sistema Consistente de Nombramiento
Se utiliza un sistema consistente de nombramiento para las variables, en la que varias variables temporales se vuelven a usar para representar una misma logica. El codigo usado con python se viene desarrollando con snake_casing, este estilo  nombra a las variables siempre en minuscula y si se quieren representar espacios o separacion de palabras se utiliza un guin bajo _, solo existe la excepcion para las clases donde cada clase se escriba empezando por una mayuscula y si existe separacion de palabras se hace con una mayuscula.

## Organizacion de Archivos y Carpetas
Los archivos de la aplicacion estan organizados en las carpetas backend y frontend, en backend ira la parte relevante para la API y la conexion a la base de datos como la infraestructura, los modelos y blueprints o rutas de la aplicacion, el frontend contara con las plantillas que serviran para representar datos dinamicos obtenidos de la API, ademas se encuentran tambien los archivos estaticos (imagenes, codigo css o js)

# Longitud de lineas limitada
Al ser las lineas horizontales largas una mala practica se ha optado por hacer algunas reducciones de lineas, como por ejemplo guardando informacion en variables temporales, y si no es posible aun asi de reducirlas, de la forma como se ve en la siguiente imagen.

