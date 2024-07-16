Ejercicio 17: https://docs.google.com/presentation/d/1NXLf7mJZZ3WC8Yvb7q0q_EbaFFm41ga-I9WwYxtg8m4/edit#slide=id.g211f0ba5be2_0_0

Estimación del Tamaño del Proyecto Utilizando COSMIC:
1.	Identificar las Interacciones Funcionales:
    •	Gestión de cuentas bancarias: (Requerimiento funcional)
        o	Crear/editar cuentas bancarias. (Interacción)
        o	Visualizar saldo y movimientos.
        o	Realizar transferencias.
        o	Descargar historial.
    •	Gestión de ingresos y gastos:
        o	Crear/editar ingresos y gastos.
        o	Categorizar ingresos y gastos.
        o	Visualizar gráficos y reportes.
        o	Establecer presupuestos.
    •	Gestión de deudas:
        o	Crear/editar deudas.
        o	Indicar detalles de la deuda.
        o	Visualizar calendario de pagos.
        o	Generar informes de progreso.

2.	 Clasificar las Interacciones Funcionales:
    •	Crear/editar cuentas bancarias (M).
    •	Visualizar saldo y movimientos (S).
    •	Realizar transferencias (M).
    •	Descargar historial (S).
    •	Crear/editar ingresos y gastos (M).
    •	Categorizar ingresos y gastos (S).
    •	Visualizar gráficos y reportes (M).
    •	Establecer presupuestos (S).
    •	Crear/editar deudas (M).
    •	Indicar detalles de la deuda (M).
    •	Visualizar calendario de pagos (M).
    •	Generar informes de progreso (S).
        o	Total: S = 5, M = 7, L = 0.

3.	Calcular el Tamaño Funcional:
    •	Según la siguiente clasificación de tamaño:
        o	Pequeña (S): 3 PFC.
        o	Mediana (M): 5 PFC.
        o	Grande (L): 7 PFC.
    •	Cada interacción funcional tiene el siguiente valor de PFC:
        o	Crear/editar cuentas bancarias: 5 PFC.
        o	Visualizar saldo y movimientos: 3 PFC.
        o	Realizar transferencias: 5 PFC.
        o	Descargar historial: 3 PFC.
        o	Crear/editar ingresos y gastos: 5 PFC.
        o	Categorizar ingresos y gastos: 3 PFC.
        o	Visualizar gráficos y reportes: 5 PFC.
        o	Establecer presupuestos: 3 PFC.
        o	Crear/editar deudas: 5 PFC.
        o	Indicar detalles de la deuda: 5 PFC.
        o	Visualizar calendario de pagos: 5 PFC.
        o	Generar informes de progreso: 3 PFCT.
    •	Tamaño Funcional Total (X PFC):
        o	 X= 5+3+5+3+5+3+5+3+5+5+5+3 = (5*7) + (7*5) = 50 PFC.
        o	Utilizando el método COSMIC, se estima que el tamaño funcional total del proyecto es de 50 Puntos de Función COSMIC (PFC).

4.	Obtener el Costo por Punto de Función:
    •	Costo mes del equipo: Dependerá del número de personas, remuneración de cada rol, otros gastos, margen de ganancia si es un proyecto para un tercero. Por ejemplo, el equipo tiene 5 personas con un costo mensual total de $20,000.
    •	Puntos de función del mes: Basado en proyectos pasados, podemos saber que el equipo de desarrollo de software produce N cantidad de puntos de función al mes. Por ejemplo, el equipo produce 25 PFC al mes.
    •	Costo por punto de función: 
        o	CPFC = Costo mes del equipo / Puntos de función del mes.
        o	Y = $ 20.000 / 25 PFC = 800 $/ PFC.
        o	El costo por punto de función (CPFC) se estima en 800 USD.

5.	Determinar la Cantidad de PFC por Mes:
    •	Por el punto 4. se sabe que W = 25 PFC/mes.
    •	Se estima que un equipo de desarrollo de software de 5 personas puede desarrollar 25 Puntos de Función COSMIC (PFC) por mes.

6.	Calcular la Duración del Proyecto:
    •	Tamaño Funcional Total(X) = 50 PFC.
    •	PFC por Mes(W) = 25 PFC/mes.
    •	Duración del Proyecto(A) = X/W = 50/25 = 2 Meses.
    •	La duración del proyecto se estima en 2 Meses.

7.	Estimar el Costo Total:
    •	Tamaño Funcional Total(X) = 50 PFC.
    •	Costo por punto de función (CPFC) = 800 $/ PFC.
    •	Costo total del proyecto (B) = X*CPFC = 50 PFC*800 $/ PFC = 40.000 $.
    •	El costo total del proyecto se estima en 40.000 USD.
