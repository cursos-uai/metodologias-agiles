# Objetivo

Desarrollar una aplicación web que permita a los usuarios gestionar sus finanzas personales de manera eficiente y segura. La aplicación debe cumplor con los siguientes requisitos funcionales.

## 1. Gestión de cuentas bancarias.

- Permitir la creación y edición de cuentas bancarias.
- Visualizar el saldo actual y el historial de movimientos de cada cuenta.
- Realiazr transferencias entre cuentas propias.
- Descargar el historial de movimientos en formato CSV o PDF

## 2. Gestión de ingresos y gastos.

- Permitir la ceración y edición de ingresos y gastos.
- Categorizar los ingresos y los gastos por tipo (salario, alquiler, alimentación, etc)
- Visualizar gráficos y reportes sobre los ingresos y gastos por categoria y período de tiempo.
- Establecer presupuestos para diferentes categorias de gastos.

## 3. Gestión de deudas

- Permitir la creación y edición de deudas.
- Indicar el monto total de la deuda, la tasa de interés, el plazo de pago y el monto de las cuotas.
- Visualizar un calendario de pagos y realizar simulaciones de diferentes escenarios de pago.
- Generar informes sobre el progreso en el pago de las deudas.

# Resolver.

### Estimación del tamaño del proyecto.

Primero que todo analizamos los requerimientos del sistema en busqueda de definir cuales seran los procesos funcionales y movimientos de datos que los component, para luego asignarle un punto de función COSMIC a cada movimiento de datos identificado

## 1. Gestión de cuentas bancarias.

- Permitir la creación y edición de cuentas bancarias.
  - Entrada: Seleccionar crear o modificar una cuenta bancaria
  - Salida: Solicitar datos para la creacion de una cuenta
  - Salida: Solicitar modificar datos existentes de una cuenta bancaria
  - Entrada: Ingreso de datos requeridos
  - Salida: Confirmacion de creacion o modificacion de cuenta.
- Visualizar el saldo actual y el historial de movimientos de cada cuenta.
  - Salida: Listar el saldo actual de la cuenta principal
  - Salida: Listar los movimientos de cada cuenta
- Realiazr transferencias entre cuentas propias.
  - Entrada: Seleccionar la opcion transferencia entre cuentas propias
  - Salida: Mostrar cuentas disponibles
  - Entrada: Seleccionar cuenta a transferir
  - Salida: Solicitar monto a transferir
  - Entrada: Ingresar monto a transferir
  - Escritura: Decrementar el monto transferido del saldo de la cuenta origen
  - Escritura: Decrementar el monto transferido del saldo de la cuenta origen
- Descargar el historial de movimientos en formato CSV o PDF
  - Entrada: Seleccionar el historial de movimientos.
  - Salida: Mostrar el historial de movimientos.
  - Entrada: Seleccionar el formato a exportar
  - Salida: Exportar el historial de movimientos en el formato solicitado

Requerimiento 1: 18 puntos de funcion COSMIC estimados

## 2. Gestión de ingresos y gastos.

- Permitir la creación y edición de ingresos y gastos.
  - Entrada: Seleccionar cargar un nuevo movimiento
  - Entrada: Seleccionar tipo de movimiento
  - Salida: Solicitar datos requeridos
  - Entrada: Ingresar datos solicitados
  - Escritura: Crear nuevo registro con el nuevo movimiento
  - Escritura: Actualizar el saldo de la cuenta
- Categorizar los ingresos y los gastos por tipo (salario, alquiler, alimentación, etc)
  - Salida: Filtrar los ingresos por tipo y mostrarlos
  - Salida: Filtrar los gastos por tipo y mostrarlos
- Visualizar gráficos y reportes sobre los ingresos y gastos por categoria y período de tiempo.
  - Entrada: Especificar periodo de tiempo
  - Salida: Mostrar grafico ingresos por categoria
  - Salida: Mostrar grafico gastos por categoria
  - Salida: Generar reportes de ingresos y gastos
- Establecer presupuestos para diferentes categorias de gastos.
  - Entrada: Seleccionar categoria de gastos para agregar presupuesto
  - Salida: Solicitar monto correspondiente al presupuesto de categoria
  - Entrada: Ingresr presupuesto
  - Escritura: Almacenar nuevo presupuesto para la categoria de gasto correspondiente

Requerimiento 1: 16 puntos de funcion COSMIC estimados

## 3. Gestión de deudas

- Permitir la creación y edición de deudas.
  - Entrada: Seleccionar cargar un nuevo deuda o editar deuda existente
  - Salida: Solicitar datos requeridos
  - Entrada: Ingresar datos solicitados
  - Escritura: Crear nuevo registro con el la nueva deuda o modificar existente
  - Escritura: Actualizar la deuda de la cuenta
- Indicar el monto total de la deuda, la tasa de interés, el plazo de pago y el monto de las cuotas.
  - Lectura: Consultar deudas existentes en la cuenta
  - Salida: Listar deudas, monto total, tasa de interes, plazo de pago y monto de las cuotas
- Visualizar un calendario de pagos y realizar simulaciones de diferentes escenarios de pago.
  - Lectura: Consultar pagos pendientes
  - Entrada: Seleccionar rango temporal
  - Salida: Mostrar calendario con las simulaciones de escenarios de pago generadas
- Generar informes sobre el progreso en el pago de las deudas.
  - Entrada: Iniciar proceso de generacion de informes al presionar un boton.
  - Lectura: Consultar deudas existentes de la cuenta
  - Salida: Mostrar informe sobre el progreso en el pago de las deudas

Requerimiento 1: 14 puntos de funcion COSMIC estimados

Utilizando el metodo COSMIC, se estima que el tamaño funcional total del proyecto es de 48 puntos de funcion COSMIC (PFC)

### Calculo del costo por punto de función.

Supongamos un equipo de 5 personar cuyo costo mensial es de 12.500 usd
Costo por punto de funcion = costo equipo mes / promedio puntos mes
Costo de funcion = 12500$ / 15 puntos funcion cosmic
Costo funcion = 833 UDS

El costo por punto de funcion (CPFC ) se estima en 833 USD.

### Cantidad de puntos de función que se pueden hacer en un mes:

Se estima que un equipo de desarrollo de software de 5 personas puede desarrollar 15 puntos de Función COSMIC(PFC)

### Duración del proyecto.

Para definir la duracion del proyecto podemos hacer uso de los puntos de funcion COSMIC identificados para el proyecto y el promedio de puntos de funcion completados por mes por el equipo de desarrollo en promedio.

Duración del proyecto = puntos de funcion del proyecto/ promedio puntos de funcion por mes

Duración del proyecto = 48 / 15 = 3.2

La duración del proyecto se estima en 3 meses y medio para ser cautos.

### Costo del proyecto

Para calcular el costo total del proyecto hacemos uso del total de puntos de funcion COSMIC identificados y del costo calculado con anterioridad por punto fe funcion COSMIC.

Costo Total = Precio Punto Funcion \* Total Puntos Funcion
Costo Total = 833 usd x 48 PFC = 39.984

El costo total del proyecto se estima en 39.984 USD
