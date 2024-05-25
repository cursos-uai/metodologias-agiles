Ejercicio 13 - TDD:
Enunciado:
Tu tarea es desarrollar una aplicación informática utilizando la técnica TDD para gestionar una cuenta bancaria. La aplicación debe permitir a los usuarios abrir una cuenta, realizar depósitos, hacer retiros y transferir fondos entre cuentas. A continuación, se detallan las etapas de desarrollo utilizando TDD:

Etapa 1: Especificación y prueba inicial 1.
1. Especifica los requisitos básicos del sistema y las funcionalidades clave, como la apertura de cuenta, depósito de fondos retiro de fondos y transferencia de fondos. 
2. Escribe una prueba inicial que verifique si el sistema puede crear una instancia de una cuenta bancaria y obtener su saldo inicial.

Etapa 2: Desarrollo de las funcionalidades básicas
3. Implementa la funcionalidad para abrir una cuenta bancaria, asegurándote de que se cumplan los requisitos especificados. Ejecuta la prueba y verifica que pase correctamente. 
4. Implementa la funcionalidad para realizar depósitos en una cuenta bancaria. Ejecuta las pruebas y verifica que pasen correctamente.
5. Implementa la funcionalidad para realizar retiros de una cuenta bancaria. Ejecuta las pruebas y verifica que pasen correctamente.
6. Implementa la funcionalidad para transferir fondos entre cuentas bancarias. Ejecuta las pruebas y verifica que pasen correctamente.

Etapa 3: Pruebas adicionales y mejoras
7. Escribe pruebas adicionales para cubrir casos de prueba específicos, como intentar retirar más dinero del disponible en una cuenta o transferir fondos a una cuenta inexistente.
8. Ejecuta todas las pruebas y verifica que pasen correctamente.
9. Refactoriza tu código si es necesario para mejorar su estructura, legibilidad y eficiencia.
10. Ejecuta todas las pruebas nuevamente para asegurarte de que el código refactorizado no haya introducido errores.

Etapa 4: Cobertura completa de pruebas
11. Asegúrate de que todas las funcionalidades del sistema estén cubiertas por pruebas automatizadas.
12. Examina los casos límite y situaciones excepcionales para garantizar que el sistema se comporte correctamente en todos los escenarios.
13. Ejecuta todas las pruebas y verifica que pasen correctamente.

Nota: Se abordará la actividad desde un enfoque teórico relacionado a TDD, ya que no se pide codificación. Se hará un resumen de las etapas que pide el enunciado junto con las 3 fases de la práctica de desarrollo mencionada.

Etapa 1: Especificación y prueba inicial 1.
1.	Funcionalidad: 
a.	Apertura de cuenta:
i.	Requisitos funcionales:
1.	El sistema debe permitir que un cliente se registre proporcionando su información personal, como nombre, apellido, dirección y documento de identidad.
2.	El sistema debe generar automáticamente un número de cuenta único para el cliente.
3.	El Sistema deberá solicitarle al cliente que debe realizar un depósito inicial mínimo especificado por el banco para activar la cuenta.
ii.	Requisitos no funcionales:
1.	El sistema debe cumplir con estándares de seguridad para proteger la información del cliente y prevenir posibles fraudes.
2.	El proceso de apertura de cuenta debe ser rápido y eficiente para proporcionar una buena experiencia al cliente.
3.	El sistema debe ser capaz de manejar un gran número de solicitudes de apertura de cuenta simultáneas sin degradación del rendimiento.

b.	Depósito de fondos:
i.	Requisitos funcionales:
1.	El sistema debe permitir que el usuario pueda seleccionar la cuenta bancaria a la cual desea realizar el depósito de fondos.
2.	El sistema deberá registrar el monto que el usuario desee depositar en la cuenta seleccionada.
3.	El sistema deberá mostrar en pantalla una confirmación al usuario para que pueda verificar y confirmar el depósito.
ii.	Requisitos no funcionales:
1.	El sistema debe estar disponible las 24 horas del día, los 7 días de la semana, para permitir a los usuarios realizar depósitos en cualquier momento.
2.	Se deben implementar medidas de seguridad en el sistema para garantizar la integridad de los datos durante el proceso de depósito de fondos y evitar posibles errores o pérdidas de información.
3.	El sistema debe ser capaz de registrar todas las transacciones de depósito de fondos realizadas, incluyendo detalles como la fecha, la hora y el monto depositado.

c.	Retiro de fondos:
i.	Requisitos funcionales:
1.	El sistema deberá permitir al usuario seleccionar la cuenta desde la cual desea retirar fondos.
2.	El sistema deberá solicitar al usuario ingresar el monto que desea retirar de la cuenta seleccionada.
3.	El sistema deberá verificar que el saldo disponible en la cuenta sea suficiente para realizar el retiro solicitado antes de procesar la transacción.
ii.	Requisitos no funcionales:
1.	El sistema deberá garantizar la seguridad de la transacción mediante la autenticación del usuario y la validación de la solicitud de retiro.
2.	El sistema deberá mantener un registro de todas las transacciones de retiro de fondos realizadas, incluyendo detalles como la fecha, la hora y el monto retirado, con fines de auditoría y seguimiento.
3.	El sistema deberá proporcionar una respuesta rápida y confirmación al usuario después de realizar un retiro de fondos, asegurando una experiencia fluida y sin demoras.

d.	Transferencia de fondos:
i.	Requisitos funcionales:
1.	El sistema deberá permitir al usuario seleccionar la cuenta de destino a la cual desea transferir fondos.
2.	El sistema deberá solicitar al usuario ingresar el monto que desea transferir de la cuenta de origen a la cuenta de destino.
3.	El sistema deberá verificar que el saldo disponible en la cuenta de origen sea suficiente para realizar la transferencia solicitada antes de procesar la transacción.
ii.	Requisitos no funcionales:
1.	El sistema deberá garantizar la seguridad de la transacción mediante la autenticación del usuario y la validación de la solicitud de transferencia.
2.	El sistema deberá mantener un registro detallado de todas las transferencias de fondos realizadas, incluyendo información sobre las cuentas involucradas, la fecha, la hora y el monto transferido, con fines de auditoría y seguimiento.
3.	El sistema deberá procesar las transferencias de fondos de manera rápida y eficiente, minimizando cualquier tiempo de espera o demoras en la confirmación de la transacción para proporcionar una experiencia de usuario satisfactoria.

2.	En esta prueba inicial se pide nomás que se verifique si el sistema puede crear una instancia de una cuenta bancaria y obtener su saldo inicial. 

Etapa 2: Desarrollo de las funcionalidades básicas
3.	a  6. En esta etapa, al estar usando TDD, se tendrá que ir haciendo una prueba por cada funcionalidad básica que se agregue, teniendo en cuenta que la implementación del códice todavía no se llevó a cabo, la prueba va a fallar. Esta funcionalidad se encontrará en la fase roja ya que se esperaba que falle, y para pasar a la prueba verde, se implementara el código justo y necesario, según los requerimientos del cliente, para que la prueba pase. 

Etapa 3: Pruebas adicionales y mejoras
7. a 8. Al igual que la etapa 2 cada nueva funcionalidad que se implemente también deberá ser probadas. Una vez que pasen todas las prueba se podrá evaluar si es necesario refactorizar el código ya que en la fase anterior consideramos que está “sucio” y que podríamos aplicar algunas reglas básicas de diseño para mejorar su estructura, legibilidad y eficiencia. Refactorizar puede que no sea necesario, en caso de serlo se tendrá que ejecutar pruebas automatizadas para verificar que todo sigue funcionando.

Etapa 4: Cobertura completa de pruebas
11. a 13 Una vez que se encuentran implementadas todas las funcionalidades del sistema, según los requisitos del cliente, y se tenga cubierta cada una con una prueba. Se deberá garantizar que el sistema se comporte correctamente en todos los escenarios posibles mediante más pruebas que se deberán ejecutar y pasar correctamente.
