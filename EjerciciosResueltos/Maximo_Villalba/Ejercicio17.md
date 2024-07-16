1. Identificación y Clasificación de Interacciones Funcionales
1. Gestión de cuentas bancarias:

Creación y edición de cuentas bancarias (M)
Visualización de saldo y historial de movimientos (M)
Transferencias entre cuentas propias (M)
Descarga de historial en CSV/PDF (S)
2. Gestión de ingresos y gastos:

Creación y edición de ingresos y gastos (M)
Categorización por tipo (M)
Visualización de gráficos y reportes (L)
Establecimiento de presupuestos (M)
3. Gestión de deudas:

Creación y edición de deudas (M)
Detalles de la deuda y simulaciones de pagos (L)
Generación de informes sobre el progreso de pago (M)
2. Cálculo del Tamaño Funcional (PFC)
Basado en la clasificación:

Pequeña (S): 1 PFC
Mediana (M): 2 PFC
Grande (L): 3 PFC
Funcionalidad	Categoría	PFC
Creación y edición de cuentas bancarias	M	2
Visualización de saldo y historial de movimientos	M	2
Transferencias entre cuentas propias	M	2
Descarga de historial de movimientos en CSV/PDF	S	1
Creación y edición de ingresos y gastos	M	2
Categorización de ingresos y gastos por tipo	M	2
Visualización de gráficos y reportes de ingresos y gastos	L	3
Establecimiento de presupuestos para categorías de gastos	M	2
Creación y edición de deudas	M	2
Detalles de la deuda y simulaciones de pagos	L	3
Generación de informes sobre el progreso de pago de deudas	M	2
3. Calcular el Tamaño Funcional Total
Sumamos los valores de PFC de todas las interacciones para obtener el tamaño funcional total del proyecto:

Tamaño Funcional Total = 23 PFC

4. Obtener el Costo por Punto de Función (CPFC)
Asumimos un costo promedio de desarrollo de software en la región, que estimamos en 120 USD por PFC.

5. Determinar la Cantidad de PFC por Mes
Estimamos que un equipo de desarrollo de 6 personas puede desarrollar 25 PFC por mes.

6. Calcular la Duración del Proyecto
Duración del Proyecto = Tamaño Funcional Total / PFC por Mes = 23 / 25 ≈ 0.92 meses

7. Estimar el Costo Total
Costo Total del Proyecto = Tamaño Funcional Total × CPFC = 23 × 120 = 2760 USD.