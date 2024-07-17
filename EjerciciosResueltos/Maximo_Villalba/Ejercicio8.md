# Requisitos Funcionales:

El sistema debe permitir a los usuarios registrarse y crear una cuenta.
Los usuarios deben poder iniciar y cerrar sesión.
Debe haber un sistema de roles para definir permisos (por ejemplo, administrador y usuario).
Los usuarios deben poder subir y gestionar archivos.
El sistema debe permitir a los usuarios compartir archivos con otros usuarios.
Debe existir un sistema de búsqueda para localizar archivos rápidamente.
El sistema debe generar informes sobre el uso y las estadísticas de los archivos.

# Requisitos No Funcionales:

El sistema debe tener una interfaz amigable y fácil de usar.
Debe ser seguro, con autenticación robusta y protección de datos.
Debe ser escalable para manejar un gran número de usuarios y archivos.
Debe ser compatible con múltiples dispositivos y navegadores.
Debe tener tiempos de respuesta rápidos para una experiencia de usuario fluida.
Debe cumplir con estándares de accesibilidad.
Debe estar bien documentado para facilitar el mantenimiento y la ampliación.

# Ejercicio 2: Caso de Uso "Subir un Nuevo Archivo"
Nombre: Subir un Nuevo Archivo

Actor Principal: Usuario

Objetivo: Permitir al usuario subir un nuevo archivo al sistema.

Precondiciones:

El usuario ha iniciado sesión en el sistema.
El usuario tiene permisos para subir archivos.
Flujo Básico:

El usuario selecciona la opción "Subir Archivo" en la interfaz de usuario.
El sistema muestra un formulario para seleccionar el archivo a subir.
El usuario elige el archivo desde su dispositivo.
El usuario confirma la subida del archivo.
El sistema valida el archivo seleccionado.
Si el archivo es válido, el sistema guarda el archivo en el servidor y actualiza la base de datos.
El sistema muestra un mensaje de confirmación de que el archivo se ha subido correctamente.
El caso de uso termina.

Flujos Alternativos:

Si el archivo seleccionado no es válido (por ejemplo, formato no permitido o tamaño excesivo), el sistema muestra un mensaje de error y solicita al usuario que elija otro archivo.
Si el usuario cancela la operación, el caso de uso termina sin subir un nuevo archivo.
Diseño del Sistema

# Ejercicio 3: Diagrama de Flujo de Datos
plaintext
Copiar código
+---------------------+       +---------------------+
|  Interfaz de Usuario|       |  Sistema de Archivos|
|                     +------->                     |
+---------+-----------+       +---------+-----------+
          |                             |
          v                             v
+---------------------+       +---------------------+
|  Formulario de Subida|       | Base de Datos      |
|  de Archivos        +------->|  de Archivos       |
+---------+-----------+       +---------+-----------+
          |                             |
          v                             v
+---------------------+       +---------------------+
| Validación de Datos |       | Actualización de la |
|                     +------->  Base de Datos      |
+---------+-----------+       +---------+-----------+
          |                             |
          v                             v
+---------------------+       +---------------------+
| Respuesta de        |       |  Interfaz de Usuario|
| Confirmación        <-------+                     |
+---------------------+       +---------------------+


# Ejercicio 4: Figma
Figma Design

Diseño del Programa
Ejercicio 5: Arquitectura del Sistema
Para una aplicación web de gestión de archivos, una arquitectura adecuada sería la arquitectura de tres capas:

# Capa de Presentación (Frontend):

Responsable de la interfaz de usuario.
Desarrollada utilizando tecnologías como HTML, CSS y JavaScript, y frameworks como React.js o Vue.js.
Se encarga de enviar las solicitudes del usuario al servidor y mostrar los datos recibidos.
Capa de Lógica de Negocio (Backend):

Contiene la lógica de la aplicación.
Desarrollada utilizando lenguajes como Python, Node.js o Ruby.
Utiliza frameworks como Django, Express.js, o Rails para facilitar el desarrollo.
Se encarga de procesar las solicitudes, realizar operaciones en la base de datos y devolver los resultados.
Capa de Datos (Base de Datos):

Almacena los datos de la aplicación, como usuarios, roles y archivos.
Puede ser una base de datos relacional como PostgreSQL o una base de datos NoSQL como MongoDB.
Proporciona almacenamiento persistente accesible desde la capa de lógica de negocio.
Justificación de la Elección:
La arquitectura de tres capas facilita la escalabilidad, mantenibilidad y reutilización del código. Además, permite una mejor gestión de los cambios y una mayor flexibilidad.

# Ejercicio 6: Diseño de la Base de Datos
Para la aplicación web de gestión de archivos, el diseño de la base de datos podría incluir las siguientes tablas:

Tabla de Usuarios:

id_usuario (PK)
nombre_usuario
contraseña
rol
Tabla de Archivos:

id_archivo (PK)
nombre_archivo
id_usuario (FK)
tamaño
fecha_subida
Tabla de Roles:

id_rol (PK)
nombre_rol
Tabla de Comparticiones:

id_comparticion (PK)
id_archivo (FK)
id_usuario_compartido (FK)
permisos
Diseño
Ejercicio 7: Diagrama de Dominio
Entidades:

Usuario: Atributos: user_id, username, password, role_id
Archivo: Atributos: file_id, filename, user_id, size, upload_date
Rol: Atributos: role_id, role_name
Compartición: Atributos: share_id, file_id, shared_user_id, permissions
Relaciones:

Un Usuario puede subir muchos Archivos.
Un Archivo puede ser compartido con muchos Usuarios.
Un Usuario puede tener un Rol.
Diagrama de Clases
Clases:

Usuario

Atributos: user_id, username, password, role_id
Métodos: validar_credenciales(), subir_archivo()
Archivo

Atributos: file_id, filename, user_id, size, upload_date
Métodos: validar_datos(), guardar_en_base_de_datos()
Rol

Atributos: role_id, role_name
Métodos: obtener_usuarios_relacionados()
Compartición

Atributos: share_id, file_id, shared_user_id, permissions
Métodos: asignar_permisos()
Pruebas
Ejercicio 9: Prueba de Validación de Datos
Verificar que se muestre un mensaje de error si se intenta subir un archivo con un formato no permitido.
Verificar que se muestre un mensaje de error si se intenta subir un archivo que excede el tamaño permitido.
Ejercicio 10: Pruebas de Integración para "Subir un Nuevo Archivo"
Prueba de Interfaz de Usuario:

Verificar que la interfaz permita al usuario seleccionar y subir un archivo correctamente.
Verificar que se muestren mensajes de error adecuados en caso de datos inválidos.
Prueba de Lógica de Negocio:

Verificar que la lógica valide correctamente los datos del archivo antes de guardarlo.
Verificar que se manejen adecuadamente los errores de validación.
Prueba de Base de Datos:

Verificar que el archivo se guarde correctamente en la base de datos con todos los atributos almacenados.
Verificar que el inventario de archivos se actualice correctamente después de subir un nuevo archivo.
Mantenimiento
Ejercicio 13: Plan de Mantenimiento para la Aplicación Web
Monitoreo Continuo:

Implementar herramientas para supervisar rendimiento, disponibilidad y seguridad.
Actualizaciones de Software:

Programar actualizaciones regulares, incluyendo parches de seguridad y correcciones de errores.
Respaldo de Datos:

Establecer un sistema de respaldo automático para garantizar la integridad de la información.
Mantenimiento Preventivo:

Realizar limpieza de la base de datos, optimización del código y revisiones de seguridad regularmente.
Gestión de Incidentes:

Desarrollar un plan de acción para responder a incidentes de seguridad y errores críticos.
Ejercicio 14: Implementación de Corrección de Errores
Identificación del Problema:

Analizar el problema detectado a través de informes de usuarios o monitoreo.
Reproducción del Problema:

Reproducir el problema en un entorno de desarrollo para comprender su causa raíz.
Desarrollo de la Solución:

Implementar la corrección utilizando prácticas de desarrollo seguro.
Pruebas de Calidad:

Realizar pruebas exhaustivas para garantizar que la corrección no cause efectos secundarios no deseados.