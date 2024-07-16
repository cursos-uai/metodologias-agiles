# Ejercicio Estimación de costos

## 1. Identificación de las Interacciones Funcionales

Basándonos en los requisitos funcionales, identificamos las siguientes interacciones entre los usuarios y la aplicación:

1. Gestión de cuentas bancarias
- Crear una cuenta bancaria.
- Editar una cuenta bancaria.
- Visualizar el saldo actual.
- Visualizar el historial de movimientos.
- Realizar transferencias entre cuentas propias.
- Descargar el historial de movimientos en formato CSV.
- Descargar el historial de movimientos en formato PDF.

2. Gestión de ingresos y gastos
- Crear un ingreso.
- Editar un ingreso.
- Crear un gasto.
- Editar un gasto.
- Categorizar ingresos y gastos.
- Visualizar gráficos de ingresos y gastos por categoría.
- Visualizar reportes de ingresos y gastos por periodo de tiempo.
- Establecer presupuestos para diferentes categorías de gastos.

3. Gestión de deudas
- Crear una deuda.
- Editar una deuda.
- Indicar el monto total de la deuda.
- Indicar la tasa de interés de la deuda.
- Indicar el plazo de pago de la deuda.
- Indicar el monto de las cuotas.
- Visualizar un calendario de pagos.
- Realizar simulaciones de diferentes escenarios de pago.
- Generar informes sobre el progreso en el pago de las deudas.

## 2. Clasificación de las Interacciones Funcionales
Clasificamos cada interacción funcional en una de las tres categorías de tamaño COSMIC:
Pequeña (S): 1 PFC
Mediana (M): 2 PFC
Grande (L): 3 PFC

| Funcionalidad| Categoría|PFC|
| ----- |:-----:|:----:|
|Crear una cuenta bancaria|S|1|
|Editar una cuenta bancaria|S|1|
|Visualizar el saldo actual|S|1|
|Visualizar el historial de movimientos|M|2|
|Realizar transferencias entre cuentas propias|M|2|
|Descargar el historial de movimientos en formato CSV|S|1|
|Descargar el historial de movimientos en formato PDF|S|1|
|Crear un ingreso|S|1|
|Editar un ingreso|S|1|
|Crear un gasto|S|1|
|Editar un gasto|S|1|
|Categorizar ingresos y gastos|M|2|
|Visualizar gráficos de ingresos y gastos por categoría|M|2|
|Visualizar reportes de ingresos y gastos por periodo|M|2|
|Establecer presupuestos para categorías de gastos|M|2|
|Crear una deuda|S|1|
|Editar una deuda|S|1|
|Indicar el monto total de la deuda|S|1|
|Indicar la tasa de interés de la deuda|S|1|
|Indicar el plazo de pago de la deuda|S|1|
|Indicar el monto de las cuotas|S|1|
|Visualizar un calendario de pagos|M|2|
|Realizar simulaciones de escenarios de pago|L|3|
|Generar informes sobre el progreso en el pago de deudas|M|2|

## 3. Calcular el Tamaño Funcional Total

Sumamos los valores de PFC de todas las interacciones para obtener el tamaño funcional total del proyecto:

    Tamaño Funcional Total = 37

## 4. Obtener el Costo por Punto de Función (CPFC)

Asumimos un costo promedio de desarrollo de software en la región que estimamos en 150 USD por PFC, considerando la complejidad del proyecto.

## 5. Determinar la Cantidad de PFC por Mes

Estimamos que un equipo de desarrollo de 5 personas puede desarrollar 20 PFC por mes.

## 6. Calcular la Duración del Proyecto

    Duración del Proyecto = Tamaño Funcional Total / PFC por Mes = 37/20 ≈ 2 meses

## 7. Estimar el Costo Total

    Costo Total del Proyecto = Tamaño Funcional Total × CPFC = 37 × 150 = 5550 USD.