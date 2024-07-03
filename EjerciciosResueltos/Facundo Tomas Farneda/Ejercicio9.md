# Ejercicio 9 | Práctica

## Análisis de Requerimientos

### Ejercicio 1

- Requerimientos funcionales

1. La aplicación web tiene que ver cuantas existencias hay en el inventario
2. La aplicación web tiene que ser capaz de agregar productos
3. La aplicación web tiene que ser capaz de remover productos
4. La aplicacion web tiene que ser capaz de modificar productos
5. La aplicación web tiene que aceptar productos que no contengan productos más de 60 palabras.

- Requerimientos no funcionales

1. La aplicación web no tiene que tardar en cargar cualquier lista más de 5 milisegundos
2. La aplicacion web tiene que resistir la vulnerabilidad de SQL Inyection
3. La interfaz de la aplicacion web tiene que ser amigable para el usuario

### Ejercicio 2

Titulo: Agregar un nuevo producto

![Caso de uso](./imgs/CUD.png)

## Diseño del Sistema

### Ejercicio 3

![Diagrama de flujo](./imgs/FlowChart.png)

### Ejercicio4

![interfaz](./imgs/Interfaz.png)

## Diseño del Programa

### Ejercicio 5

La arquitectura que me parece adecuada para la aplicación web es la
modelo-vista-controladora (MVC), ya que delimita de forma eficiente los
componentes que contendrá la aplicación.

### Ejercicio 6

![DataBase](./imgs/DataBase.png)

## Diseño

### Diagrama de Dominio

![DiagramaDominio](./imgs/DiagramaDominio.png)

### Diagrama de Robustez

![DiagramaRobustez](./imgs/DiagramaRobustez.png)

### Prototipo

#### Inicio

![Prototipo(Inicio)](./imgs/PrototipoInicio.png)

#### Agregar Producto

![Prototipo(AgregarProducto)](./imgs/PrototipoAgregarProducto.png)

#### Resultado

![Prototipo(Resultado)](./imgs/PrototipoFinal.png)

### Diagrama de Secuencia

![DiagramaSecuencia](./imgs/DiagramaSecuencia.png)

### Diagrama de Clases

![DiagramaClases](./imgs/DiagramaClases.png)

### Ejercicio 7

La forma en la que implementaría la funcionalidad es con el lenguaje C# y Razor Pages, con estas herramientas haría una aplicación con el framework Blazor en Visual Studio Community 2022. Para guardar los datos utilizaría SQL Server.

Las funcionalidades se irán implementando a partir de iteraciones, que en este caso serán dos. Una donde el requerimiento para implementar sea "Agregar un nuevo producto" y la otra donde el requerimiento para implementar sea "Validar producto"

### Ejercicio 8

Habiendo elegido una arquitectura en capas implementaría la lógica de negocio en varias clases. Una que hace validaciones, otra que vincule la interfaz y la capa da acceso de datos.

## Pruebas

### Ejercicio 9

Prueba unitaria 1: Verificar que el producto se registre exitosamente en la base de datos.

Prueba unitaria 2: Verificar que el precio del producto no tenga un valor negativo.

### Ejercicio 10

Las siguientes pruebas integran los modulos de "Agregar un nuevo producto" y el de validaciones.

Prueba de integracion 1: Verificar que ningún campo se encuentre vacio y que se registre el producto en la base de datos correctamente.

Prueba de integracion 2: Verificar que el nombre del producto no supere el limite de 60 palabras y que se registre en la base de datos correctamente.

## Despliegue del Programa

### Ejercicio 11

La aplicacion web será instalada mediante un programa ".exe" en la carpeta  "Archivos de programa(x86)".

### Ejercicio 12

La aplicación será desplegada a un servidor de producción cuando se realicen los siguientes pasos.

1. El servidor debe estar preparado, es decir que sea capaz de acceder al mismo y que este actualizado.
2. Las configuraciones del entorno tienen que estar preparadas, es decir que tienen que estar listas todas las dependencias necesarias
3. Se tienen que realizar las configuraciones necesarias al servidor web.
4. Se tiene que enviar los archivos de la aplicación al servidor web.
5. Se tiene que configurar la base de datos, ya sea creandola, brindandole todos los permisos al usuario o importando datos
6. Se tienen que configurar las variables del entorno.
7. Se tiene que configurar la seguridad del servidor web.

## Mantenimiento

### Ejercicio 13

El plan de mantenimiento para la aplicación web será el siguiente:

1. Antes de que comience un nuevo mes reindexar todos los indices, para así asegurar una buena velocidad en la búsqueda de los datos cuando se necesiten.
2. Cada día se va a monitorear el estado del servidor.
3. Cada mitad de semana se va a realizar un respaldo de la base de datos

### Ejercicio 14

Se encontro un error en la aplicacion que consistia en que la aplicacion web aceptada caracteres especiales como "@" en el campo para introducir el nombre del producto.
