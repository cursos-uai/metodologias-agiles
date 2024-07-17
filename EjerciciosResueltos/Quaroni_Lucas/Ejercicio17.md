# Objetivo

Desarrollar una aplicación web que permita a los usuarios gestionar sus finanzas personales de manera eficiente y segura. La aplicación debe cumplir con los siguientes requisitos funcionales.

## 1. Gestión de cuentas bancarias

- Permitir la creación y edición de cuentas bancarias.
- Visualizar el saldo actual y el historial de movimientos de cada cuenta.
- Realizar transferencias entre cuentas propias.
- Descargar el historial de movimientos en formato CSV o PDF.

## 2. Gestión de ingresos y gastos

- Permitir la creación y edición de ingresos y gastos.
- Categorizar los ingresos y los gastos por tipo (salario, alquiler, alimentación, etc.).
- Visualizar gráficos y reportes sobre los ingresos y gastos por categoría y período de tiempo.
- Establecer presupuestos para diferentes categorías de gastos.

## 3. Gestión de deudas

- Permitir la creación y edición de deudas.
- Indicar el monto total de la deuda, la tasa de interés, el plazo de pago y el monto de las cuotas.
- Visualizar un calendario de pagos y realizar simulaciones de diferentes escenarios de pago.
- Generar informes sobre el progreso en el pago de las deudas.

# Resolución

### Estimación del tamaño del proyecto

Primero analizamos los requerimientos del sistema para definir los procesos funcionales y movimientos de datos, asignando un punto de función COSMIC a cada movimiento de datos identificado.

## 1. Gestión de cuentas bancarias

- Permitir la creación y edición de cuentas bancarias.
  - Entrada: Seleccionar crear o modificar una cuenta bancaria.
  - Salida: Solicitar datos para la creación de una cuenta.
  - Salida: Solicitar modificar datos existentes de una cuenta bancaria.
  - Entrada: Ingreso de datos requeridos.
  - Salida: Confirmación de creación o modificación de cuenta.
- Visualizar el saldo actual y el historial de movimientos de cada cuenta.
  - Salida: Listar el saldo actual de la cuenta principal.
  - Salida: Listar los movimientos de cada cuenta.
- Realizar transferencias entre cuentas propias.
  - Entrada: Seleccionar la opción transferencia entre cuentas propias.
  - Salida: Mostrar cuentas disponibles.
  - Entrada: Seleccionar cuenta a transferir.
  - Salida: Solicitar monto a transferir.
  - Entrada: Ingresar monto a transferir.
  - Escritura: Decrementar el monto transferido del saldo de la cuenta origen.
  - Escritura: Incrementar el monto transferido al saldo de la cuenta destino.
- Descargar el historial de movimientos en formato CSV o PDF.
  - Entrada: Seleccionar el historial de movimientos.
  - Salida: Mostrar el historial de movimientos.
  - Entrada: Seleccionar el formato a exportar.
  - Salida: Exportar el historial de movimientos en el formato solicitado.

Requerimiento 1: 20 puntos de función COSMIC estimados.

## 2. Gestión de ingresos y gastos

- Permitir la creación y edición de ingresos y gastos.
  - Entrada: Seleccionar cargar un nuevo movimiento.
  - Entrada: Seleccionar tipo de movimiento.
  - Salida: Solicitar datos requeridos.
  - Entrada: Ingresar datos solicitados.
  - Escritura: Crear nuevo registro con el nuevo movimiento.
  - Escritura: Actualizar el saldo de la cuenta.
- Categorizar los ingresos y los gastos por tipo (salario, alquiler, alimentación, etc.).
  - Salida: Filtrar los ingresos por tipo y mostrarlos.
  - Salida: Filtrar los gastos por tipo y mostrarlos.
- Visualizar gráficos y reportes sobre los ingresos y gastos por categoría y período de tiempo.
  - Entrada: Especificar periodo de tiempo.
  - Salida: Mostrar gráfico ingresos por categoría.
  - Salida: Mostrar gráfico gastos por categoría.
  - Salida: Generar reportes de ingresos y gastos.
- Establecer presupuestos para diferentes categorías de gastos.
  - Entrada: Seleccionar categoría de gastos para agregar presupuesto.
  - Salida: Solicitar monto correspondiente al presupuesto de categoría.
  - Entrada: Ingresar presupuesto.
  - Escritura: Almacenar nuevo presupuesto para la categoría de gasto correspondiente.

Requerimiento 2: 18 puntos de función COSMIC estimados.

## 3. Gestión de deudas

- Permitir la creación y edición de deudas.
  - Entrada: Seleccionar cargar una nueva deuda o editar deuda existente.
  - Salida: Solicitar datos requeridos.
  - Entrada: Ingresar datos solicitados.
  - Escritura: Crear nuevo registro con la nueva deuda o modificar existente.
  - Escritura: Actualizar la deuda de la cuenta.
- Indicar el monto total de la deuda, la tasa de interés, el plazo de pago y el monto de las cuotas.
  - Lectura: Consultar deudas existentes en la cuenta.
  - Salida: Listar deudas, monto total, tasa de interés, plazo de pago y monto de las cuotas.
- Visualizar un calendario de pagos y realizar simulaciones de diferentes escenarios de pago.
  - Lectura: Consultar pagos pendientes.
  - Entrada: Seleccionar rango temporal.
  - Salida: Mostrar calendario con las simulaciones de escenarios de pago generadas.
- Generar informes sobre el progreso en el pago de las deudas.
  - Entrada: Iniciar proceso de generación de informes al presionar un botón.
  - Lectura: Consultar deudas existentes de la cuenta.
  - Salida: Mostrar informe sobre el progreso en el pago de las deudas.

Requerimiento 3: 16 puntos de función COSMIC estimados.

### Estimación total

Utilizando el método COSMIC, se estima que el tamaño funcional total del proyecto es de 54 puntos de función COSMIC (PFC).

### Cálculo del costo por punto de función

Supongamos un equipo de 5 personas cuyo costo mensual es de 15,000 USD.
Costo por punto de función = costo equipo mes / promedio puntos mes
Costo por punto de función = 15,000 USD / 18 PFC
Costo por punto de función = 833 USD

El costo por punto de función (CPFC) se estima en 833 USD.

### Cantidad de puntos de función por mes

Se estima que un equipo de desarrollo de software de 5 personas puede desarrollar 18 puntos de función COSMIC (PFC) por mes.

### Duración del proyecto

Para definir la duración del proyecto, utilizamos los puntos de función COSMIC identificados y el promedio de puntos de función completados por mes por el equipo de desarrollo.

Duración del proyecto = puntos de función del proyecto / promedio puntos de función por mes
Duración del proyecto = 54 / 18 = 3

La duración del proyecto se estima en 3 meses.

### Costo del proyecto

Para calcular el costo total del proyecto utilizamos el total de puntos de función COSMIC identificados y el costo calculado por punto de función COSMIC.

Costo Total = Precio Punto Función * Total Puntos Función
Costo Total = 833 USD * 54 PFC = 44,982 USD

El costo total del proyecto se estima en 44,982 USD.