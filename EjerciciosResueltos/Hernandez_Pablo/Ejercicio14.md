Ejercicio 14
Histoias de usuarios de una aplicacion de gestión de presupuesto de galpones para aves

1. EPICA: Gestionar presupuestos
1a. Titulo: Registrar nuevo presupuesto
	Como: Usuario Gestor de presupuestos
	Quiero: Dar de alta presupuestos en el sistema
	Para: Darles seguimiento
	Validación: Confirmacion de creación de registro haciendo una busqueda en la db

1b. Titulo: Editar presupuesto existente
	Como: Usuario Gestor de presupuestos
	Quiero: Modificar los datos y/o el estado de los presupuestos cargados previamente
	Para: Corregir o actualizar la información 
	Validación: Confirmacion de modificacion de registro revisando la fecha y hora de edicion del presupuesto en la db

1c. Titulo: Eliminar presupuesto existente
	Como: Usuario Gestor de presupuestos
	Quiero: Borrar presupuestos cargados previamente
	Para: Limpiar 
	Validación: Confirmacion de eliminacion de registro haciendo una busqueda en la db

1d. Titulo: Buscar presupuesto existente
	Como: Usuario Gestor de presupuestos
	Quiero: Buscar presupuestos por criterios como fecha, cliente o estado
	Para: Localizar rápidamente información específica sobre presupuestos previamente registrados
	Validación: Presentación de resultados relevantes y precisos de acuerdo con los criterios de búsqueda.

1e. Titulo: Enviar presupuesto
	Como: Usuario Gestor de presupuestos
	Quiero: Enviar el presupuesto al cliente por las vias de contacto disponibles
	Para: Informarle y esperar su respuesta
	Validación: Verificar la confirmacion de entrega exitosa de cada plataforma utilizada

2. EPICA: Generar reportes
Titulo: Generar reportes
	Como: Administrador
	Quiero: Generar reportes con informacion relevante de los presupuestos
	Para: Tomar decisiones
	Validación: Documento de reporte generado
