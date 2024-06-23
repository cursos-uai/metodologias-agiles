# Ejercicio 14: Historias de usuarios de una aplicación de gestión de presupuesto de galpones para aves

## Objetivo
El objetivo de este ejercicio es que los alumnos universitarios practiquen la creación de historias de usuarios para un sistema informático de presupuesto de construcción de galpones, utilizando la metodología ágil.

## Descripción del ejercicio
1. Los alumnos deberán formar equipos de trabajo, de preferencia de 3 a 5 personas por equipo.
2. Cada equipo deberá seleccionar la temática de construcción de galpones para su sistema informático de presupuesto.
3. Los equipos deberán generar al menos tres historias de usuario para su sistema, basadas en la temática seleccionada. Cada historia de usuario debe incluir un título y una descripción que contenga los criterios de aceptación.
4. Las historias de usuario deben estar enfocadas en las funcionalidades y características del sistema informático, considerando aspectos como la creación de presupuestos detallados, seguimiento del presupuesto durante la construcción, inclusión de etapas, generación de informes, entre otros.
5. Los equipos deben asegurarse de que las historias de usuario sean claras, concisas y comprensibles, siguiendo las buenas prácticas de redacción de historias ágiles.
6. Al finalizar, cada equipo deberá presentar sus historias de usuario al resto de la clase, explicando el contexto de su sistema y los criterios de aceptación de cada historia.
7. Se fomenta el intercambio de ideas y la retroalimentación constructiva entre los equipos durante las presentaciones.

**Nota**: Los equipos pueden utilizar ejemplos y situaciones hipotéticas para desarrollar las historias de usuario, considerando las necesidades y requisitos típicos de un sistema de presupuesto de construcción de galpones. Además, se recomienda utilizar herramientas como tarjetas o post-its para escribir y visualizar las historias de usuario durante el ejercicio.

## Historias de usuario

### Historia de usuario 1
**Título**: Generación de presupuesto  
**Como**: Usuario  
**Quiero**: Generar un presupuesto para la construcción de un galpón  
**Para**: Tener una estimación de los costos antes de iniciar el proyecto  

### Historia de usuario 2
**Título**: Edición de presupuesto  
**Como**: Usuario  
**Quiero**: Editar el presupuesto generado  
**Para**: Ajustar los costos conforme avanza el proyecto y se presentan cambios en los precios o necesidades  

### Historia de usuario 3
**Título**: Seguimiento de presupuesto  
**Como**: Usuario  
**Quiero**: Hacer un seguimiento del presupuesto durante la construcción  
**Para**: Controlar los gastos y evitar sobrecostos  

### Historia de usuario 4
**Título**: Incorporación de etapas del proyecto  
**Como**: Usuario  
**Quiero**: Dividir el proyecto en etapas  
**Para**: Llevar un control más detallado del progreso y los costos asociados a cada etapa  

### Historia de usuario 5
**Título**: Generación de informes  
**Como**: Usuario  
**Quiero**: Generar informes detallados del presupuesto  
**Para**: Presentar a los stakeholders el estado financiero del proyecto  

### Historia de usuario 6
**Título**: Exportar presupuesto en PDF  
**Como**: Usuario  
**Quiero**: Exportar el presupuesto a un archivo PDF  
**Para**: Compartirlo fácilmente con otras personas interesadas en el proyecto  

### Historia de usuario 7
**Título**: Validación de datos de entrada  
**Como**: Usuario  
**Quiero**: Que el sistema valide los datos de entrada  
**Para**: Asegurarme de que la información ingresada sea correcta y consistente  

**Validación**:  
- El sistema debe mostrar un mensaje de error si algún campo requerido está vacío.
- El sistema debe validar que los valores numéricos estén dentro de rangos aceptables.
- El sistema debe permitir solo formatos de fecha válidos.
- Los mensajes de error deben ser claros y específicos sobre el problema detectado.

### Historia de usuario 8
**Título**: Notificaciones de sobrecostos  
**Como**: Usuario  
**Quiero**: Recibir notificaciones cuando el proyecto exceda el presupuesto estimado  
**Para**: Tomar acciones correctivas de inmediato  

### Historia de usuario 9
**Título**: Acceso multiusuario  
**Como**: Administrador  
**Quiero**: Permitir el acceso a múltiples usuarios con diferentes roles  
**Para**: Gestionar el proyecto colaborativamente y de manera segura  

### Historia de usuario 10
**Título**: Historial de versiones del presupuesto  
**Como**: Usuario  
**Quiero**: Ver el historial de versiones del presupuesto  
**Para**: Revisar cambios realizados y mantener un registro de cómo ha evolucionado el presupuesto  

**Validación**:  
- El sistema debe mostrar un listado con todas las versiones del presupuesto, incluyendo fecha y hora de cada modificación.
- Cada versión debe permitir la visualización de los cambios específicos realizados.
- El sistema debe permitir revertir a una versión anterior con un solo clic.

### Historia de usuario 11
**Título**: Asignación de recursos  
**Como**: Usuario  
**Quiero**: Asignar recursos (materiales, mano de obra) a cada etapa del proyecto  
**Para**: Controlar y planificar el uso de los recursos de manera eficiente  

**Validación**:  
- El sistema debe permitir seleccionar recursos de una lista predefinida.
- Debe ser posible asignar cantidades específicas de cada recurso a las diferentes etapas.
- El sistema debe actualizar el presupuesto automáticamente en función de la asignación de recursos.

### Historia de usuario 12
**Título**: Comparación de presupuestos  
**Como**: Usuario  
**Quiero**: Comparar el presupuesto actual con presupuestos anteriores  
**Para**: Analizar diferencias y evaluar el impacto de cambios en el proyecto  

