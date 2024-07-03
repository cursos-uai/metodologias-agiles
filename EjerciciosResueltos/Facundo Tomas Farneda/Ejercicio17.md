# Ejercicio 17

Se asume que el equipo de desarrollo esta compuesto por 3 integrantes y su promedio de puntos de función es de 14 por mes.

## Gestión de cuentas bancarias

### Creación de cuentas

1. Entrada: Introducir datos del usuario
2. Lectura: Leer los datos del usuario
3. Escritura: Crear un registro en la base de datos con los datos del usuario
4. Salida: Mostrar en pantalla que la creación resultó en un éxito

### Edición de cuentas

1. Entrada: Introducir datos del usuario
2. Lectura: Leer los datos del usuario
3. Lectura: Verificar que los datos del usuario están en la base de datos
4. Entrada: Introducir nuevos datos del usuario
5. Lectura: Leer los nuevos datos del usuario
6. Lectura: Validar que no coincidan con los datos previos
7. Escritura: Modificar el registro del usuario con los nuevos datos
8. Salida: Mostrar en pantalla que la modificación resultó en un éxito

### Visualizar saldo actual e historial de movimientos

1. Entrada: Introducir datos del usuario
2. Lectura: Leer los datos del usuario
3. Lectura: Verificar que los datos del usuario están en la base de datos
4. Salida: Mostrar en pantalla el saldo actual e historial de movimientos del usuario

### Realizar transferencias entre cuentas propias

1. Entrada: Elegir a que cuenta transferir
2. Entrada: Introducir monto a transferir
3. Lectura: Verificar que la cuenta tenga suficientes fondos para transferir
4. Escritura: Restar los fondos de la cuenta que transfiere con el monto a transferir
5. Escritura: Sumar los fondos especificados a la cuenta introducida
6. Salida: Mostrar en pantalla que la transferencia se hizo con éxito
7. Salida: Mostrar los fondos que se tienen actualmente

### Descargar historial de movimientos en formato CSV o PDF

1. Entrada: Presionar botón para imprimir en cierto formato
2. Lectura: Leer historial de movimientos
3. Salida: Crear archivo en cierto formato
4. Salida: Guardar archivo en cierto formato

## Gestión de ingresos y gastos

### Creación de ingresos

1. Entrada: Introducir nombre de ingreso
2. Lectura: Leer nombre introducido
3. Escritura: Crear un registro en la base de datos sobre dicho ingreso

### Creación de gastos

1. Entrada: Introducir nombre de gasto
2. Lectura: Leer nombre de gasto
3. Escritura: Crear un registro en la base de datos sobre dicho gasto

### Categorizar ingresos y gastos por tipo

1. Entrada: Seleccionar un gasto o ingreso
2. Lectura: Leer lo que fue seleccionado
3. Entrada: Seleccionar una categoría
4. Lectura: Leer la categoría seleccionada
5. Escritura: Modificar el registro de lo que fue seleccionado con la categoría que fue elegida
6. Salida: Mostrar por pantalla que se categorizó lo que fue elegido

### Visualizar gráficos y reportes sobre los ingresos y gastos por categorías y periodo de tiempo

1. Entrada: Presionar botón reporte de ingresos y gastos
2. Lectura: Leer cuales son los gastos e ingresos que tienen una categoría desde la base de datos
3. Escritura: Calcular reportes según los gastos e ingresos detectados
4. Escritura: Realizar gráficos según los gastos e ingresos detectados
5. Salida: Mostrar los resultados por pantalla

### Establecer presupuestos para diferentes categorías de gastos

1. Entrada: Presionar botón presupuesto
2. Lectura: Leer y agrupar los gastos que tienen una categoría desde la base de datos
3. Lectura: Calcular presupuestos por categoría de gastos
4. Salida: Mostrar por pantalla cada uno de los presupuestos hechos

## Gestión de deudas

### Creación de deudas

1. Entrada: Presionar botón generar deuda
2. Lectura: Leer los detalles de la deuda generada
3. Escritura: Generar un registro de una deuda en la base de datos

### Edición de deudas

1. Entrada: Presionar botón editar en cierta deuda
2. Entrada: Se introducen los nuevos datos de la deuda
3. Lectura: Leer los nuevos detalles de la deuda
4. Escritura: Se modifican los detalles de la deuda en la base de datos.

### Indicar monto total de deuda, tasa de interés, plazo de pago y el monto de las cuotas

1. Entrada: Presionar botón mostrar detalles de cierta deuda
2. Lectura: Leer los detalles de la deuda en la base de datos
3. Salida: Se muestran en pantalla los detalles de cierta deuda

### Visualizar calendario de pagos y realizar simulaciones de diferentes escenarios de pago

1. Entrada: Presionar botón ver calendario de pagos
2. Lectura: Leer las deudas pendientes guardadas en la base de datos
3. Lectura: Realizar simulaciones de los diferentes escenarios de pago posibles
4. Salida: Mostrar en pantalla en calendario y el resultados de las diferentes simulaciones

### Generar informes sobre el progreso en el pago de deudas

1. Entrada: Presionar botón generar informe de pago de deudas
2. Lectura: Leer el progreso del pago de las deudas pendientes guardadas en la base de datos
3. Salida: Mostrar en pantalla el progreso del pago de las deudas pendientes

## Estimación del tamaño del proyecto

Utilizando el método COSMIC, se estima que el tamaño funcional total del proyecto es de 65 Puntos de Función COSMIC (PFC)

## Cálculo del costo por punto de función

Costo mes del equipo: 11800 USD
Puntos de función por mes: 14

CPFC = 11800 USD / 14
CPFC = 848,57 USD

El costo por punto de función se estima en 848,57 USD

## Cantidad de puntos de función que se pueden hacer en un mes

Se estima que un equipo de desarrollo de software de 3 personas puede desarrollar 14 Puntos de Función COSMIC (PFC)

## Duración del proyecto

64 PFC / 14 PFC x mes = 4,57 meses

La duración del proyecto se estima en 4,57 meses

## Costo del proyecto

CPFC x 64 PFC =
848,7 USD x 64 PFC = 54316,8 USD

El costo total del proyecto se estima en 54316,8 USD