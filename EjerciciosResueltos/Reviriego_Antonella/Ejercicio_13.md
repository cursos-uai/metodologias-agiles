# Ejercicio 13

## Enunciado:
Tu tarea es desarrollar una aplicación informática utilizando la técnica TDD para gestionar una cuenta bancaria. La aplicación debe permitir a los usuarios abrir una cuenta, realizar depósitos, hacer retiros y transferir fondos entre cuentas. A continuación se detallan las etapas de desarrollo utilizando TDD:

### Etapa 1: Especificación y prueba inicial

1. **Especifica los requisitos básicos del sistema y las funcionalidades clave**:
   - Apertura de cuenta bancaria: Permitir a los usuarios abrir una nueva cuenta bancaria con un saldo inicial de 0.
   - Depósito de fondos: Permitir a los usuarios depositar fondos en su cuenta bancaria.
   - Retiro de fondos: Permitir a los usuarios retirar fondos de su cuenta bancaria, asegurando que no se pueda retirar más de lo que está disponible en la cuenta.
   - Transferencia de fondos: Permitir a los usuarios transferir fondos entre cuentas bancarias, asegurando que las cuentas de origen tengan fondos suficientes y que las cuentas de destino existan.

2. **Escribe una prueba inicial que verifique si el sistema puede crear una instancia de una cuenta bancaria y obtener su saldo inicial**:
   - Verificar que se pueda crear una instancia de una cuenta bancaria.
   - Verificar que el saldo inicial de una nueva cuenta sea 0.

### Etapa 2: Desarrollo de las funcionalidades básicas

3. **Implementa la funcionalidad para abrir una cuenta bancaria**:
   - Confirmar que la creación de una cuenta bancaria con un saldo inicial de 0 sea exitosa.
   - Ejecuta la prueba y verifica que pase correctamente.

4. **Implementa la funcionalidad para realizar depósitos en una cuenta bancaria**:
   - Verificar que se puedan depositar fondos en una cuenta bancaria.
   - Confirmar que el saldo de la cuenta se actualice correctamente después de un depósito.
   - Ejecuta las pruebas y verifica que pasen correctamente.

5. **Implementa la funcionalidad para realizar retiros de una cuenta bancaria**:
   - Verificar que se puedan retirar fondos de una cuenta bancaria.
   - Asegurar que no se pueda retirar más de lo que está disponible en la cuenta.
   - Confirmar que el saldo de la cuenta se actualice correctamente después de un retiro.
   - Ejecuta las pruebas y verifica que pasen correctamente.

6. **Implementa la funcionalidad para transferir fondos entre cuentas bancarias**:
   - Verificar que se puedan transferir fondos de una cuenta bancaria a otra.
   - Asegurar que la cuenta de origen tenga fondos suficientes para la transferencia.
   - Confirmar que los saldos de ambas cuentas se actualicen correctamente después de una transferencia.
   - Ejecuta las pruebas y verifica que pasen correctamente.

### Etapa 3: Pruebas adicionales y mejoras

7. **Escribe pruebas adicionales para cubrir casos de prueba específicos**:
   - Verificar que no se pueda retirar más dinero del disponible en una cuenta.
   - Asegurar que no se puedan transferir fondos a una cuenta inexistente.
   - Confirmar que se manejen correctamente las excepciones y errores en casos específicos (como saldo insuficiente o cuentas no válidas).

8. **Ejecución de todas las pruebas**:
   - Ejecutar todas las pruebas desarrolladas para asegurar que todas las funcionalidades básicas y los casos específicos se comporten correctamente.

9. **Refactoriza tu código**:
   - Mejorar la estructura, legibilidad y eficiencia del código sin cambiar su comportamiento.
   - Confirmar que todas las pruebas continúen pasando después de la refactorización.

10. **Ejecución de todas las pruebas nuevamente**:
    - Verificar que el código refactorizado no haya introducido errores y que todas las pruebas pasen correctamente.

### Etapa 4: Cobertura completa de pruebas

11. **Asegúrate de que todas las funcionalidades del sistema estén cubiertas por pruebas automatizadas**:
    - Revisar y asegurar que todas las funcionalidades del sistema estén adecuadamente cubiertas por pruebas automatizadas.

12. **Examina los casos límite y situaciones excepcionales**:
    - Verificar que el sistema se comporte correctamente en todos los escenarios posibles, incluyendo casos límite y excepcionales.

13. **Ejecución de todas las pruebas y verificación final**:
    - Ejecutar todas las pruebas nuevamente para asegurarse de que el sistema cumpla con los requisitos establecidos y se comporte correctamente en todos los escenarios previstos.
