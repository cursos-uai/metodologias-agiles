# Ejercicio 17 estimación de costos

## Ejercicio 1

### 

### Gestión de cuentas bancarias

1. **Crear y editar cuentas bancarias**
    - **Entrada**: Seleccionar la opción de crear o editar una cuenta bancaria.
    - **Entrada**: Ingresar datos de la cuenta (nombre, número, tipo, saldo inicial).
    - **Salida**: Confirmación de creación/edición de la cuenta bancaria.
2. **Visualizar saldo actual y el historial de movimientos de cada cuenta**
    - **Entrada**: Seleccionar la cuenta bancaria deseada.
    - **Lectura**: Obtener saldo actual y el historial de movimientos de la cuenta.
    - **Salida**: Mostrar en pantalla el saldo actual y el historial de movimientos.
3. **Realizar transferencias entre cuentas propias**
    - **Entrada**: Seleccionar la opción de transferencia entre cuentas.
    - **Entrada**: Ingresar cuenta de origen, cuenta de destino y monto a transferir.
    - **Salida**: Confirmación de la transferencia realizada.
4. **Descargar el historial de movimientos en formato CSV o PDF**
    - **Entrada**: Seleccionar la cuenta bancaria.
    - **Entrada**: Seleccionar opción de descarga en CSV o PDF.
    - **Lectura**: Obtener historial de movimientos de la cuenta.
    - **Salida**: Generar y descargar archivo CSV o PDF.

### Gestión de ingresos y gastos

1. **Crear y editar ingresos y gastos**
    - **Entrada**: Seleccionar la opción de crear o editar un ingreso/gasto.
    - **Entrada**: Ingresar datos del ingreso/gasto (categoría, monto, fecha).
    - **Salida**: Confirmación de creación/edición del ingreso/gasto.
2. **Categorizar ingresos y gastos por tipo**
    - **Entrada**: Seleccionar la categoría correspondiente al ingreso/gasto.
    - **Entrada**: Ingresar o editar detalles del ingreso/gasto.
    - **Salida**: Confirmación de categorización.
3. **Visualizar gráficos y reportes sobre ingresos y gastos por categoría y período de tiempo**
    - **Entrada**: Seleccionar la opción de reportes.
    - **Entrada**: Elegir categorías y período de tiempo.
    - **Lectura**: Obtener datos de ingresos y gastos según los filtros seleccionados.
    - **Salida**: Mostrar gráficos y reportes en pantalla.
4. **Establecer presupuestos para diferentes categorías de gastos**
    - **Entrada**: Seleccionar la opción de presupuestos.
    - **Entrada**: Ingresar categorías de gasto y los montos presupuestados.
    - **Salida**: Confirmación de creación/edición de presupuesto.

### Gestión de deudas

1. **Crear y editar deudas**
    - **Entrada**: Seleccionar la opción de crear o editar una deuda.
    - **Entrada**: Ingresar datos de la deuda (monto total, tasa de interés, plazo de pago, monto de las cuotas).
    - **Salida**: Confirmación de creación/edición de la deuda.
2. **Visualizar un calendario de pagos y realizar simulaciones de diferentes escenarios de pago**
    - **Entrada**: Seleccionar la opción de calendario de pagos.
    - **Lectura**: Obtener datos de pagos programados.
    - **Salida**: Mostrar en pantalla el calendario de pagos.
    - **Entrada**: Ingresar datos para simulación (variación de monto/cuota).
    - **Salida**: Mostrar resultados de la simulación en pantalla.
3. **Generar informes sobre el progreso en el pago de las deudas**
    - **Entrada**: Seleccionar la opción de informes de deudas.
    - **Lectura**: Obtener datos de pagos realizados y pendientes.
    - **Salida**: Mostrar informes en pantalla.

## Ejercicio 2

### Clasificación de Interacciones Funcionales

### Gestión de cuentas bancarias

1. **Crear y editar cuentas bancarias**
    - **Entrada**: Seleccionar la opción de crear o editar una cuenta bancaria. (S)
    - **Entrada**: Ingresar datos de la cuenta (nombre, número, tipo, saldo inicial). (S)
    - **Salida**: Confirmación de creación/edición de la cuenta bancaria. (S)
2. **Visualizar saldo actual y el historial de movimientos de cada cuenta**
    - **Entrada**: Seleccionar la cuenta bancaria deseada. (S)
    - **Lectura**: Obtener saldo actual y el historial de movimientos de la cuenta. (M)
    - **Salida**: Mostrar en pantalla el saldo actual y el historial de movimientos. (M)
3. **Realizar transferencias entre cuentas propias**
    - **Entrada**: Seleccionar la opción de transferencia entre cuentas. (S)
    - **Entrada**: Ingresar cuenta de origen, cuenta de destino y monto a transferir. (S)
    - **Salida**: Confirmación de la transferencia realizada. (S)
4. **Descargar el historial de movimientos en formato CSV o PDF**
    - **Entrada**: Seleccionar la cuenta bancaria. (S)
    - **Entrada**: Seleccionar opción de descarga en CSV o PDF. (S)
    - **Lectura**: Obtener historial de movimientos de la cuenta. (M)
    - **Salida**: Generar y descargar archivo CSV o PDF. (M)

### Gestión de ingresos y gastos

1. **Crear y editar ingresos y gastos**
    - **Entrada**: Seleccionar la opción de crear o editar un ingreso/gasto. (S)
    - **Entrada**: Ingresar datos del ingreso/gasto (categoría, monto, fecha). (S)
    - **Salida**: Confirmación de creación/edición del ingreso/gasto. (S)
2. **Categorizar ingresos y gastos por tipo**
    - **Entrada**: Seleccionar la categoría correspondiente al ingreso/gasto. (S)
    - **Entrada**: Ingresar o editar detalles del ingreso/gasto. (S)
    - **Salida**: Confirmación de categorización. (S)
3. **Visualizar gráficos y reportes sobre ingresos y gastos por categoría y período de tiempo**
    - **Entrada**: Seleccionar la opción de reportes. (S)
    - **Entrada**: Elegir categorías y período de tiempo. (S)
    - **Lectura**: Obtener datos de ingresos y gastos según los filtros seleccionados. (M)
    - **Salida**: Mostrar gráficos y reportes en pantalla. (L)
4. **Establecer presupuestos para diferentes categorías de gastos**
    - **Entrada**: Seleccionar la opción de presupuestos. (S)
    - **Entrada**: Ingresar categorías de gasto y los montos presupuestados. (S)
    - **Salida**: Confirmación de creación/edición de presupuesto. (S)

### Gestión de deudas

1. **Crear y editar deudas**
    - **Entrada**: Seleccionar la opción de crear o editar una deuda. (S)
    - **Entrada**: Ingresar datos de la deuda (monto total, tasa de interés, plazo de pago, monto de las cuotas). (S)
    - **Salida**: Confirmación de creación/edición de la deuda. (S)
2. **Visualizar un calendario de pagos y realizar simulaciones de diferentes escenarios de pago**
    - **Entrada**: Seleccionar la opción de calendario de pagos. (S)
    - **Lectura**: Obtener datos de pagos programados. (M)
    - **Salida**: Mostrar en pantalla el calendario de pagos. (M)
    - **Entrada**: Ingresar datos para simulación (variación de monto/cuota). (S)
    - **Salida**: Mostrar resultados de la simulación en pantalla. (M)
3. **Generar informes sobre el progreso en el pago de las deudas**
    - **Entrada**: Seleccionar la opción de informes de deudas. (S)
    - **Lectura**: Obtener datos de pagos realizados y pendientes. (M)
    - **Salida**: Mostrar informes en pantalla. (L)

## Ejercicio 3

Tomando los siguientes valores:

Pequeña (S): 3 PFC

Mediana (M): 7 PFC

Grande (L): 15 PFC

### Gestión de cuentas bancarias

1. **Crear y editar cuentas bancarias - Subtotal**: 9 PFC
2. **Visualizar saldo actual y el historial de movimientos de cada cuenta - Subtotal**: 17 PFC
3. **Realizar transferencias entre cuentas propias - Subtotal**: 9 PFC
4. **Descargar el historial de movimientos en formato CSV o PDF - Subtotal**: 20 PFC

### Gestión de ingresos y gastos

1. **Crear y editar ingresos y gastos - Subtotal**: 9 PFC
2. **Categorizar ingresos y gastos por tipo - Subtotal**: 9 PFC
3. **Visualizar gráficos y reportes sobre ingresos y gastos por categoría y período de tiempo - Subtotal**: 28 PFC
4. **Establecer presupuestos para diferentes categorías de gastos - Subtotal**: 9 PFC

### Gestión de deudas

1. **Crear y editar deudas - Subtotal**: 9 PFC
2. **Visualizar un calendario de pagos y realizar simulaciones de diferentes escenarios de pago - Subtotal**: 27 PFC
3. **Generar informes sobre el progreso en el pago de las deudas - Subtotal**: 25 PFC

### Tamaño Funcional Total del Proyecto

- **Gestión de cuentas bancarias**: 55 PFC
- **Gestión de ingresos y gastos**: 55 PFC
- **Gestión de deudas**: 61 PFC

**Tamaño Funcional Total del Proyecto**: 171 PFC

## Ejercicio 4

Aproximadamente el costo por punto de fusión o CPFC en argentina es de unos $350 USD, teniendo en cuenta el proyecto que es y que posiblemente sea un cliente argentino.

## Ejercicio 5

En función de la experiencia y eficiencia del equipo, que es de un tamaño de 10 personas, se estima que puede realizar 30 puntos de fusión por mes 

## Ejercicio 6

**Duración del proyecto =**   **171 puntos de función COSMIC total / 30 puntos de función COSMIC por mes**

**Duración del proyecto = 5,7 meses de desarrollo**

## Ejercicio 7

Costo total = **171 puntos de función COSMIC total x $350 USD costo aprox. por punto de fusión**

Costo total del proyecto = $**59.850 USD**