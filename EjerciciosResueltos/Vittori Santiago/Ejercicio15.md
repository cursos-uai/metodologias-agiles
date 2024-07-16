# Ejercicio 15 | Historia de usuario
---

## Historias de usuario para un sistema informático de presupuesto de construcción de galpones

### 1. Crear presupuesto inicial
**Título**: Crear presupuesto inicial  
**Como** Administrador del sistema  
**Quiero** Crear un presupuesto inicial para la construcción del galpón  
**Para** Tener una estimación de los costos básicos involucrados  

**Validación**: Verificar que al ingresar los parámetros iniciales, el sistema genere un presupuesto que incluya todos los costos básicos (materiales, mano de obra, etc.) y que los totales sean correctos y coherentes con los datos ingresados.

### 2. Seleccionar materiales de construcción
**Título**: Seleccionar materiales de construcción  
**Como** Usuario del sistema  
**Quiero** Seleccionar los materiales de construcción necesarios  
**Para** Personalizar el presupuesto según los materiales específicos requeridos  

**Validación**: Confirmar que el sistema permite seleccionar y cambiar materiales, y que el presupuesto refleje correctamente el costo y las especificaciones de los materiales seleccionados.

### 3. Configurar tamaño del galpón
**Título**: Configurar tamaño del galpón  
**Como** Ingeniero de proyecto  
**Quiero** Configurar el tamaño del galpón en el sistema  
**Para** Ajustar el presupuesto basado en las dimensiones específicas  

**Validación**: Asegurarse de que al modificar las dimensiones del galpón, todos los cálculos de costos se actualicen automáticamente y de forma precisa en el presupuesto.

### 4. Agregar detalles del sistema de ventilación
**Título**: Agregar detalles del sistema de ventilación  
**Como** Técnico en climatización  
**Quiero** Agregar detalles del sistema de ventilación en el presupuesto  
**Para** Asegurar que el presupuesto incluya los costos necesarios para el sistema de ventilación  

**Validación**: Verificar que los detalles del sistema de ventilación se puedan ingresar en el sistema y que el presupuesto refleje correctamente los costos y requisitos de estos sistemas.

### 5. Seleccionar tipo de alimentación automática
**Título**: Seleccionar tipo de alimentación automática  
**Como** Encargado de alimentación  
**Quiero** Seleccionar el tipo de alimentación automática en el sistema  
**Para** Incluir el costo del sistema de alimentación en el presupuesto  

**Validación**: Comprobar que el sistema permite seleccionar diferentes tipos de sistemas de alimentación automática y que el presupuesto se actualice correctamente con los costos asociados.

### 6. Incluir sistema de recolección de residuos
**Título**: Incluir sistema de recolección de residuos  
**Como** Gerente de operaciones  
**Quiero** Incluir un sistema de recolección de residuos en el presupuesto  
**Para** Garantizar un manejo adecuado de los desechos y cumplir con regulaciones sanitarias  

**Validación**: Realizar una prueba funcional para verificar que los costos y detalles del sistema de recolección de residuos se integren correctamente en el presupuesto.

### 7. Estimar costos de mano de obra
**Título**: Estimar costos de mano de obra  
**Como** Jefe de recursos humanos  
**Quiero** Estimar los costos de mano de obra en el sistema  
**Para** Tener una idea completa del costo total de construcción  

**Validación**: Verificar que al ingresar los detalles de los trabajadores y sus respectivas tasas de pago, el sistema calcule y muestre el costo total de mano de obra correctamente.

### 8. Calcular el tiempo estimado de construcción
**Título**: Calcular el tiempo estimado de construcción  
**Como** Planificador de proyectos  
**Quiero** Calcular el tiempo estimado de construcción  
**Para** Planificar el proyecto adecuadamente  

**Validación**: Implementar TDD para la función de cálculo del tiempo, asegurando que los cálculos sean precisos y correctos, y que todas las pruebas unitarias pasen.

### 9. Generar informe detallado del presupuesto
**Título**: Generar informe detallado del presupuesto  
**Como** Administrador del sistema  
**Quiero** Generar un informe detallado del presupuesto  
**Para** Tener un documento formal que pueda ser presentado a inversionistas o directivos  

**Validación**: Realizar una prueba funcional para asegurar que el informe contiene todos los detalles necesarios, como costos por categorías, totales generales, y que el formato sea correcto y comprensible.

### 10. Comparar diferentes opciones de materiales
**Título**: Comparar diferentes opciones de materiales  
**Como** Usuario del sistema  
**Quiero** Comparar diferentes opciones de materiales  
**Para** Elegir la opción más económica y adecuada para el galpón  

**Validación**: Validar que el sistema permite seleccionar y comparar varias opciones de materiales y que el presupuesto se actualice en tiempo real con los costos y especificaciones de las opciones seleccionadas.
