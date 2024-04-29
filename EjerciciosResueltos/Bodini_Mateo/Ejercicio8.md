# Ejercicio 1: Análisis de Requerimientos

## Ejercicio 1:
### Requisitos Funcionales:
1. El sistema debe permitir al usuario iniciar sesión como cliente.
2. El sistema debe permitir al usuario explorar productos disponibles en el catálogo.
3. El sistema debe permitir al usuario agregar productos al carrito de compras.
4. El sistema debe permitir al usuario eliminar productos del carrito de compras.
5. El sistema debe permitir al usuario modificar la cantidad de productos en el carrito de compras.
6. El sistema debe permitir al usuario realizar el pago de los productos en el carrito de compras.
7. El sistema debe generar un recibo de compra que incluya detalles sobre los productos adquiridos y el total pagado.

### Requisitos No Funcionales:
1. El sistema debe ser compatible con los principales navegadores web (Google Chrome, Mozilla Firefox, etc.).
2. El sistema debe tener tiempos de carga rápidos para garantizar una experiencia de usuario fluida.
3. El sistema debe ser seguro, con medidas de autenticación y encriptación para proteger la información del usuario y los detalles de la compra.
4. El sistema debe ser intuitivo y fácil de usar, con una interfaz de usuario amigable que guíe al usuario a través del proceso de compra.
5. El sistema debe ser escalable para manejar un crecimiento futuro en la cantidad de productos y usuarios.

## Ejercicio 2:
## Caso de Uso: Agregar un Nuevo Producto al Catálogo
**Actores Principales:** Usuario Administrador

**Precondiciones:** El usuario administrador ha iniciado sesión en el sistema.

### Flujo Básico:
1. El usuario administrador selecciona la opción de agregar un nuevo producto en la interfaz de usuario.
2. El sistema muestra un formulario de ingreso de datos para el nuevo producto, solicitando información como nombre, descripción, categoría, precio, etc.
3. El usuario administrador completa los campos requeridos con la información del nuevo producto.
4. El usuario administrador confirma la creación del nuevo producto.
5. El sistema valida los datos ingresados y agrega el nuevo producto al catálogo.
6. El sistema muestra un mensaje de confirmación al usuario administrador indicando que el producto ha sido agregado exitosamente.

### Excepciones:
1. Si algún campo obligatorio en el formulario de ingreso de datos no se completa, el sistema muestra un mensaje de error y solicita al usuario administrador que complete todos los campos obligatorios antes de continuar.
2. Si la validación de los datos ingresados falla (por ejemplo, un formato incorrecto para el precio), el sistema muestra un mensaje de error específico y solicita al usuario administrador que corrija los datos.

**Postcondiciones:** 
El nuevo producto es agregado con éxito al catálogo de productos disponibles para los clientes.

---
# 2. Diseño del Sistema:
## Ejercicio 3:
![Text](/metodologias-agiles/EjerciciosResueltos/Bodini_Mateo/Screenshot%202024-04-29%20172318.png)
## Ejercicio 4:
![Text](/metodologias-agiles/EjerciciosResueltos/Bodini_Mateo/Inicio.png)

---
# 3. Diseño del Programa:

## Ejercicio 5: 

### Arquitectura de tres capas (Frontend, Backend, Base de Datos)
- **Justificación:** Esta arquitectura separa la aplicación en tres capas distintas: el frontend para la interfaz de usuario, el backend para la lógica de la aplicación y la base de datos para el almacenamiento de datos. Es una opción común y flexible que permite escalabilidad, ya que cada capa puede ser escalada de forma independiente.

## Ejercicio 6
### 

```sql
-- Creación de la base de datos
CREATE DATABASE ecommerce;

-- Selección de la base de datos
USE ecommerce;

-- Tabla de usuarios
CREATE TABLE usuarios (
    id INT PRIMARY KEY AUTO_INCREMENT,
    nombre VARCHAR(50) NOT NULL,
    apellido VARCHAR(50) NOT NULL,
    email VARCHAR(50) NOT NULL,
    password VARCHAR(50) NOT NULL,
    role ENUM('cliente', 'admin') NOT NULL DEFAULT 'cliente'
);

-- Tabla de productos
CREATE TABLE productos (
    id INT PRIMARY KEY AUTO_INCREMENT,
    nombre VARCHAR(50) NOT NULL,
    precio DECIMAL(10, 2) NOT NULL,
    stock INT NOT NULL,
    id_admin INT,
    FOREIGN KEY (id_admin) REFERENCES usuarios(id) ON DELETE SET NULL
);

-- Tabla de compras
CREATE TABLE compras (
    id INT PRIMARY KEY AUTO_INCREMENT,
    id_usuario INT NOT NULL,
    id_producto INT NOT NULL,
    cantidad INT NOT NULL,
    fecha DATE NOT NULL,
    FOREIGN KEY (id_usuario) REFERENCES usuarios(id),
    FOREIGN KEY (id_producto) REFERENCES productos(id)
);

-- Tabla de administradores
CREATE TABLE admins (
    id INT PRIMARY KEY AUTO_INCREMENT,
    nombre VARCHAR(50) NOT NULL,
    apellido VARCHAR(50) NOT NULL,
    email VARCHAR(50) NOT NULL,
    password VARCHAR(50) NOT NULL,
    role ENUM('admin') NOT NULL DEFAULT 'admin'
);

-- Tabla de categorías
CREATE TABLE categorias (
    id INT PRIMARY KEY AUTO_INCREMENT,
    nombre VARCHAR(50) NOT NULL
);

-- Tabla de relación entre productos y categorías
CREATE TABLE productos_categorias (
    id_producto INT NOT NULL,
    id_categoria INT NOT NULL,
    FOREIGN KEY (id_producto) REFERENCES productos(id),
    FOREIGN KEY (id_categoria) REFERENCES categorias(id)
);

-- Tabla de pedidos
CREATE TABLE pedidos (
    id INT PRIMARY KEY AUTO_INCREMENT,
    id_usuario INT NOT NULL,
    fecha DATE NOT NULL,
    FOREIGN KEY (id_usuario) REFERENCES usuarios(id)
);

-- Tabla de detalles de pedidos
CREATE TABLE detalles_pedidos (
    id INT PRIMARY KEY AUTO_INCREMENT,
    id_pedido INT NOT NULL,
    id_producto INT NOT NULL,
    cantidad INT NOT NULL,
    precio DECIMAL(10, 2) NOT NULL,
    FOREIGN KEY (id_pedido) REFERENCES pedidos(id),
    FOREIGN KEY (id_producto) REFERENCES productos(id)
);

-- Tabla de imágenes de productos
CREATE TABLE imagenes_productos (
    id INT PRIMARY KEY AUTO_INCREMENT,
    id_producto INT NOT NULL,
    ruta_imagen VARCHAR(255) NOT NULL,
    FOREIGN KEY (id_producto) REFERENCES productos(id)
);
```