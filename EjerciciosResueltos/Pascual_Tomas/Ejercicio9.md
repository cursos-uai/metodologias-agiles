# Ejercicio 8 sobre Metodologías de Desarrollo en Cascada con RUP

 ## 1. Análisis de requerimientos

  ### Ejercicio 1

   #### Requisitos Funcionales:

    1. El sistema debe permitir a los usuarios iniciar sesión con un nombre de usuario y contraseña.
    2. Los usuarios deben poder agregar, modificar y eliminar productos del inventario.
    3. Debe existir un sistema de categorías para organizar los productos.
    4. Los usuarios deben poder realizar búsquedas y filtrar productos por nombre, categoría, etc.
    5. El sistema debe registrar transacciones de entrada y salida de productos.
    6. Debe haber diferentes roles de usuario con diferentes niveles de acceso (por ejemplo, administrador y empleado).
    7. El sistema debe generar informes de inventario, ventas, etc.

   #### Requisitos No Funcionales:
    1. El sistema debe ser fácil de usar y tener una interfaz intuitiva.
    2. Debe ser seguro, con funciones de autenticación y autorización robustas.
    3. Debe ser escalable para manejar un gran volumen de productos y transacciones.
    4. Debe ser compatible con múltiples navegadores web y dispositivos.
    5. Debe tener tiempos de respuesta rápidos para garantizar una experiencia de usuario fluida.
    6. Debe cumplir con estándares de rendimiento para garantizar una respuesta rápida del sistema.
    7. Debe tener una buena documentación para facilitar el mantenimiento y la expansión del sistema.

  #### Ejercicio 2: Caso de Uso "Agregar un Nuevo Producto"

    **Nombre:** Agregar un Nuevo Producto

    **Actor Principal:** Usuario

    **Objetivo:** Permitir al usuario agregar un nuevo producto al inventario.

    **Precondiciones:**
    - El usuario ha iniciado sesión en el sistema.
    - El usuario tiene permisos para agregar productos.

    **Flujo Básico:**
    1. El usuario selecciona la opción "Agregar Producto" en la interfaz de usuario.
    2. El sistema muestra un formulario para ingresar los detalles del nuevo producto.
    3. El usuario completa los campos del formulario, incluyendo nombre, descripción, categoría, cantidad en stock, precio, y código de barras.
    4. El usuario confirma la entrada de datos.
    5. El sistema valida los datos ingresados por el usuario.
    6. Si los datos son válidos, el sistema guarda el nuevo producto en la base de datos y actualiza el inventario.
    7. El sistema muestra un mensaje de confirmación de que el producto se ha agregado correctamente.
    8. El caso de uso termina.

    **Flujos Alternativos:**
    - Si los datos ingresados por el usuario no son válidos (por ejemplo, falta el nombre del producto o el precio es negativo), el sistema muestra un mensaje de error y solicita al usuario que corrija los campos incorrectos.
    - Si el usuario cancela la operación, el caso de uso termina sin agregar un nuevo producto.

 ## 2. Diseño del Sistema

  ### Ejercicio 3

   **Diagrama de flujo de datos**
       +-------------------+              +-------------------+
       |    Interfaz de    |    Datos     |    Sistema de     |
       |    Usuario        +------------->|    Gestión de     |
       |                   |              |    Inventario     |
       +---------+---------+              +---------+---------+
                 |                                   |
                 |                                   |
                 v                                   v
       +-------------------+              +-------------------+
       |    Formulario de  |    Datos     |   Base de Datos   |
       |    Agregar        +------------->|   de Inventario   |
       |    Producto       |              |                   |
       +---------+---------+              +---------+---------+
                 |                                   |
                 |                                   |
                 v                                   v
       +-------------------+              +-------------------+
       |    Validación de  |    Datos     |   Actualización   |
       |    Datos          +------------->|   del Inventario  |
       |                   |              |                   |
       +---------+---------+              +---------+---------+
                 |                                   |
                 |                                   |
                 v                                   v
       +-------------------+              +-------------------+
       |    Respuesta de   |    Datos     |    Interfaz de    |
       |    Confirmación   <-------------+    Usuario         |
       |                   |              |                   |
       +-------------------+              +-------------------+

  ### Ejercicio 4

   **Figma:** https://www.figma.com/file/5jVStYTBpjBIGie3VibLLi/Untitled?type=design&node-id=0%3A1&mode=design&t=FqmWTsGOWbICJn9W-1

 ## 3. Diseño del Programa

  ### Ejercicio 5

   Para la aplicación web de gestión de inventario, una arquitectura adecuada sería la arquitectura de tres capas, que consta de:

    1. **Capa de Presentación (Frontend):**
    - Responsable de la interfaz de usuario con la que interactúan los usuarios.
    - Puede ser desarrollada utilizando tecnologías como HTML, CSS y JavaScript para la parte del cliente, y frameworks de frontend como React.js o Angular para construir la interfaz de usuario dinámica y atractiva.
    - La capa de presentación se encarga de enviar las solicitudes del usuario al servidor y mostrar los datos recibidos de la capa de lógica de negocio.

    2. **Capa de Lógica de Negocio (Backend):**
    - Contiene la lógica de la aplicación y se encarga de procesar las solicitudes del usuario, realizar operaciones en la base de datos y devolver los resultados al cliente.
    - Puede ser desarrollada utilizando un lenguaje de programación como Python, Java, C#, PHP, entre otros.
    - Utiliza un framework web como Django, Flask, Spring Boot, ASP.NET, Laravel, etc., para facilitar el desarrollo de la lógica de negocio y la integración con la capa de datos.

    3. **Capa de Datos (Base de Datos):**
    - Almacena los datos de la aplicación, incluidos los productos del inventario, usuarios, roles, transacciones, etc.
    - Puede ser una base de datos relacional como MySQL, PostgreSQL, SQL Server, o una base de datos NoSQL como MongoDB, dependiendo de los requisitos de la aplicación.
    - La capa de datos proporciona un almacenamiento persistente para la aplicación y es accesible desde la capa de lógica de negocio para realizar operaciones de lectura y escritura.

   #### Justificación de la Elección:

    La arquitectura de tres capas proporciona una separación clara de las preocupaciones y facilita la escalabilidad, mantenibilidad y reutilización del código. Además, permite una mejor gestión de los cambios y una mayor flexibilidad.

   #### Ejercicio 6: Diseño de la Base de Datos

    Para la aplicación web de gestión de inventario, el diseño de la base de datos podría incluir las siguientes tablas:

    1. **Tabla de Usuarios:**
    - id_usuario (PK)
    - nombre_usuario
    - contraseña
    - rol

    2. **Tabla de Productos:**
    - id_producto (PK)
    - nombre_producto
    - descripción
    - id_categoria (FK)
    - cantidad_stock
    - precio
    - código_barras

    3. **Tabla de Categorías:**
    - id_categoria (PK)
    - nombre_categoria

    4. **Tabla de Transacciones:**
    - id_transacción (PK)
    - id_producto (FK)
    - tipo_transacción (entrada/salida)
    - cantidad
    - fecha

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
