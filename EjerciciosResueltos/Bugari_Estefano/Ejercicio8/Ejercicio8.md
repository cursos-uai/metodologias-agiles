# 1 Análisis de Requerimientos
### Ejercicio 1
* Requerimientos funcionales: 
- Gestión de productos, dar de alta, editar y dar de baja un producto. 
- Búsqueda de productos, filtrar por nombre, categoría, precio, etc...
* Requerimientos no funcionales:
- El sistema debe poder manejar volúmes de datos grandes, ya sea por si se actualizan los precios de muchos productos a la vez o se ingresan muchos a la vez, o casos similares.
- Usabilidad, la interfaz del sistema debe ser sencilla e intuitiva.

### Ejercicio 2
* Redactar el caso de uso "agregar un nuevo producto".
- El usuario presiona en agregar un nuevo producto.
- El sistema Muestra un formulario con los datos a ingresar.
- El usuario completa los datos y presiona en confirmar.
- El sistema valida los datos.
- El sistema guarda los datos.

* Excepciones.
- El sistema detecta datos incorrectos en la validación e informa error.

# 2 Diseño del sistema
### Ejercicio 3
<image src="./DiagramaFlujo.png" alt="Diagrama de flujo">

### Ejercicio 4
<image src="./Login.png" alt="Login">

# 3 Diseño del programa
- Elijo la arquitectura MVC porque es las que más conozco y me parece adecuada para separar la lógica de la aplicación.

# 4 Diseño del programa
1. Modelo de dominio
<image src="./ModeloDominio.png" alt="Diagrama de modelo de dominio">

4. Diagrama de secuencia
<image src="./DiagramaSecuencia.png" alt="Diagrama de secuenca">

5. Diagrama de clases
<image src="./DiagramaClases.png" alt="Diagrama de clases">

# 5 Pruebas
### Ejercicio 9
1. Prueba de carga de página:
Verificar que al acceder a la página de agregar un nuevo producto, se recibe una respuesta exitosa del servidor (código de estado HTTP 200) y que la página contiene el título "Agregar un nuevo producto".
2. Prueba de agregar producto:
Simula el envío de un formulario con los datos de un nuevo producto (nombre, descripción, precio, cantidad y proveedor) y verifica que, después de enviar el formulario, se recibe una respuesta exitosa del servidor y que se muestra un mensaje indicando que el producto se agregó correctamente.
3. Prueba de campos requeridos:
Verifica que si se intenta enviar el formulario sin completar todos los campos requeridos (nombre, descripción, precio, cantidad), se recibe una respuesta del servidor indicando que estos campos son obligatorios.
4. Prueba de validación de precio y cantidad:
Verifica que si se intenta enviar el formulario con valores no numéricos en los campos de precio y cantidad, se recibe una respuesta del servidor indicando que se deben ingresar valores numéricos válidos.

# 6 Despliegue del programa
### Ejercicio 11
Preparación del Entorno de Producción:

Seleccionar un proveedor de servicios en la nube.
Configura un servidor web y una base de datos.
Configuración de la Aplicación:

Configurar las variables de entorno necesarias.
Configurar el servidor web para servir la aplicación.
Pruebas en el Entorno de Producción:

Realiza pruebas exhaustivas de funcionalidad, rendimiento y seguridad.
Despliegue:

Inicia la aplicación en el servidor.
Mantenimiento y Actualizaciones:

Implementar un proceso de gestión de cambios.
Establecer un plan de respaldo de datos.

# 7 Plan de mantenimiento
### Ejercicio 13
Actualizaciones de Seguridad y Parches:

Mantener actualizadas todas las bibliotecas y dependencias de la aplicación.
Respaldo y Recuperación de Datos:

Establecer un plan de respaldo regular y realizar pruebas de restauración.
Monitoreo del Rendimiento:

Supervisar el rendimiento de la aplicación y realizar ajustes según sea necesario.
Gestión de Errores:

Implementar un sistema de seguimiento de problemas para responder y abordar rápidamente los errores reportados.

Evaluación Continua:

Evaluar regularmente el rendimiento, la seguridad y la usabilidad de la aplicación.
Identificar y trabajar en mejoras continuas según sea necesario.