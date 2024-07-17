## Objetivo

Desarrollar una aplicación web que permita a los usuarios gestionar sus finanzas personales de manera eficiente y segura.

## Requisitos Funcionales

1. **Gestión de cuentas bancarias**:
   - Permitir la creación y edición de cuentas bancarias.
   - Visualizar el saldo actual y el historial de movimientos de cada cuenta.
   - Realizar transferencias entre cuentas propias.
   - Descargar el historial de movimientos en formato CSV o PDF.
2. **Gestión de ingresos y gastos**:
   - Permitir la creación y edición de ingresos y gastos.
   - Categorizar los ingresos y gastos por tipo (salario, alquiler, alimentación, etc.).
   - Visualizar gráficos y reportes sobre los ingresos y gastos por categoría y período de tiempo.
   - Establecer presupuestos para diferentes categorías de gastos.
3. **Gestión de deudas**:
   - Permitir la creación y edición de deudas. Indicar el monto total de la deuda, la tasa de interés, el plazo de pago y el monto de las cuotas.
   - Visualizar un calendario de pagos y realizar simulaciones de diferentes escenarios de pago.
   - Generar informes sobre el progreso en el pago de las deudas.

## Resolución

### 1. Identificación de las Interacciones Funcionales

Analizando los requisitos funcionales, se identifican las siguientes interacciones:

1.1 Creación y edición de cuentas bancarias.  
1.2 Visualización del saldo actual y del historial de movimientos.  
1.3 Realización de transferencias entre cuentas propias.  
1.4 Descarga del historial de movimientos.  
2.1 Creación y edición de ingresos y gastos.  
2.2 Categorizar ingresos y gastos.  
2.3 Visualización de gráficos y reportes.  
2.4 Establecimiento de presupuestos.  
3.1 Creación y edición de deudas.  
3.2 Visualización de un calendario de pagos.  
3.3 Generación de informes sobre deudas.

### 2. Clasificación de las Interacciones Funcionales

Cada interacción funcional se clasifica en categorías de tamaño COSMIC:

- **Pequeña (S)**: Interacciones sencillas y directas.
- **Mediana (M)**: Interacciones con complejidad moderada.
- **Grande (L)**: Interacciones complejas y multifacéticas.

| Interacción Funcional                   | Tamaño |
| --------------------------------------- | ------ |
| Creación y edición de cuentas bancarias | M      |
| Visualización del saldo y del historial | M      |
| Realización de transferencias           | M      |
| Descarga del historial de movimientos   | S      |
| Creación y edición de ingresos y gastos | M      |
| Categorizar ingresos y gastos           | S      |
| Visualización de gráficos y reportes    | L      |
| Establecimiento de presupuestos         | M      |
| Creación y edición de deudas            | M      |
| Visualización de un calendario de pagos | M      |
| Generación de informes sobre deudas     | L      |

### 3. Cálculo del Tamaño Funcional

Asignamos un valor de Puntos de Función COSMIC (PFC) a cada interacción:

- **Pequeña (S)**: 2 PFC
- **Mediana (M)**: 4 PFC
- **Grande (L)**: 8 PFC

| Interacción Funcional                   | Tamaño | PFC |
| --------------------------------------- | ------ | --- |
| Creación y edición de cuentas bancarias | M      | 4   |
| Visualización del saldo y del historial | M      | 4   |
| Realización de transferencias           | M      | 4   |
| Descarga del historial de movimientos   | S      | 2   |
| Creación y edición de ingresos y gastos | M      | 4   |
| Categorizar ingresos y gastos           | S      | 2   |
| Visualización de gráficos y reportes    | L      | 8   |
| Establecimiento de presupuestos         | M      | 4   |
| Creación y edición de deudas            | M      | 4   |
| Visualización de un calendario de pagos | M      | 4   |
| Generación de informes sobre deudas     | L      | 8   |

**Tamaño Funcional Total = 48 PFC**

### 4. Cálculo del Costo por Punto de Función

Suponemos que el costo por punto de función (CPFC) es de 150 USD.

### 5. Determinación de la Cantidad de PFC por Mes

Se estima que un equipo de 5 personas puede desarrollar 20 PFC por mes.

### 6. Cálculo de la Duración del Proyecto

Duración del proyecto (A meses) = Tamaño Funcional Total (X PFC) / Cantidad de PFC por mes (W PFC/mes)

Duración del proyecto (A meses) = 48 PFC / 20 PFC/mes = 2.4 meses

Redondeando, la duración del proyecto es de 3 meses.

### 7. Estimación del Costo Total

Costo Total (B USD) = Tamaño Funcional Total (X PFC) × Costo por Punto de Función (Y USD/PFC)

Costo Total (B USD) = 48 PFC × 150 USD/PFC = 7200 USD


- **Tamaño Funcional Total**: 48 PFC
- **Costo por Punto de Función (CPFC)**: 150 USD
- **Cantidad de PFC por mes (W)**: 20 PFC/mes
- **Duración del Proyecto**: 3 meses
- **Costo Total del Proyecto**: 7200 USD
