# Ejercicio 8 sobre Metodologías de Desarrollo en Cascada

 ## 1. Análisis de requerimientos

  ### Ejercicio 1

   #### Requisitos Funcionales:

   - *Registro de Productos:* Permitir a los usuarios agregar nuevos productos al inventario, incluyendo información como nombre, descripción, categoría, cantidad en stock, precio, etc.

   - *Actualizacion de prodcutos:* Posibilitar la modificación de la información de los productos existentes, como el cambio de precio, cantidad en stock, descripción, etc.

   - *Gestión de inventarios:* Permitir a los usuarios visualizar el inventario actualizado en tiempo real, así como realizar acciones como añadir, eliminar o modificar productos.

   - *Registro de Entradas y Salidas:* Registrar las entradas y salidas de productos del inventario, indicando la cantidad y la razón de la transacción (venta, compra, devolución, etc.).

   - *Control de Stock:* Mantener un seguimiento preciso del stock disponible, mostrando alertas cuando los niveles de stock están bajos o cuando se agotan ciertos productos.

   - *Generación de Reportes:* Permitir la generación de informes y estadísticas sobre el inventario, como el historial de ventas, los productos más vendidos, el inventario actual, etc.

   - *Gestión de Usuarios:* Administrar diferentes roles de usuario (administrador, empleado, etc.) con diferentes niveles de acceso y privilegios dentro del sistema.

   - *Seguridad:* Garantizar la seguridad de los datos del inventario y la autenticación de usuarios mediante la implementación de medidas como el cifrado de datos, el acceso mediante contraseñas seguras, etc.

   #### Requisitos no Funcionales:

   - *Rendimiento:* La aplicación debe ser capaz de manejar un gran volumen de productos y transacciones sin experimentar retrasos significativos en la respuesta.

   - *Usabilidad:* Usabilidad: La interfaz de usuario debe ser intuitiva y fácil de usar, con un diseño limpio y organizado que permita a los usuarios realizar tareas sin dificultad.

   - *Escalabilidad:* El sistema debe ser escalable para poder crecer con el negocio, soportando un aumento en el número de usuarios y productos sin comprometer su rendimiento.

   - *Disponibilidad:* La aplicación debe estar disponible las 24 horas del día, los 7 días de la semana, con un tiempo de inactividad mínimo para mantenimiento programado.

   - *Mantenibilidad:* El código debe estar bien estructurado y documentado para facilitar futuras actualizaciones y modificaciones en el sistema.

   - *Confiabilidad:* La aplicación debe ser confiable y estable, minimizando la posibilidad de errores y fallos del sistema que puedan afectar la integridad de los datos del inventario.

  ### Ejercicio 2

   #### Caso de Uso: Agregar un nuevo Prodcuto

   - **Actor Principal:** Usuario (Administrador,Empleado)
   - **Precondiciones:** El usuario ha iniciado sesión en el sistema,
                         El usuario tiene los permisos necesarios para agregar un producto al inventario
   - **Flujo Básico:** 1. El usuario accede a la sección de gestión de inventario en la aplicación.
                       2. El usuario selecciona la opción de "Agregar Nuevo Producto".
                       3. El sistema muestra un formulario vacío para ingresar los detalles del nuevo producto.
                       4. El usuario completa los campos obligatorios del formulario, como nombre, categoría, cantidad en stock y precio.
                       5. El usuario opcionalmente puede añadir información adicional, como descripción, código de barras, etc.
                       6. El usuario confirma la información ingresada y selecciona la opción de "Guardar".
                       7. El sistema valida los datos ingresados por el usuario.
                       8. Si los datos son válidos, el sistema registra el nuevo producto en el inventario y muestra un mensaje de éxito.
                       9. El usuario puede optar por agregar otro producto o regresar al menú principal.
   - **Flujo Alternativo:** 7a. Si algún dato obligatorio no ha sido ingresado o no es válido, el sistema muestra un mensaje de error indicando los campos que requieren atención.
                            7b. El usuario corrige los errores y vuelve a intentar guardar el producto.
   - **Postcondiciones:** El nuevo producto se añade al inventario y está disponible para su visualización y gestión por parte del usuario.
                          El usuario puede realizar acciones adicionales sobre el nuevo producto, como editar sus detalles o gestionar su stock.

 ## 2. Diseño del Sistema

  ### Ejercicio 3

   **Diagrama de flujo de datos**
+----------------------------------+
|           Usuario                |
|    (Administrador, Empleado)     |
+--------------+-------------------+
               |
               v
+--------------|-------------------+
|      Interfaz de Usuario         |
|   (Página web de gestión de      |
|         inventario)              |
+--------------|-------------------+
               |
               v
+--------------|-------------------+
|   Controlador de la Aplicación   |
|    (Back-end de la aplicación)   |
+--------------|-------------------+
               |
               v
+--------------|-------------------+
|        Base de Datos             |
|    (Almacena la información      |
|         del inventario)          |
+----------------------------------+

  ### Ejercicio 4

   **Figma:** https://www.figma.com/file/5jVStYTBpjBIGie3VibLLi/Untitled?type=design&node-id=0%3A1&mode=design&t=FqmWTsGOWbICJn9W-1

 ## 3. Diseño del Programa

  ### Ejercicio 5

   **Arquitectura del sistema**

   Para la aplicación web de gestión de inventario, una arquitectura adecuada sería la arquitectura de tres capas, que consta de la capa de presentación, la capa de lógica de negocio y la capa de acceso a datos.

   Elijo esta opcion ya que la arquitectura de tres capas proporciona una estructura sólida y flexible para la aplicación web de gestión de inventario, que permite una fácil mantenibilidad, escalabilidad, reutilización de componentes y testeabilidad del sistema.

  ### Ejercicio 6

   **Base de Datos**

    Tabla: Usuarios
     user_id (Clave primaria)
     username
     password
     role_id (Clave foránea referenciando la tabla Roles)

    Tabla: Roles
     role_id (Clave primaria)
     role_name (nombre del rol)
     Tabla: Productos
     product_id (Clave primaria)
     nombre
     descripcion
     categoria_id (Clave foránea referenciando la tabla Categorias)
     cantidad_en_stock
     precio
     codigo_de_barras

    Tabla: Categorias
     categoria_id (Clave primaria)
     nombre
     Tabla: Transacciones
     transaction_id (Clave primaria)
     product_id (Clave foránea referenciando la tabla Productos)
     user_id (Clave foránea referenciando la tabla Usuarios)
     tipo (entrada o salida)
     cantidad
     fecha
     motivo
    
    Tabla: Compras
     compra_id (Clave primaria)
     user_id (Clave foránea referenciando la tabla Usuarios)
     fecha
     total
    
    Tabla: Detalle_Compra
     detalle_compra_id (Clave primaria)
     compra_id (Clave foránea referenciando la tabla Compras)
     product_id (Clave foránea referenciando la tabla Productos)
     cantidad
     precio_unitario
    
    Tabla: Ventas
     venta_id (Clave primaria)
     user_id (Clave foránea referenciando la tabla Usuarios)
     fecha
     total
    
    Tabla: Detalle_Venta
     detalle_venta_id (Clave primaria)
     venta_id (Clave foránea referenciando la tabla Ventas)
     product_id (Clave foránea referenciando la tabla Productos)
     cantidad
     precio_unitario

 ## 4. Diseño

  ### Ejercicio 7

   ***Diagrama de Dominio:***

   #### Entidades:
   - **Usuario**
    - Atributos: user_id, username, password, role_id
   - **Producto**
    - Atributos: product_id, nombre, descripcion, categoria_id, cantidad_en_stock, precio, codigo_de_barras
  - **Categoria**
    - Atributos: categoria_id, nombre

   ### Relaciones:
   - Un Usuario puede agregar muchos Productos.
   - Un Producto pertenece a una sola Categoria.

   ***Diagrama de Clases:***

   ### Clases:
    - **Usuario**
     - Atributos: user_id, username, password, role_id
    - Métodos: 
     - validar_credenciales()
     - agregar_producto()

    - **Producto**
     - Atributos: product_id, nombre, descripcion, categoria_id, cantidad_en_stock, precio, codigo_de_barras
    - Métodos: 
     - validar_datos()
     - guardar_en_base_de_datos()

    - **Categoria**
     - Atributos: categoria_id, nombre
    - Métodos: 
     - obtener_productos_relacionados()

 ## 4. Diseño

  ### Ejercicio 9

  1. **Prueba de Validación de Datos:**
    - Verificar que se muestre un mensaje de error si se intenta agregar un producto con un precio negativo.
    - Verificar que se muestre un mensaje de error si se intenta agregar un producto sin un nombre.

  2. **Prueba de Guardado en la Base de Datos:**
    - Verificar que el producto se guarde correctamente en la base de datos cuando se ingresan datos válidos.
    - Verificar que se incremente el número de productos en el inventario después de agregar un nuevo producto.

  3. **Prueba de Duplicados:**
    - Verificar que se muestre un mensaje de error si se intenta agregar un producto con un nombre que ya existe en el inventario.

  4. **Prueba de Categoría:**
    - Verificar que el producto se asocie correctamente con la categoría seleccionada al agregarlo.

  ### Ejercicio 10: Pruebas de Integración para "Agregar un nuevo producto"

  1. **Prueba de Interfaz de Usuario:**
    - Verificar que la interfaz de usuario permita al usuario ingresar los detalles del nuevo producto de manera correcta.
    - Verificar que se muestren mensajes de error adecuados en caso de datos inválidos.

  2. **Prueba de Lógica de Negocio:**
    - Verificar que la lógica de negocio valide correctamente los datos ingresados por el usuario antes de guardar el producto en la base de datos.
    - Verificar que se manejen adecuadamente los casos de duplicados y otros errores de validación.

  3. **Prueba de Base de Datos:**
    - Verificar que el producto se guarde correctamente en la base de datos con todos los atributos correctamente almacenados.
    - Verificar que se actualice correctamente el inventario después de agregar un nuevo producto.

  ### 7. Mantenimiento:

  #### Ejercicio 13: Plan de Mantenimiento para la Aplicación Web

    1. **Monitoreo Continuo:**
      - Implementar herramientas de monitoreo para supervisar el rendimiento, la disponibilidad y la seguridad de la aplicación de manera continua.

    2. **Actualizaciones de Software:**
      - Programar actualizaciones regulares del software, incluyendo parches de seguridad, correcciones de errores y nuevas características.

    3. **Respaldo de Datos:**
      - Establecer un sistema de respaldo automático de datos para garantizar la integridad y disponibilidad de la información crítica.

    4. **Mantenimiento Preventivo:**
      - Realizar mantenimiento preventivo regularmente, como la limpieza de la base de datos, la optimización del código y la revisión de la seguridad.

    5. **Gestión de Incidentes:**
      - Desarrollar un plan de acción para responder rápidamente a incidentes de seguridad, errores críticos y tiempos de inactividad no planificados.

    #### Ejercicio 14: Implementación de Corrección de Errores

    1. **Identificación del Problema:**
      - Analizar el problema detectado en la aplicación, ya sea a través de informes de errores de los usuarios o del monitoreo del sistema.

    2. **Reproducción del Problema:**
      - Reproducir el problema en un entorno de desarrollo para comprender su causa raíz y determinar la mejor solución.

    3. **Desarrollo de la Solución:**
      - Implementar la corrección de errores utilizando prácticas de desarrollo seguro y probado.

    4. **Pruebas de Calidad:**
      - Realizar pruebas exhaustivas para garantizar que la corrección de errores no cause efectos secundarios no deseados y que resuelva el problema original de manera efectiva.

    5. **Despliegue de la Corrección:**
      - Implementar la corrección de errores en el entorno de producción de manera controlada y planificada, minimizando el impacto en los usuarios.

  ### 8. Preparándonos para Nuevos Retos:

   #### Ejercicio 15: Equipo de Trabajo y Roles para IA Generativa

    1. **Equipo de Trabajo:**
      - Científico de Datos: Responsable de investigar y aplicar técnicas de IA generativa para la creación de modelos.
      - Ingeniero de Software: Encargado de desarrollar e implementar sistemas informáticos para entrenar y desplegar modelos de IA generativa.
      - Diseñador UX/UI: Diseña la interfaz de usuario para interactuar con las aplicaciones basadas en IA generativa, asegurando una experiencia de usuario intuitiva y atractiva.
      - Especialista en DevOps: Gestiona la infraestructura y el despliegue de las aplicaciones, así como la automatización de procesos de desarrollo y despliegue.
      - Gerente de Proyecto: Supervisa la planificación, coordinación y ejecución del proyecto, asegurando que se alcancen los objetivos en tiempo y forma.

    2. **Roles:**
      - Investigación y Desarrollo: Científico de Datos, Ingeniero de Software.
      - Diseño y Experiencia de Usuario: Diseñador UX/UI.
      - Implementación y Despliegue: Ingeniero de Software, Especialista en DevOps.
      - Gestión y Coordinación: Gerente de Proyecto.