## 3. Diseño del Programa:

### Ejercicio 5:
Elige una arquitectura adecuada para la aplicación web del ejercicio 1 y justifica tu elección.



Considerando los requisitos funcionales y no funcionales del sistema de gestión de inventario, propongo una arquitectura de tres capas como la más adecuada para este proyecto. Esta arquitectura ofrece un equilibrio entre flexibilidad, escalabilidad, seguridad y facilidad de mantenimiento.

##### Capas de la arquitectura:

* Capa de presentación (Presentation Layer):
Se encarga de la interacción con el usuario, mostrando interfaces gráficas y procesando entradas del usuario.

* Capa de lógica de negocio (Business Logic Layer):
Implementa las reglas de negocio y la lógica central del sistema.
Procesa las solicitudes de la capa de presentación, realiza cálculos y manipula datos.

* Capa de acceso a datos (Data Access Layer):
Se encarga de la interacción con la base de datos, almacenando, recuperando y administrando datos.
Aísla la capa de lógica de negocio de los detalles de implementación de la base de datos.