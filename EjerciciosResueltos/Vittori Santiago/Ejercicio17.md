# Ejercicio 17 | Estimación de Costos
---

## Estimación de costos para una aplicación de gestión de finanzas personales

### Objetivo

Desarrollar una aplicación web que permita a los usuarios gestionar sus finanzas personales de manera eficiente y segura. La aplicación debe cumplir con los siguientes requisitos funcionales:

#### 1. Gestión de Cuentas Bancarias:
- Permitir la creación y edición de cuentas bancarias.
- Visualizar el saldo actual y el historial de movimientos de cada cuenta.
- Realizar transferencias entre cuentas propias.
- Descargar el historial de movimientos en formato CSV o PDF.

#### 2. Gestión de Ingresos y Gastos:
- Permitir la creación y edición de ingresos y gastos.
- Categorizar los ingresos y gastos por tipo (salario, alquiler, alimentación, etc.).
- Visualizar gráficos y reportes sobre los ingresos y gastos por categoría y período de tiempo.
- Establecer presupuestos para diferentes categorías de gastos.

#### 3. Gestión de Deudas:
- Permitir la creación y edición de deudas.
- Indicar el monto total de la deuda, la tasa de interés, el plazo de pago y el monto de las cuotas.
- Visualizar un calendario de pagos y realizar simulaciones de diferentes escenarios de pago.
- Generar informes sobre el progreso en el pago de las deudas.

### Resolución de la Estimación de Costos

#### 1. Identificación de las Interacciones Funcionales:
Analizando los requisitos funcionales, se identifican las siguientes interacciones entre los usuarios y la aplicación:

- Creación y edición de cuentas bancarias.
- Visualización de saldo actual y movimientos.
- Realización de transferencias entre cuentas.
- Descarga de historial de movimientos.
- Creación y edición de ingresos y gastos.
- Categorización de ingresos y gastos.
- Visualización de gráficos y reportes.
- Establecimiento de presupuestos.
- Creación y edición de deudas.
- Visualización de calendario de pagos.
- Generación de informes de progreso.

#### 2. Clasificación de las Interacciones Funcionales:
Cada interacción funcional se clasifica en una de las tres categorías de tamaño COSMIC: Pequeña (S), Mediana (M) o Grande (L).

- **Creación y edición de cuentas bancarias**: M
- **Visualización de saldo actual y movimientos**: M
- **Realización de transferencias entre cuentas**: M
- **Descarga de historial de movimientos**: S
- **Creación y edición de ingresos y gastos**: M
- **Categorización de ingresos y gastos**: S
- **Visualización de gráficos y reportes**: L
- **Establecimiento de presupuestos**: M
- **Creación y edición de deudas**: M
- **Visualización de calendario de pagos**: L
- **Generación de informes de progreso**: M

#### 3. Cálculo del Tamaño Funcional:
Asignando un valor de Puntos de Función COSMIC (PFC) a cada interacción:
- Pequeña (S): 5 PFC
- Mediana (M): 10 PFC
- Grande (L): 15 PFC

Tamaño funcional total:
- Creación y edición de cuentas bancarias: 10 PFC
- Visualización de saldo actual y movimientos: 10 PFC
- Realización de transferencias entre cuentas: 10 PFC
- Descarga de historial de movimientos: 5 PFC
- Creación y edición de ingresos y gastos: 10 PFC
- Categorización de ingresos y gastos: 5 PFC
- Visualización de gráficos y reportes: 15 PFC
- Establecimiento de presupuestos: 10 PFC
- Creación y edición de deudas: 10 PFC
- Visualización de calendario de pagos: 15 PFC
- Generación de informes de progreso: 10 PFC

**Tamaño Funcional Total**: 110 PFC

#### 4. Obtención del Costo por Punto de Función:
Investigando el costo promedio de desarrollo de software en la región y considerando la complejidad del proyecto, se estima que el costo por punto de función (CPFC) es de 100 USD.

#### 5. Determinación de la Cantidad de PFC por Mes:
Un equipo de desarrollo de software de 5 personas puede desarrollar 20 PFC por mes, considerando la experiencia y eficiencia del equipo.

#### 6. Cálculo de la Duración del Proyecto:
Dividiendo el tamaño funcional total del proyecto (110 PFC) por la cantidad de PFC que se pueden desarrollar por mes (20 PFC/mes), se obtiene la duración estimada del proyecto en meses:

Duración del Proyecto = 110 PFC / 20 PFC = 5.5 meses

#### 7. Estimación del Costo Total:
Multiplicando el tamaño funcional total del proyecto (110 PFC) por el costo por punto de función (100 USD/PFC), se obtiene el costo total estimado del proyecto:

Costo Total = 110 PFC x 100 USD = 11,000 USD

### Consideraciones Adicionales
Para mejorar la estimación y asegurar la precisión, se pueden agregar los siguientes pasos y detalles:

- **Revisión del Proceso de Estimación**: Implementar una revisión por pares del proceso de estimación para identificar posibles omisiones o errores.
- **Factores de Riesgo y Contingencia**: Incluir una contingencia del 15% para cubrir posibles riesgos y cambios en los requisitos, llevando el costo total a 12,650 USD.
- **Uso de Herramientas de Gestión**: Emplear herramientas de gestión de proyectos y seguimiento de tiempo (e.g., Jira, Trello) para monitorear el progreso y ajustar la estimación de costos en tiempo real.
- **Entrenamiento y Capacitación**: Considerar el costo de capacitación del equipo en tecnologías específicas necesarias para el proyecto, lo que puede agregar aproximadamente 1,000 USD al presupuesto total.

### Resumen Final

- **Tamaño Funcional Total**: 110 PFC
- **Costo por Punto de Función**: 100 USD/PFC
- **Cantidad de PFC por Mes**: 20 PFC/mes
- **Duración del Proyecto**: 5.5 meses
- **Costo Total Estimado**: 11,000 USD
- **Costo con Contingencia**: 12,650 USD
- **Costo Total con Capacitación**: 13,650 USD