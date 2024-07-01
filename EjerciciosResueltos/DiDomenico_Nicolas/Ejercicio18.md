Ejercicio 18 + Presentación:
-	Integrantes del grupo: Bugari Estefano, Di Domenico Nicolás, Mandrile Laureano, Mandrile Nicolás.
-	Contexto: Una empresa de desarrollo de software ha decidido adoptar la metodología Scrum para mejorar la eficiencia y calidad de sus proyectos. Tu equipo ha sido seleccionado para liderar la implementación de Scrum en un nuevo proyecto de desarrollo de una aplicación web para una empresa de logística.


-	Número de prompt: 1.
-	Rol que representa el prompt: Product Owner.
-	Entrada de información que recibe el prompt: El cliente ha proporcionado los siguientes requerimientos iniciales para una aplicación web de gestión de envíos logísticos:
    -	Administración de perfiles de usuario.
    -	Notificaciones automáticas sobre el estado de los envíos.
    -	Soporte para múltiples idiomas en la interfaz de usuario.
    -	Funcionalidad de chat para soporte en tiempo real.
-	Prompt: En el contexto de la metodología scrum, actúa como product owner para el proyecto de desarrollo de una aplicación web para una empresa de logística.
-	Resultado de ejecutar el prompt: Product Backlog Inicial.
    1.	Historia de Usuario 1: Administración de Perfiles de Usuario.
        -	Como: Usuario del sistema.
        -	Quiero: Poder administrar mi perfil para actualizar mi información personal.
        -	Para: Mantener mi información actualizada y segura.
        -	Validación: El sistema permite editar y guardar cambios en el perfil, y muestra una notificación de confirmación después de actualizar la información.
    2.	Historia de Usuario 2: Notificaciones Automáticas sobre el Estado de los Envíos.
        -	Como: Usuario del sistema.
        -	Quiero: Recibir notificaciones automáticas sobre el estado de mis envíos.
        -	Para: Estar al tanto del progreso y estado de mis envíos en tiempo real.
        -	Validación: El sistema envía notificaciones automáticas en tiempo real sobre cambios de estado del envío, y permite configurar preferencias de notificación.
    3.	Historia de Usuario 3: Soporte para Múltiples Idiomas en la Interfaz de Usuario.
        -	Como: Usuario del sistema.
        -	Quiero: Cambiar el idioma de la interfaz de usuario.
        -	Para: Utilizar la aplicación en mi idioma preferido.
        -	Validación: La interfaz de usuario cambia al idioma seleccionado y mantiene la preferencia para futuras sesiones, mostrando todo el contenido en el idioma elegido.
    4.	Historia de Usuario 4: Funcionalidad de Chat para Soporte en Tiempo Real.
        -	Como: Usuario del sistema.
        -	Quiero: Utilizar una función de chat para obtener soporte en tiempo real.
        -	Para: Resolver rápidamente cualquier problema o duda sobre mis envíos.
        -	Validación: El sistema conecta al usuario con un representante de soporte en tiempo real, permite enviar y recibir mensajes, y guarda el historial de chat.
1. Técnicas utilizadas en los prompts:
-	Como entrada se le dió requerimientos clasificados en funcionales. Tanto de ejemplos de otros proyectos como para que los tenga de referencia, como los requerimientos nuestros que queremos que use.
-	Para indicarle la salida esperada, se le dió como ejemplo Historias de Usuario para los requerimientos mencionados anteriormente de otro proyecto, y una vez que conoció como queremos que arme las historias de usuario, que genere las correspondientes a nuestros requerimientos.
2. Estrategia para Contextualizar en los Diferentes Roles o Etapas: 
-	Product Owner: Este rol recibió los requerimientos iniciales del cliente y creó el Product Backlog, priorizando las historias de usuario.
-	Ejemplo de Prompt: "En el contexto de la metodología Scrum, actúa como Product Owner para el proyecto de desarrollo de una aplicación web para una empresa de logística."
-	Salida: Product Backlog con historias de usuario detalladas.
3. Resultados de Poca Calidad y Reflexión:
-	Las historias de usuario resultantes carecen de detalles específicos, lo que puede llevar a malentendidos durante el desarrollo. Por ejemplo, en el “Cómo” se podría haber identificado bien el rol del usuario. Además las validaciones pueden estar incompletas, poco detalladas o no cumplir con las reglas para considerarse un criterio de aceptación, por lo tanto las validaciones podrían quedar de la siguiente manera:  
    -	Historia de Usuario 1: Administración de Perfiles de Usuario:
        - El sistema permite editar los campos de información personal (nombre, correo electrónico, dirección, etc.).
        - Después de guardar los cambios, el sistema muestra una notificación de confirmación que indica "Información actualizada correctamente".
        - Los cambios realizados se reflejan inmediatamente en el perfil del usuario.
        - Los datos actualizados se verifican en la base de datos para asegurar que los cambios fueron guardados correctamente.
    -	Historia de Usuario 2: Notificaciones Automáticas sobre el Estado de los Envíos:
        - El sistema envía notificaciones automáticas en tiempo real cuando el estado del envío cambia a "Enviado", "En tránsito", "En reparto" y "Entregado".
        - Las notificaciones se envían dentro de los 5 minutos posteriores a cada cambio de estado.
        - El usuario puede configurar preferencias de notificación para recibir alertas por correo electrónico, SMS, y/o notificaciones push.
        - El sistema permite activar o desactivar cada tipo de notificación y esta preferencia se guarda para futuras sesiones.
    -	Historia de Usuario 3: Soporte para Múltiples Idiomas en la Interfaz de Usuario:
        - La interfaz de usuario cambia al idioma seleccionado inmediatamente después de que el usuario elige una opción del menú de idiomas.
        - La preferencia de idioma se guarda y se aplica automáticamente en las futuras sesiones del usuario.
        - Todo el contenido visible en la aplicación (menús, botones, mensajes, etc.) se muestra en el idioma seleccionado, y se verifica que no haya partes no traducidas.
        - El sistema realiza una comprobación de QA para asegurarse de que todas las cadenas de texto están correctamente traducidas.
    -	Historia de Usuario 4: Funcionalidad de Chat para Soporte en Tiempo Real:
        - El sistema conecta al usuario con un representante de soporte en tiempo real dentro de los primeros 30 segundos después de iniciar el chat.
        - El usuario puede enviar y recibir mensajes instantáneamente durante la sesión de chat.
        - El historial del chat se guarda automáticamente y está disponible para futuras referencias.
        - El sistema muestra un mensaje de confirmación "Conectado con soporte" una vez que el usuario está conectado con un representante.
-	Tal vez si se le agrega al prompt teoría sobre lo que hace el Scrum Master, podría arrojar resultados más acertados a lo que se busca con el proyecto. Además se le puede dar como entrada ciertas reglas sobre cómo queremos que arme las historias de usuario.
-	Se podrían haber dado un orden de prioridad a cada historia de usuario mediante el uso de story point, ya que es responsabilidad del Product Owner asegurarse de que exista una Product Backlog actualizado y priorizado.
-	Consideramos que faltaria como salida del sprint, no solo las historias de usuario, sino también el sprint goal, para así en la siguiente fase de sprint planning poder determinar con qué historias se van a trabajar para cumplir con la sprint goal al finalizar el sprint.

4. Mejoras se pueden hacer a los prompts y a su proceso de creación:
-	Prompt Original: "En el contexto de la metodología Scrum, actúa como Product Owner para el proyecto de desarrollo de una aplicación web para una empresa de logística.“
-	Prompt Mejorado: "En el contexto de la metodología Scrum, actúa como Product Owner (indico responsabilidades) para el proyecto de desarrollo de una aplicación web para una empresa de logística. La aplicación debe permitir a los usuarios administrar sus perfiles, recibir notificaciones automáticas sobre el estado de los envíos, soportar múltiples idiomas en la interfaz de usuario y proporcionar una funcionalidad de chat para soporte en tiempo real. Te encargaras de tomar cada uno de estos requerimientos y transformarlos en historias de usuario según los siguientes criterios: (ejemplos de historias de usuario con el formato y el nivel de detalle que queremos) “

- Número de prompt: 2.
- Rol que representa el prompt: Team Development.
- Entrada de información que recibe el prompt: Product Backlog.
- Prompt: Ahora tomarás el rol del equipo de desarrollo y deberás tomar la salida anterior (las historias de usuario) como entrada en esta fase de planificación de sprint basado en la metodología scrum. La salida ser un conjunto de tareas y el responsable de cada una.
- Resultado de ejecutar el prompt: plan del sprint con las siguientes tareas y responsables:
    -	Para la Administración de Perfiles de Usuario:
        -	Diseñar la interfaz de usuario para la administración de perfiles: Desarrollador A.
        -	Implementar la funcionalidad de edición de perfil: Desarrollador B
        -	Agregar validación de datos para los campos del perfil: Desarrollador C.
        -	Desarrollar notificaciones de confirmación tras la actualización del perfil: Desarrollador D.
        -	Realizar pruebas de integración para asegurar que la actualización del perfil se refleja en todas las áreas relevantes: Tester A.
    -	Para la Notificaciones Automáticas sobre el Estado de los Envíos:
        -	Diseñar la interfaz de usuario para la configuración de notificaciones: Desarrollador A.
        -	Implementar la funcionalidad de envío de notificaciones automáticas: Desarrollador B.
        -	Desarrollar opciones de configuración de notificaciones: Desarrollador C.
        -	Realizar pruebas de envío de notificaciones en diferentes escenarios: Tester B.
        -	Implementar la funcionalidad para que el usuario pueda desactivar o ajustar las preferencias de notificación: Desarrollador D.
    -	Para el Soporte para Múltiples Idiomas en la Interfaz de Usuario:
        -	Desarrollar la funcionalidad de selección de idioma en la interfaz de usuario: Desarrollador A.
        -	Implementar traducciones para los idiomas disponibles en la aplicación: Desarrollador B.
        -	Actualizar la interfaz de usuario para soportar cambios de idioma sin reiniciar la sesión: Desarrollador C.
        -	Asegurar que las preferencias de idioma se guardan y aplican en futuras sesiones del usuario: Desarrollador D.
        -	Realizar pruebas de usabilidad y precisión de las traducciones en diferentes idiomas: Tester A.
    -	Para la Funcionalidad de Chat para Soporte en Tiempo Real:
        -	Diseñar la interfaz de usuario para la funcionalidad de chat: Desarrollador A.
        -	Implementar la funcionalidad de chat en tiempo real: Desarrollador B.
        -	Desarrollar la funcionalidad para guardar y acceder al historial de chat: Desarrollador C.
        -	Implementar indicadores de disponibilidad de representantes de soporte: Desarrollador D.
        -	Realizar pruebas de funcionalidad y rendimiento del chat en tiempo real: Tester B
1. Técnicas utilizadas en los prompts:
    -	Separación de las historias de usuario en tareas más pequeñas y manejables
    -	Asignación de tareas a cada uno de los roles del equipo
2. Estrategia para Contextualizar en los Diferentes Roles o Etapas: 
    -	Team Development: El equipo de desarrollo tomó el Product Backlog y planificó el sprint, desglosando las historias de usuario en tareas específicas y asignando responsables.
    -	Ejemplo de Prompt: "Ahora tomarás el rol del equipo de desarrollo y deberás tomar la salida anterior (las historias de usuario) como entrada en esta fase de planificación de sprint."
    -	Salida: Plan del sprint con tareas detalladas y responsables asignados.
3. Resultados de Poca Calidad y Reflexión:
    -	Se podría haber asignado la prioridad que tiene cada tarea.
    -	Se podría haber implementado puntos de función para la estimación de costos en el proyectos.
    -	Indicar cuales van a ser los roles de nuestro equipo, así no los inventa.
    -	Indicar con teoría el rol del equipo de desarrollo en el contexto de Scrum.

4. Mejoras se pueden hacer a los prompts y a su proceso de creación:
    -	Prompt Original: "Ahora tomarás el rol del equipo de desarrollo y deberás tomar la salida anterior (las historias de usuario) como entrada en esta fase de planificación de sprint.“
    -	Prompt Mejorado: "En el contexto de la metodología Scrum, ahora asumirás el rol del equipo de desarrollo para el proyecto de una aplicación web para una empresa de logística. Tu objetivo es tomar las historias de usuario del Product Backlog proporcionadas y planificar el sprint, desglosando cada historia de usuario en tareas específicas y asignando responsables. Recuerda que el equipo de desarrollo en Scrum es multifuncional y trabaja colaborativamente para entregar incrementos funcionales del producto al final de cada sprint. Además deberás estimar el Tamaño del Proyecto Utilizando COSMIC de la siguiente monera:
        1.	Identificar las Interacciones Funcionales: Cada requerimiento funcional identificado en las historias de usuario al desglosarlas en tareas, estas serán las interacciones funcionales que tendrás que clasificar.
        2.	Clasificar las Interacciones Funcionales en: Pequeña (S), Mediana (M) y Grande (L).
        3.	Calcular el Tamaño Funcional: Asignarle a cada interacción la siguiente clasificación de tamaño y luego calcular el Tamaño Funcional Total(X) [PFC].
            a.	Si es Pequeña (S): 3 PFC.
            b.	Si es Mediana (M): 5 PFC.
            c.	Si es Grande (L): 7 PFC.
        4.	Obtener el Costo por Punto de Función:
            a.	 Costo mes del equipo: Dependerá del número de personas, remuneración de cada rol, otros gastos, margen de ganancia si es un proyecto para un tercero. Por ejemplo, el equipo tiene 5 personas con un costo mensual total de $20,000. [$]
            b.	Puntos de función del mes(W): Basado en proyectos pasados, podemos saber que el equipo de desarrollo de software produce N cantidad de puntos de función al mes [PFC/mes]. Por ejemplo, el equipo produce 25 PFC al mes.
            c.	Costo por punto de función(CPFC): CPFC = Costo mes del equipo / W [$/ PFC]
        5.	Calcular la Duración del Proyecto(A): A = X/W [Meses]
        6.	Estimar el Costo total del proyecto(B): B = X*CPFC [$]
            El equipo está compuesto por los siguientes roles:
            ●	Desarrollador A
            ●	Desarrollador B
            ●	Desarrollador C 
            ●	Desarrollador D
            ●	Tester A 
            ●	Tester B”

- Número de prompt: 3.
- Rol que representa el prompt: Scrum Master.
- Entrada de información que recibe el prompt: Plan del Sprint.
- Prompt: Una vez obtenido el plan del sprint, con sus tareas y responsable, deberás ponerte en el rol del Scrum Master para generar como salida la descripción del incremento de software funcional que el cliente espera al finalizar el spring, estos puntos de la descripción son los que el scrum master chequeará en los daily meeting para comprobar el estado de desarrollo del proyecto que lleva a cabo el team development.
- Resultado de ejecutar el prompt: Incremento de sofware funcional se espera que contemple las siguientes funcionalidades:
    -	Los usuarios deben poder actualizar su información personal de manera sencilla y segura.
    -	Los usuarios deben recibir notificaciones automáticas en tiempo real sobre el estado de sus envíos.
    -	Los usuarios deben poder seleccionar y utilizar la aplicación en su idioma preferido.
    -	Los usuarios deben poder acceder a soporte en tiempo real a través de un chat.
1. Técnicas utilizadas en los prompts:
    -	Al estar trabajando con scrum se implementaran dailys meetings, estas constan de preguntas que le hará el SM a los miembros del equipo de desarrollo para controlar la evolución del proyecto y que se estén aplicando correctamente las reglas del SCRUM.
2. Estrategia para Contextualizar en los Diferentes Roles o Etapas:
    -	Scrum Master: Este rol generó la descripción del incremento de software funcional esperado y facilitó las daily scrums para monitorear el progreso.
    -	Ejemplo de Prompt: "Una vez obtenido el plan del sprint con sus tareas y responsables, deberás ponerte en el rol del Scrum Master para generar la descripción del incremento de software funcional.“
    -	Salida: Descripción del incremento de software funcional y reporte de daily scrums.
3. Resultados de Poca Calidad y Reflexión:
    -	Creemos que el resultado es el correcto. Aunque tuvimos que quitar de los resultados esperados las descripciones paso a paso de cómo se tenían que hacer las tareas para lograr el incremento funcional. Esto es incorrecto ya que el scrum master no tiene esta responsabilidad. Es por esto que con mejora se le puede dar más contexto al prompt sobre lo que es ser SCrum master.
4. Mejoras se pueden hacer a los prompts y a su proceso de creación:
    -	Prompt Original: "Una vez obtenido el plan del sprint, con sus tareas y responsable, deberás ponerte en el rol del Scrum Master para generar como salida la descripción del incremento de software funcional que el cliente espera al finalizar el spring, estos puntos de la descripción son los que el scrum master chequeará en los daily meeting para comprobar el estado de desarrollo del proyecto que lleva a cabo el team development.“
    -	Prompt Mejorado: "En el contexto de la metodología Scrum, ahora asumirás el rol del Scrum Master para el proyecto de desarrollo de una aplicación web para una empresa de logística. Tu objetivo es tomar el plan del sprint, con sus tareas y responsables, y generar la descripción del incremento de software funcional que el cliente espera al finalizar el sprint. Como Scrum Master, tu rol incluye facilitar las daily scrums para monitorear el progreso del equipo de desarrollo y asegurar que se estén aplicando correctamente las reglas de Scrum. En cada daily meeting, verifica el estado de desarrollo de acuerdo a los criterios de aceptación y la definición de 'hecho' de cada tarea. Enfócate en identificar impedimentos y asegurarte de que el equipo esté alineado con los objetivos del sprint.”

- Número de prompt: 4.
- Rol que representa el prompt: Scrum Master.
- Entrada de información que recibe el prompt: incremento de software funcional.
- Prompt: Quiero que sigas con el rol de SCRUM Master y generes como salida de esta sprint review la retroalimentación del cliente (conocer la satisfacción del cliente y si existen nuevos requerimientos a implementar) y lecciones aprendidas (en qué aspectos mejorar en el desarrollo de este proyecto). Recordar que como entrada se han cumplido con el incremento de software funcional.
- Resultado de ejecutar el prompt: Conocer la satisfacción del cliente con el incremento de software funcional entregado y determinar si existen nuevos requerimientos a implementar.
    -	Retroalimentación del cliente:
        -	Satisfacción General: El cliente ha expresado una alta satisfacción con el incremento de software funcional entregado. Los usuarios han podido actualizar sus perfiles, recibir notificaciones automáticas, cambiar el idioma de la interfaz y acceder a soporte en tiempo real sin inconvenientes.
        -	 Comentarios Específicos:
            -	Administración de Perfiles de Usuario: Los usuarios han encontrado la interfaz de administración de perfiles intuitiva y fácil de usar. La validación de datos y las notificaciones de confirmación han funcionado como se esperaba.
            -	Notificaciones Automáticas: Las notificaciones en tiempo real han sido muy apreciadas, permitiendo a los usuarios mantenerse informados sobre el estado de sus envíos de manera eficiente.
            -	Soporte para Múltiples Idiomas: La capacidad de cambiar el idioma de la interfaz ha mejorado significativamente la usabilidad de la aplicación para usuarios de diferentes regiones.
            -	Funcionalidad de Chat: El chat en tiempo real ha sido una adición valiosa, facilitando la resolución rápida de problemas y consultas.
        -	Nuevos Requerimientos:
            -	El cliente sugiere agregar más opciones de personalización para las notificaciones, como la posibilidad de seleccionar qué eventos específicos desencadenan una notificación.
            -	El cliente solicita la integración con calendarios (por ejemplo, Google Calendar) para permitir a los usuarios programar recordatorios de eventos clave relacionados con sus envíos.
            -	Se ha pedido una funcionalidad para que los administradores puedan generar reportes sobre la actividad de los usuarios, incluyendo estadísticas de uso y comportamientos.
    -	Lecciones Aprendidas:
        -	Asegurarse de que todos los miembros del equipo tengan una comprensión clara de los requerimientos y expectativas del cliente desde el principio.
        -	Optimizar la gestión del tiempo para evitar retrasos en la entrega de tareas.
        -	Aumentar la rigurosidad de las pruebas antes de la entrega del incremento funcional.
        -	Mantener una mayor flexibilidad para adaptarse rápidamente a cambios o nuevos requerimientos del cliente.
        -	Mejorar la documentación del proyecto para asegurar que todos los cambios y decisiones estén claramente registrados.
1. Técnicas utilizadas en los prompts:
    -	Evaluación de satisfacción del cliente.
    -	Recolección de nuevos requerimientos.
    -	Identificación de lecciones aprendidas y áreas de mejora.
2. Estrategia para Contextualizar en los Diferentes Roles o Etapas:
    -	Feedback del Cliente: El Scrum Master recopiló la retroalimentación del cliente sobre el incremento de software entregado y las lecciones aprendidas.
    -	Ejemplo de Prompt: "Continuando en el rol de Scrum Master, genera la retroalimentación del cliente y las lecciones aprendidas tras la entrega del incremento de software funcional.“
    -	Salida: Retroalimentación del cliente y plan de mejora para el próximo sprint.
3. Resultados de Poca Calidad y Reflexión:
    -	Si bien se corrigió, hubo un error al usar el prompt original, en donde el ChatGpt confundida la daily meeting con el sprint review. Por lo tanto, como mejora del prompt se tendrá que dar contexto sobre la fase de sprint review.
    -	Consideramos que falta un prompt en donde el product owner se reuna con el cliente para mostrar las metas y objetivos cumplidos del sprint con el incremento de funcionalidad para luego redefinir el product backlog. En este prompt solamente se menciona al Scrum master,  este no tiene como responsabilidad interactuar con el cliente directamente, sino que está como intermediario del Product Owner y el Team Development.
4. Mejoras se pueden hacer a los prompts y a su proceso de creación:
    -	Prompt Original: “Quiero que sigas con el rol de SCRUM Master y generes como salida de esta sprint review la retroalimentación del cliente (conocer la satisfacción del cliente y si existen nuevos requerimientos a implementar) y lecciones aprendidas (en qué aspectos mejorar en el desarrollo de este proyecto). Recordar que como entrada se han cumplido con el incremento de software funcional.”
    -	Prompt Mejorado: “En el contexto de la metodología Scrum, ahora seguirás en el rol de Scrum Master y generarás la retroalimentación del cliente al finalizar esta sprint review. La sprint review es una reunión realizada al final del sprint en la que el equipo presenta el trabajo completado al Product Owner y otras partes interesadas. Esta revisión incluye una demostración del incremento de software funcional y una discusión sobre lo que se ha logrado en el sprint. Tu objetivo es obtener la satisfacción del cliente con el incremento de software funcional entregado, identificar cualquier nuevo requerimiento a implementar y documentar las lecciones aprendidas para mejorar en el desarrollo de este proyecto. Recuerda que como entrada se han cumplido con los objetivos del incremento de software funcional.”

- Número de prompt: 5.
- Rol que representa el prompt: Scrum Master.
- Entrada de información que recibe el prompt: Retroalimentación del cliente y lecciones aprendidas.
- Prompt: Continuando en el rol de scrum master se deberá, para esta fase de Sprint Retrospective, armar un plan de mejora para el próximo sprint, teniendo en cuenta las lecciones aprendidas y la retroalimentación del cliente.
- Resultado de ejecutar el prompt: Plan de mejora para el siguiente sprint:
    -	Mejoras en el Sistema de Notificaciones.
    -	Integración con Calendarios.
    -	Incorporar funcionalidad de reporte de actividad de usuarios.
    -	Lograr una Comunicación Efectiva.
    -	Mejora en la Gestión del Tiempo.
    -	Mejora en Pruebas y Validación.
    -	Mejora en Flexibilidad y Adaptación.
    -	Mejora en Documentación.
1. Técnicas utilizadas en los prompts:
    -	Análisis de retroalimentación del cliente.
    -	Identificación de áreas de mejora a partir de lecciones aprendidas.
    -	Planificación de acciones concretas y asignación de responsabilidades.
2. Estrategia para Contextualizar en los Diferentes Roles o Etapas:
    -	Scrum Master: Facilita la Sprint Retrospective y lidera la creación del plan de mejora, asegurándose de que las acciones propuestas se implementen en el próximo sprint.
3. Resultados de Poca Calidad y Reflexión:
    -	Creemos que en este prompt no se necesita mejoras. Pero como comentario a parte de mejora se podría implementar otros prompt para representar la interacción que tiene el product owner con el cliente cuando se le muestre el prototipo al finalizar el sprint y de esta manera redefinir el product backlog para el siguiente sprint. Esto es una oportunidad para mostrar el trabajo completado al cliente y a otros stakeholders.
4. Mejoras se pueden hacer a los prompts y a su proceso de creación:
    -	Prompt Original: “-”
    -	Prompt Mejorado: “-”
    -	Prompt Extra: “En el contexto de la metodología Scrum, ahora asumirás el rol de Product Owner para el proyecto de desarrollo de una aplicación web para una empresa de logística. Tu objetivo es interactuar con el cliente al finalizar el sprint, mostrando el incremento de software funcional completado y recopilando retroalimentación. Utiliza esta retroalimentación para redefinir y priorizar el Product Backlog para el siguiente sprint. La salida debe incluir los nuevos requerimientos y ajustes propuestos por el cliente, así como una versión actualizada del Product Backlog.”


5. Agente que utiliza a todos los prompt para que el trabajo se realice de forma automática y en una acción:
-	Prompt único: "En el contexto de la metodología Scrum, actúa como un agente multifuncional para un proyecto de desarrollo de una aplicación web para una empresa de logística. Tu objetivo es recibir los requerimientos del cliente y seguir todas las fases de Scrum, asumiendo los roles de Product Owner, Equipo de Desarrollo y Scrum Master, para completar el ciclo de desarrollo de software teniendo en cuenta las 5 ceremonias fundamentales de scrum:
    1.	El Sprint Planning al comienzo del Sprint
    2.	Daily Scrums a diario
    3.	Un Sprint Review al final del Sprint para inspeccionar el incremento realizado.
    4.	Y, finalmente, una Retrospectiva para inspeccionar el equipo y levantar mejoras que se apliquen en el siguiente Sprint.
    5.	Adicionalmente se ha incorporado también una reunión de Grooming o Refinement, que sirve para, dentro del Sprint, afinar y aclarar ciertas historias de usuario que pudieran quedar pendientes durante el Sprint Planning.
