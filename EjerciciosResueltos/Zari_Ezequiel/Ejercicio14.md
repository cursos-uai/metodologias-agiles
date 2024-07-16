# Etapa 1: Especificación y Prueba Inicial

## 1. Especificación de los Requisitos Básicos del Sistema y Funcionalidades Claves

### Apertura de Cuenta:
- Permitir a los usuarios registrar una nueva cuenta bancaria.
- Asignar un saldo inicial de 0 a la cuenta recién creada.

### Depósito de Fondos:
- Permitir a los usuarios ingresar una cantidad específica de dinero en su cuenta.
- Incrementar el saldo de la cuenta en consecuencia.

### Retiro de Fondos:
- Permitir a los usuarios retirar una cantidad específica de dinero de su cuenta.
- Disminuir el saldo de la cuenta en consecuencia.
- No permitir retiros que excedan el saldo disponible.

### Transferencia de Fondos:
- Permitir a los usuarios transferir una cantidad específica de dinero de una cuenta a otra.
- Disminuir el saldo de la cuenta de origen y aumentar el saldo de la cuenta de destino.
- No permitir transferencias que excedan el saldo disponible en la cuenta de origen.

## 2. Prueba Inicial

Verificar si el sistema puede crear una instancia de una cuenta bancaria y obtener su saldo inicial.



```python
import unittest

class TestBankAccount(unittest.TestCase):
    def test_create_account(self):
        # Crear una instancia de la cuenta bancaria
        account = BankAccount()
        # Verificar que el saldo inicial sea 0
        self.assertEqual(account.get_balance(), 0)

if __name__ == '__main__':
    unittest.main()

Ejecucion prueba inicial.

$ python test_bank_account.py


# Etapa 2: Desarrollo de las Funcionalidades Básicas

## 3. Implementa la Funcionalidad para Abrir una Cuenta Bancaria

### Prueba

```python
import unittest

class TestBankAccount(unittest.TestCase):
    def test_create_account(self):
        account = BankAccount()
        self.assertEqual(account.get_balance(), 0)

if __name__ == '__main__':
    unittest.main()

Implementación

class BankAccount:
    def __init__(self):
        self.balance = 0
    
    def get_balance(self):
        return self.balance

## 4. Implementa la Funcionalidad para Realizar Depósitos en la Cuenta
Prueba

class TestBankAccount(unittest.TestCase):
    def test_create_account(self):
        account = BankAccount()
        self.assertEqual(account.get_balance(), 0)

    # Nueva prueba para depositar fondos
    def test_deposit_funds(self):
        account = BankAccount()
        account.deposit(100)
        self.assertEqual(account.get_balance(), 100)

if __name__ == '__main__':
    unittest.main()

### Implementación

class BankAccount:
    def __init__(self):
        self.balance = 0
    
    def get_balance(self):
        return self.balance

    def deposit(self, amount):
        if amount > 0:
            self.balance += amount
        else:
            raise ValueError("Deposit amount must be positive")

import unittest

class TestBankAccount(unittest.TestCase):
    def test_create_account(self):
        account = BankAccount()
        self.assertEqual(account.get_balance(), 0)

    def test_deposit_funds(self):
        account = BankAccount()
        account.deposit(100)
        self.assertEqual(account.get_balance(), 100)

if __name__ == '__main__':
    unittest.main()

## 5. Implementa la Funcionalidad para Realizar Retiros de la Cuenta

- Prueba

class TestBankAccount(unittest.TestCase):
    def test_create_account(self):
        account = BankAccount()
        self.assertEqual(account.get_balance(), 0)

    def test_deposit_funds(self):
        account = BankAccount()
        account.deposit(100)
        self.assertEqual(account.get_balance(), 100)

    # Nueva prueba para retirar fondos
    def test_withdraw_funds(self):
        account = BankAccount()
        account.deposit(100)
        account.withdraw(50)
        self.assertEqual(account.get_balance(), 50)

        # Verificar que no se puede retirar más de lo que hay en la cuenta
        with self.assertRaises(ValueError):
            account.withdraw(100)

if __name__ == '__main__':
    unittest.main()

- Implementación
class BankAccount:
    def __init__(self):
        self.balance = 0
    
    def get_balance(self):
        return self.balance

    def deposit(self, amount):
        if amount > 0:
            self.balance += amount
        else:
            raise ValueError("Deposit amount must be positive")

    def withdraw(self, amount):
        if amount > 0:
            if self.balance >= amount:
                self.balance -= amount
            else:
                raise ValueError("Insufficient funds")
        else:
            raise ValueError("Withdrawal amount must be positive")

import unittest

class TestBankAccount(unittest.TestCase):
    def test_create_account(self):
        account = BankAccount()
        self.assertEqual(account.get_balance(), 0)

    def test_deposit_funds(self):
        account = BankAccount()
        account.deposit(100)
        self.assertEqual(account.get_balance(), 100)

    def test_withdraw_funds(self):
        account = BankAccount()
        account.deposit(100)
        account.withdraw(50)
        self.assertEqual(account.get_balance(), 50)
        
        with self.assertRaises(ValueError):
            account.withdraw(100)

if __name__ == '__main__':
    unittest.main()


## 6. Implementa la Funcionalidad para Transferir Fondos entre Cuentas

Prueba
class TestBankAccount(unittest.TestCase):
    def test_create_account(self):
        account = BankAccount()
        self.assertEqual(account.get_balance(), 0)

    def test_deposit_funds(self):
        account = BankAccount()
        account.deposit(100)
        self.assertEqual(account.get_balance(), 100)

    def test_withdraw_funds(self):
        account = BankAccount()
        account.deposit(100)
        account.withdraw(50)
        self.assertEqual(account.get_balance(), 50)
        
        with self.assertRaises(ValueError):
            account.withdraw(100)

    # Nueva prueba para transferir fondos
    def test_transfer_funds(self):
        account1 = BankAccount()
        account2 = BankAccount()
        account1.deposit(100)
        account1.transfer(account2, 50)
        self.assertEqual(account1.get_balance(), 50)
        self.assertEqual(account2.get_balance(), 50)

        # Verificar que no se pueda transferir más de lo que hay en la cuenta
        with self.assertRaises(ValueError):
            account1.transfer(account2, 100)

if __name__ == '__main__':
    unittest.main()

- Implementación

class BankAccount:
    def __init__(self):
        self.balance = 0
    
    def get_balance(self):
        return self.balance

    def deposit(self, amount):
        if amount > 0:
            self.balance += amount
        else:
            raise ValueError("Deposit amount must be positive")

    def withdraw(self, amount):
        if amount > 0:
            if self.balance >= amount:
                self.balance -= amount
            else:
                raise ValueError("Insufficient funds")
        else:
            raise ValueError("Withdrawal amount must be positive")

    def transfer(self, target_account, amount):
        if amount > 0:
            if self.balance >= amount:
                self.withdraw(amount)
                target_account.deposit(amount)
            else:
                raise ValueError("Insufficient funds to transfer")
        else:
            raise ValueError("Transfer amount must be positive")

import unittest

class TestBankAccount(unittest.TestCase):
    def test_create_account(self):
        account = BankAccount()
        self.assertEqual(account.get_balance(), 0)

    def test_deposit_funds(self):
        account = BankAccount()
        account.deposit(100)
        self.assertEqual(account.get_balance(), 100)

    def test_withdraw_funds(self):
        account = BankAccount()
        account.deposit(100)
        account.withdraw(50)
        self.assertEqual(account.get_balance(), 50)
        
        with self.assertRaises(ValueError):
            account.withdraw(100)

    def test_transfer_funds(self):
        account1 = BankAccount()
        account2 = BankAccount()
        account1.deposit(100)
        account1.transfer(account2, 50)
        self.assertEqual(account1.get_balance(), 50)
        self.assertEqual(account2.get_balance(), 50)

        with self.assertRaises(ValueError):
            account1.transfer(account2, 100)

if __name__ == '__main__':
    unittest.main()


# Etapa 3: Pruebas Adicionales y Mejoras

## 7. Escribe Pruebas Adicionales

### Intentar Retirar más Dinero del Disponible en la Cuenta

def test_withdraw_more_than_balance(self):
    account = BankAccount()
    account.deposit(100)
    with self.assertRaises(ValueError):
        account.withdraw(150)

Intentar Transferir Fondos a una Cuenta Inexistente (No se puede representar directamente una cuenta inexistente)
def test_transfer_to_non_existent_account(self):
    account1 = BankAccount()
    account1.deposit(100)
    with self.assertRaises(AttributeError):
        account1.transfer(None, 50)

## 8. Ejecuta las Pruebas y Verifica que Pasen Correctamente

$ python test_bank_account.py


## 9. Refactoriza tu Código si es Necesario

### Mejoras Hechas:

- Simplificación de las validaciones
- Comentarios para una mayor claridad
- Código Refactorizado

class BankAccount:
    def __init__(self):
        # Inicializa el saldo de la cuenta a 0
        self.balance = 0
    
    def get_balance(self):
        # Retorna el saldo actual de la cuenta
        return self.balance

    def deposit(self, amount):
        # Deposita una cantidad en la cuenta
        # Verifica que la cantidad a depositar sea positiva
        if amount <= 0:
            raise ValueError("Deposit amount must be positive")
        # Incrementa el saldo de la cuenta con la cantidad depositada
        self.balance += amount

    def withdraw(self, amount):
        # Retira una cantidad de la cuenta
        # Verifica que la cantidad a retirar sea positiva
        if amount <= 0:
            raise ValueError("Withdrawal amount must be positive")
        # Verifica que haya fondos suficientes para retirar
        if self.balance < amount:
            raise ValueError("Insufficient funds")
        # Disminuye el saldo de la cuenta con la cantidad retirada
        self.balance -= amount

    def transfer(self, target_account, amount):
        # Transfiere una cantidad a otra cuenta bancaria
        # Verifica que la cuenta de destino sea una instancia de BankAccount
        if not isinstance(target_account, BankAccount):
            raise AttributeError("Target account must be a BankAccount instance")
        # Verifica que la cantidad a transferir sea positiva
        if amount <= 0:
            raise ValueError("Transfer amount must be positive")
        # Realiza el retiro de fondos de la cuenta actual
        self.withdraw(amount)
        # Realiza el depósito de fondos en la cuenta de destino
        target_account.deposit(amount)

## 10. Ejecuta Todas las Pruebas Nuevamente
$ python test_bank_account.py


# Etapa 4: Cobertura completa de pruebas
## 11. Asegurar que todas las funcionalidades del sistema estén cubiertas por pruebas automatizadas

-Pruebas actuales:

-Crear una cuenta bancaria
-Depositar fondos
-Retirar fondos
-Transferir fondos
-Casos excepcionales (retirar más de lo disponible, transferir a cuenta inexistente)
## 12. Examinar los casos límite y situaciones excepcionales

- Agregar pruebas para los casos límite y excepcionales

import unittest

class BankAccount:
    def __init__(self):
        self.balance = 0
    
    def get_balance(self):
        return self.balance

    def deposit(self, amount):
        if amount <= 0:
            raise ValueError("El monto del depósito debe ser positivo")
        self.balance += amount

    def withdraw(self, amount):
        if amount <= 0:
            raise ValueError("El monto del retiro debe ser positivo")
        if self.balance < amount:
            raise ValueError("Fondos insuficientes")
        self.balance -= amount

    def transfer(self, target_account, amount):
        if amount <= 0:
            raise ValueError("El monto de la transferencia debe ser positivo")
        if self.balance < amount:
            raise ValueError("Fondos insuficientes para transferir")
        self.withdraw(amount)
        target_account.deposit(amount)

class TestBankAccount(unittest.TestCase):
    def test_create_account(self):
        # Crear una cuenta bancaria y verificar que el saldo inicial es 0
        account = BankAccount()
        self.assertEqual(account.get_balance(), 0)

    def test_deposit_funds(self):
        # Depositar fondos y verificar que el saldo se actualiza correctamente
        account = BankAccount()
        account.deposit(100)
        self.assertEqual(account.get_balance(), 100)

    def test_withdraw_funds(self):
        # Retirar fondos y verificar que el saldo se actualiza correctamente
        account = BankAccount()
        account.deposit(100)
        account.withdraw(50)
        self.assertEqual(account.get_balance(), 50)
        
        # Verificar que retirar más de lo disponible lanza un error
        with self.assertRaises(ValueError):
            account.withdraw(100)

    def test_transfer_funds(self):
        # Transferir fondos entre cuentas y verificar los saldos
        account1 = BankAccount()
        account2 = BankAccount()
        account1.deposit(100)
        account1.transfer(account2, 50)
        self.assertEqual(account1.get_balance(), 50)
        self.assertEqual(account2.get_balance(), 50)

        # Verificar que transferir más de lo disponible lanza un error
        with self.assertRaises(ValueError):
            account1.transfer(account2, 100)

    def test_withdraw_more_than_balance(self):
        # Verificar que retirar más de lo disponible lanza un error
        account = BankAccount()
        account.deposit(100)
        with self.assertRaises(ValueError):
            account.withdraw(150)

    def test_transfer_to_non_existent_account(self):
        # Verificar que transferir a una cuenta inexistente lanza un error
        account1 = BankAccount()
        account1.deposit(100)
        with self.assertRaises(AttributeError):
            account1.transfer(None, 50)

    def test_deposit_zero_or_negative(self):
        # Depositar una cantidad negativa o cero
        account = BankAccount()
        with self.assertRaises(ValueError):
            account.deposit(0)
        with self.assertRaises(ValueError):
            account.deposit(-10)

    def test_withdraw_zero_or_negative(self):
        # Retirar una cantidad negativa o cero
        account = BankAccount()
        with self.assertRaises(ValueError):
            account.withdraw(0)
        with self.assertRaises(ValueError):
            account.withdraw(-20)

    def test_transfer_zero_or_negative(self):
        # Transferir una cantidad negativa o cero
        account1 = BankAccount()
        account2 = BankAccount()
        with self.assertRaises(ValueError):
            account1.transfer(account2, 0)
        with self.assertRaises(ValueError):
            account1.transfer(account2, -30)

    def test_transfer_more_than_balance(self):
        # Transferir más fondos de los disponibles
        account1 = BankAccount()
        account2 = BankAccount()
        account1.deposit(200)
        with self.assertRaises(ValueError):
            account1.transfer(account2, 300)

if __name__ == '__main__':
    unittest.main()


## 13. Ejecutar todas las pruebas y verificar que pasen correctamente

### Código completo final con todas las pruebas
import unittest

class BankAccount:
    def __init__(self):
        self.balance = 0
    
    def get_balance(self):
        return self.balance

    def deposit(self, amount):
        if amount <= 0:
            raise ValueError("El monto del depósito debe ser positivo")
        self.balance += amount

    def withdraw(self, amount):
        if amount <= 0:
            raise ValueError("El monto del retiro debe ser positivo")
        if self.balance < amount:
            raise ValueError("Fondos insuficientes")
        self.balance -= amount

    def transfer(self, target_account, amount):
        if amount <= 0:
            raise ValueError("El monto de la transferencia debe ser positivo")
        if self.balance < amount:
            raise ValueError("Fondos insuficientes para transferir")
        self.withdraw(amount)
        target_account.deposit(amount)

class TestBankAccount(unittest.TestCase):
    def test_create_account(self):
        account = BankAccount()
        self.assertEqual(account.get_balance(), 0)

    def test_deposit_funds(self):
        account = BankAccount()
        account.deposit(100)
        self.assertEqual(account.get_balance(), 100)

    def test_withdraw_funds(self):
        account = BankAccount()
        account.deposit(100)
        account.withdraw(50)
        self.assertEqual(account.get_balance(), 50)
        
        with self.assertRaises(ValueError):
            account.withdraw(100)

    def test_transfer_funds(self):
        account1 = BankAccount()
        account2 = BankAccount()
        account1.deposit(100)
        account1.transfer(account2, 50)
        self.assertEqual(account1.get_balance(), 50)
        self.assertEqual(account2.get_balance(), 50)

        with self.assertRaises(ValueError):
            account1.transfer(account2, 100)

    def test_withdraw_more_than_balance(self):
        account = BankAccount()
        account.deposit(100)
        with self.assertRaises(ValueError):
            account.withdraw(150)

    def test_transfer_to_non_existent_account(self):
        account1 = BankAccount()
        account1.deposit(100)
        with self.assertRaises(AttributeError):
            account1.transfer(None, 50)

    def test_deposit_zero_or_negative(self):
        account = BankAccount()
        with self.assertRaises(ValueError):
            account.deposit(0)
        with self.assertRaises(ValueError):
            account.deposit(-10)

    def test_withdraw_zero_or_negative(self):
        account = BankAccount()
        with self.assertRaises(ValueError):
            account.withdraw(0)
        with self.assertRaises(ValueError):
            account.withdraw(-20)

    def test_transfer_zero_or_negative(self):
        account1 = BankAccount()
        account2 = BankAccount()
        with self.assertRaises(ValueError):
            account1.transfer(account2, 0)
        with self.assertRaises(ValueError):
            account1.transfer(account2, -30)

    def test_transfer_more_than_balance(self):
        account1 = BankAccount()
        account2 = BankAccount()
        account1.deposit(200)
        with self.assertRaises(ValueError):
            account1.transfer(account2, 300)

if __name__ == '__main__':
    unittest.main()


### Ejecutar todas las pruebas
$ python test_bank_account.py
