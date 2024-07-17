## **1. Identificación y Clasificación de Interacciones Funcionales**

**1. Gestión de cuentas bancarias:**
* Creación y edición de cuentas bancarias - M 
* Visualización de saldo y historial de movimientos - M  
* Transferencias entre cuentas propias - S    
* Descarga de historial en CSV/PDF - S    

**2. Gestión de ingresos y gastos:**    
* Creación y edición de ingresos y gastos - M
* Categorización por tipo - M
* Visualización de gráficos y reportes - L    
* Establecimiento de presupuestos - M 

**3. Gestión de deudas:**   
* Creación y edición de deudas - M    
* Detalles de la deuda y simulaciones de pagos - L   
* Generación de informes sobre el progreso de pago - M

## **2. Cálculo del Tamaño Funcional (PFC)**
**Basado en la clasificación:** 
Basado en la clasificación:

Pequeña (S): 1 PFC
Mediana (M): 2 PFC
Larga (L): 3 PFC


**Funcionalidad / Categoría / PFC**
Creación y edición de cuentas bancarias	M	2
Visualización de saldo y historial de movimientos	M	2
Transferencias entre cuentas propias	S	1
Descarga de historial en CSV/PDF	S	1
Creación y edición de ingresos y gastos	M	2
Categorización por tipo de ingresos y gastos	L	3
Visualización de gráficos y reportes de ingresos y gastos	L	3
Establecimiento de presupuestos para categorías de gastos	M	2
Creación y edición de deudas	M	2
Detalles de la deuda y simulaciones de pagos	L	3
Generación de informes sobre el progreso de pago de deudas	M	2


## 3. Calcular el Tamaño Funcional Total

**Sumamos los valores de PFC de todas las interacciones:**

Tamaño Funcional Total=2+2+1+1+2+2+3+2+2+3+2
Tamaño Funcional Total=24 PFC

## 4. Obtener el Costo por Punto de Función (CPFC)

El costo promedio de desarrollo de software en la región, que estimamos en 100 USD por PFC.

## 5. Determinar la Cantidad de PFC por Mes

Estimamos que un equipo de desarrollo de 4 personas puede desarrollar 15 PFC por mes.

Cantidad de PFC por Mes = 15 PFC/mes
Cantidad de PFC por Mes = 15 PFC/mes

Esta estimación nos permitirá calcular la duración del proyecto basada en el tamaño funcional total de 24 PFC.

## 6. Calcular la Duración del Proyecto

Duración del Proyecto = Tamaño Funcional Total / PFC por Mes
Duración del Proyecto = 24 / 15
Duración del Proyecto ≈ 1.6 meses

Este cálculo nos da una estimación de aproximadamente 1.6 meses para completar el proyecto, considerando un equipo de desarrollo de 4 personas que puede completar 15 PFC por mes.

## 7. Estimar el Costo Total

Costo Total del Proyecto = Tamaño Funcional Total × CPFC
Costo Total del Proyecto = 24 × 100 USD/PFC
Costo Total del Proyecto = 2400 USD