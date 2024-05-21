# Ejercicios sobre Metodologías de Desarrollo en Cascada

## Análisis de Requerimientos:

### Ejercicio 1
Un cliente te solicita una aplicación web para gestionar su inventario. Define los requisitos funcionales y no funcionales del sistema.


#### Requerimientos Funcionales:

- Gestión de Productos: La aplicación debe permitir al usuario agregar, editar, eliminar y visualizar productos.

- Gestión de Inventario: La aplicación debe permitir al usuario incrementar o disminuir la cantidad de un producto en el inventario.

- Búsqueda de Productos: La aplicación debe permitir al usuario buscar productos por su nombre o categoría.

- Reportes de Inventario: La aplicación debe generar reportes del estado actual del inventario.
---
#### Requerimientos No Funcionales:

- Usabilidad: La aplicación debe ser fácil de usar y tener una interfaz intuitiva.

- Rendimiento: La aplicación debe responder rápidamente a las solicitudes del usuario.

- Seguridad: La aplicación debe proteger la información del inventario y los datos del usuario.

- Disponibilidad: La aplicación debe estar disponible para el usuario en todo momento.

---

### Ejercicio 2
Redacta un caso de uso para la funcionalidad de "Agregar un nuevo producto" en la aplicación web del ejercicio 1.

![Caso de uso](/EjerciciosResueltos/Diaz_Agustin/imagenes/UseCaseDiagram.png)

|  |  Caso de uso   |Fehca: 20/5/24|
|--|---------------|-----|
|Código|CUD 01.1|
|Nombre|Agregar nuevo productos|
|Autor| Agustin Diaz|
|Revisor|Alejandro Sartorio|
|Versión |01|
|Estado |pendiente|
|Descripción |El actor agrega un producto.|
|Actores|Usuario|
|Pre-condicion|El actor debe tener habilitada al menos una acción sobre el formulario “Agregar productos”|
|CU-extensión|CUD 01|
|Puntos de extensión|
|Curso |
|1|El sistema verifica las acciones que puede realizar el actor en el formulario "Agregar productos", y muestra el formulario.|
|2 |El actor elige una lista de pedidos.|
|3 |El actor selecciona un producto.|
|4|El actor ingresa la cantidad que desee.|
|5|El actor hace click en el botón “Confirmar” |
|5.1|El sistema verifica que haya un producto seleccionado y si la cantidad ingresada es mayor a cero, si es así, procede a mandar un mail a los administradores informando sobre un nuevo pedido para finalizar cerrando el formulario.|
|5.2|En caso de que no haya un producto seleccionado o la cantidad sea 0, se le informará al usuario el error.|
|Curso alternativo|El actor hace click en el botón “Cancelar”.|
|2|El sistema mostrará una advertencia si el usuario está de acuerdo entonces el formulario se cerrará.|
|2.1|Si el usuario no está de acuerdo se cerrará la advertencia y no se cancelará el producto.|
|Post-condición|El usuario ha agregado un producto.|




## Diseño del Sistema:
### Ejercicio 3 
Elabora un diagrama de flujo de datos para la aplicación web del ejercicio 1.

![Flujo de datos](/EjerciciosResueltos/Diaz_Agustin/imagenes/FlowchartDiagram.jpg)


### Ejercicio 4 
Diseña la interfaz de usuario para la pantalla de "Inicio" de la aplicación web del ejercicio 1.

![Interfaz](/EjerciciosResueltos/Diaz_Agustin/imagenes/interfaz.jpeg)

## Diseño del Programa:
### Ejercicio 5
Elige una arquitectura adecuada para la aplicación web del ejercicio 1 y justifica tu elección.

La arquitectura elegida es la arquitectura de niveles, divide la aplicación en tres componentes principales:

- El nivel de Presentación sería la interfaz de usuario donde los usuarios pueden agregar, editar, eliminar y visualizar productos, así como incrementar o disminuir la cantidad de un producto en el inventario.

- El nivel de Lógica de Negocio manejaría las solicitudes del usuario, como agregar un nuevo producto o actualizar el inventario. Este nivel también aplicaría las reglas de negocio, como validar los datos del producto o verificar si hay suficiente stock antes de permitir una disminución en el inventario.

- El nivel de Datos sería la base de datos donde se almacenan los detalles del producto y la información del inventario.

Esta arquitectura la elijo ya que es utilizada debido a su flexibilidad, escalabilidad y separación de responsabilidades, lo que facilita el mantenimiento y la expansión de la aplicación pensando en el futuro.


### Ejercicio 6
Diseña la base de datos para la aplicación web del ejercicio 1.

![Base de datos](/EjerciciosResueltos/Diaz_Agustin/imagenes/DB.jpeg)

## Diseño:
Utilizando los siguientes diagrama resuelva los casos de usos de los  ejercicios 7 y 8: 
- Diagrama de Dominio: Identifica las entidades, atributos y relaciones del sistema.
- Diagrama de Robustez: Analiza cómo el sistema responde a diferentes escenarios de uso.
- Prototipo: Crea una versión simplificada del sistema para probar la usabilidad y funcionalidad.
- Diagrama de Secuencia: Describe la interacción entre los diferentes objetos del sistema.
- Diagrama de Clases: Define las clases, sus atributos, métodos y relaciones
	
### Ejercicio 7
Implementa la funcionalidad de "Agregar un nuevo producto" en la aplicación web del ejercicio 1 utilizando el lenguaje de programación de tu preferencia.

![Robustez](/EjerciciosResueltos/Diaz_Agustin/imagenes/Robustez.jpeg)

### Ejercicio 8
Implementa la lógica de negocio para la funcionalidad de "Agregar un nuevo producto" en la aplicación web del ejercicio 1.

![Sequence](/EjerciciosResueltos/Diaz_Agustin/imagenes/SequenceDiagram.jpg)

## 5. Pruebas:
### Ejercicio 9
Define un conjunto de pruebas unitarias para la funcionalidad de "Agregar un nuevo producto" en la aplicación web del ejercicio 1.

Pseudocódigo:

```
// Prueba unitaria 1: Verificar que un producto se puede agregar con datos válidos
function testAgregarProductoConDatosValidos() {
    producto = crearProducto("Producto 1", "Descripción del Producto 1", 10, "Categoría 1")
    resultado = agregarProducto(producto)
    assert(resultado == true)
}

// Prueba unitaria 2: Verificar que no se puede agregar un producto sin nombre
function testAgregarProductoSinNombre() {
    producto = crearProducto("", "Descripción del Producto 1", 10, "Categoría 1")
    resultado = agregarProducto(producto)
    assert(resultado == false)
}

// Prueba unitaria 3: Verificar que no se puede agregar un producto con cantidad negativa
function testAgregarProductoConCantidadNegativa() {
    producto = crearProducto("Producto 1", "Descripción del Producto 1", -10, "Categoría 1")
    resultado = agregarProducto(producto)
    assert(resultado == false)
}
```
### Ejercicio 10
 Ejecuta pruebas de integración para la funcionalidad de "Agregar un nuevo producto" en la aplicación web del ejercicio 1.

```
// Prueba de integración 1: Verificar que un producto se puede agregar y luego recuperar de la base de datos

function testAgregarYRecuperarProducto() {
    producto = crearProducto("Producto 1", "Descripción del Producto 1", 10, "Categoría 1")
    agregarProducto(producto)
    productoRecuperado = obtenerProducto("Producto 1")
    assert(productoRecuperado.nombre == "Producto 1")
    assert(productoRecuperado.descripcion == "Descripción del Producto 1")
    assert(productoRecuperado.cantidad == 10)
    assert(productoRecuperado.categoria == "Categoría 1")
}

// Prueba de integración 2: Verificar que un producto se puede agregar y luego aparece en la lista de productos

function testAgregarYListarProducto() {
    producto = crearProducto("Producto 1", "Descripción del Producto 1", 10, "Categoría 1")
    agregarProducto(producto)
    listaProductos = listarProductos()
    assert("Producto 1" in listaProductos)
}
```

## 6. Despliegue del Programa:
### Ejercicio 11

Definir un plan de despliegue para la aplicación web del ejercicio 1.

---
El plan de despliegue que yo implementaria para la aplicación web tiene los siguientes pasos:

1. Preparación del entorno de producción: Configurar el servidor de producción con el sistema operativo adecuado, las dependencias necesarias y la configuración de seguridad apropiada.

2. Configuración de la base de datos: Configura la base de datos en el servidor de producción. La creación de la base de datos, la configuración de las tablas y la configuración de los usuarios y permisos de la base de datos.

3. Despliegue del código de la aplicación: Transfiere el código de la aplicación al servidor de producción. Lo haria mediante un sistema de control de versiones como Git, o mediante la transferencia directa de archivos.

4. Configuración de la aplicación: Configura la aplicación en el servidor de producción. Configuración de las variables de entorno, la configuración del servidor web y la conexión con la base de datos.

5. Pruebas de la aplicación: Realizar pruebas en el servidor de producción para asegurar que la aplicación funciona correctamente. Incluye pruebas de funcionalidad, pruebas de rendimiento y pruebas de seguridad.

6. Monitoreo y mantenimiento: Una vez que la aplicación esté en funcionamiento, es importante monitorear su rendimiento y mantenerla actualizada con las últimas correcciones de seguridad y actualizaciones de funcionalidad.

### Ejercicio 12
Despliega la aplicación web del ejercicio 1 en un servidor de producción.

---
Para ejecutar el plan de despliegue, yo seguiria los pasos descritos en el plan:

1. Preparación del entorno de producción: Instalar el sistema operativo en el servidor de producción, configura las dependencias necesarias (como Node.js, Python, etc.) y establece las reglas de firewall y otras configuraciones de seguridad.

2. Configuración de la base de datos: Instalar el sistema de gestión de bases de datos (como MySQL, PostgreSQL, etc.) en el servidor de producción. Crear la base de datos y las tablas utilizando los scripts SQL que has definido durante el desarrollo. Configura los usuarios y permisos de la base de datos según sea necesario.

3. Despliegue del código de la aplicación: Clonar el repositorio de Git en el servidor de producción, o transferir los archivos de la aplicación al servidor mediante SCP o FTP. Asegurar de que todos los archivos estén en el lugar correcto y que los permisos de archivo sean los adecuados.

4. Configuración de la aplicación: Configurar las variables de entorno necesarias para la aplicación, como la cadena de conexión de la base de datos. Configurar el servidor web (como Nginx, Apache, etc.) para servir la aplicación.

5. Pruebas de la aplicación: Realizar pruebas en el servidor de producción para asegurarte de que todo funciona correctamente. Incluyendo la navegación por la aplicación, la realización de acciones como agregar un producto y la comprobación de la carga y el tiempo de respuesta de la aplicación.

6. Monitoreo y mantenimiento: Configurar herramientas de monitoreo para rastrear el rendimiento de la aplicación y recibir alertas si algo sale mal. Mantener la aplicación actualizada instalando regularmente las últimas actualizaciones de seguridad y funcionalidad.

## 7. Mantenimiento:
### Ejercicio 13
Definir un plan de mantenimiento para la aplicación web del ejercicio 1.

---
El plan de mantenimiento que usaria para la aplicación web de gestión de inventario tiene los siguientes pasos:

1. Monitoreo Continuo: Utilizar herramientas de monitoreo para rastrear el rendimiento de la aplicación y recibir alertas si algo sale mal.

2. Actualizaciones de Seguridad: Mantener la aplicación y todas sus dependencias actualizadas con las últimas correcciones de seguridad.

3. Pruebas Regulares: Realizar pruebas regulares para asegurar que todas las características de la aplicación funcionan como se espera.

4. Respaldo de Datos: Realizar respaldos regulares de la base de datos para prevenir la pérdida de datos.

5. Revisión de Código: Realizar revisiones de código regulares para mantener la calidad del código y prevenir la introducción de nuevos errores.

6. Mejora Continua: Basándote en el feedback de los usuarios y en tus propias observaciones, realizar mejoras continuas en la aplicación.

### Ejercicio 14
Implementa una corrección de errores para un problema detectado en la aplicación web del ejercicio 1.

---
A la hora de implementar una correción de errores estos serian los pasos:

1. Reproducir el Problema: Intentar reproducir el problema en tu entorno de desarrollo para entender qué está sucediendo.

2. Identificar la Causa: Una vez que reproduzcas el problema, examinar el código para identificar la causa. En este caso, podrías descubrir que el botón de “Guardar” no está vinculado correctamente al evento de envío del formulario.

3. Implementar la Corrección: Una vez que se identifica la causa, implementamos la corrección. En este caso, corregimos la vinculación del botón de “Guardar” al evento de envío del formulario.

4. Pruebas: Después de implementar la corrección, realizar pruebas para asegurar que el problema se ha resuelto y de que no se introdujo algun nuevo problema.

5. Despliegue: Una vez que se realizaron las pruebas exhaustivas, desplegar la corrección en el entorno de producción.

## 8. Nos preparamos para nuevos retos

### Ejercicio 15
Arme un equipo de trabajo y defina los roles para realizar los ejercicios anteriores para un futuro dominio de aplicación relacionado con inteligencia artificial generatica. 

---
- Gerente de Proyecto / Analista de Requerimientos: supervisará el proyecto, coordinará con los stakeholders, y se asegurará de que el equipo esté en el camino correcto para cumplir con los objetivos del proyecto. 

- Arquitecto de Software / Desarrollador de Backend: responsable de elegir la arquitectura adecuada para la aplicación, de diseñar la estructura general del sistema, y de implementar la lógica de negocio de la aplicación. 

- Desarrollador de Frontend: encargado de implementar la interfaz de usuario de la aplicación.

- Tester / Ingeniero de DevOps: responsable de crear y ejecutar pruebas para asegurarse de que la aplicación funcione correctamente. También se encargará del despliegue y mantenimiento de la aplicación en el servidor de producción.

- Experto en IA / Desarrollador de Base de Datos: responsable de integrar las funcionalidades de inteligencia artificial en la aplicación y de asegurarse de que funcionen correctamente. También se encargará de diseñar y mantener la base de datos de la aplicación.