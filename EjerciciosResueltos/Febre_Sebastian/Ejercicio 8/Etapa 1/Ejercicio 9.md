## 5. Pruebas:

### Ejercicio 9: 
Define un conjunto de pruebas unitarias para la funcionalidad de "Agregar un nuevo producto" en la aplicación web del ejercicio 1.


Un conjunto de pruebas unitarias proporcionan una forma de verificar la funcionalidad de "Agregar un nuevo producto" en la aplicación web, asegurando que los datos se envíen correctamente, se inserten en la base de datos de manera adecuada y que la base de datos se limpie adecuadamente después de la prueba:

##### 1. Prueba de envío exitoso de datos del formulario: 
Esta prueba verifica que los datos del formulario se envíen correctamente al servidor al intentar agregar un nuevo producto. Se asegura de que se reciban una respuesta HTTP 200 OK y que la solicitud se procese sin errores.

##### . Prueba de inserción en la base de datos: 
Después de enviar los datos del formulario, esta prueba verifica que el nuevo producto se haya insertado correctamente en la base de datos. Se realiza una consulta a la base de datos para recuperar el producto recién agregado y se verifican sus atributos para asegurarse de que coincidan con los datos enviados.

##### 3. Prueba de limpieza de la base de datos: 
Al final de la prueba, se asegura de limpiar la base de datos eliminando el producto agregado. Esto garantiza que la base de datos vuelva a su estado original después de la ejecución de la prueba y evita que los datos de prueba interfieran con otras pruebas.

