# Ejercicio 14 | TDD
---

## Etapa 1: Especificación y prueba inicial

### 1. Especificación de los requisitos básicos del sistema y funcionalidades claves.

1. Apertura de cuenta:
    - Permitir a los usuarios abrir una nueva cuenta bancaria.
    - Asignar un saldo inicial de 0 a la cuenta recién creada.
  
2. Depósito de fondos:
    - Permitir a los usuarios depositar una cantidad específica de dinero en su cuenta.
    - Incrementar el saldo de la cuenta en consecuencia.
  
3. Retiro de fondos:
    - Permitir a los usuarios retirar una cantidad específica de dinero de su cuenta.
    - Disminuir el saldo de la cuenta en consecuencia.
    - No permitir retiros que excedan el saldo disponible.
  
4. Transferencia de fondos:
    - Permitir a los usuarios transferir una cantidad específica de dinero de una cuenta a otra.
    - Disminuir el saldo de la cuenta de origen y aumentar el saldo de la cuenta de destino.
    - No permitir transferencias que excedan el saldo disponible en la cuenta de origen.

### 2. Prueba inicial

Verficar si el sistema puede crear una instancia de una cuenta bancaria y obtnener su saldo inicial.

1. Escribir la pruba inicial
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
```

2. Ejecutar la prueba inicial
```bash
$ python test_bank_account.py
```
Al ejecutar esta prueba, obtendremos un error porque la clase BankAccount aún no está definida. Esto es esperado en TDD.

3. Implementar el código para pasar la prueba
```python
class BankAccount:
    def __init__(self):
        self.balance = 0
    
    def get_balance(self):
        return self.balance

# Ahora ejecutamos nuevamente las pruebas
import unittest

class TestBankAccount(unittest.TestCase):
    def test_create_account(self):
        account = BankAccount()
        self.assertEqual(account.get_balance(), 0)

if __name__ == '__main__':
    unittest.main()
```

4. Verificamos que la prueba pase correctamente
```bash
$ python test_bank_account.py
```
Al ejecutar el script, la prueba debería pasar, indicando que la cuenta bancaria se crea correctamente con un saldo inicial de 0.

## Etapa 2: Desarrollo de las funcionalidades básicas

### 3. Implementa la funcionalidad para abrir una cuenta bancaria
- Prueba
```python
import unittest

class TestBankAccount(unittest.TestCase):
    def test_create_account(self):
        account = BankAccount()
        self.assertEqual(account.get_balance(), 0)

if __name__ == '__main__':
    unittest.main()
```
- Implementación
```python
class BankAccount:
    def __init__(self):
        self.balance = 0
    
    def get_balance(self):
        return self.balance
```
### 4. Implementa la funcionalidad para realizar depósitos en la cuenta
- Prueba
```python
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
```
- Implementación
```python
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
```
### 5. Implementa la funcionalidad para realizar retiros de la cuenta
- Prueba
```python
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
```
- Implementación
```python
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
```
### 6. Implementa la funcionalidad para transferir fondos entre cuentas
- Prueba
```python
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
```
- Implementación
```python
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
```
## Etapa 3: Pruebas adicionales y mejoras

### 7. Pruebas adicionales    
1. Intentar retirar más dinero del disponible en la cuenta
```python
def test_withdraw_more_than_balance(self):
    account = BankAccount()
    account.deposit(100)
    with self.assertRaises(ValueError):
        account.withdraw(150)
```
2. Intentar transferir fondos a una cuenta inexistente (No se puede representar directamente una cuenta inexistente)
```python
def test_transfer_to_non_existent_account(self):
    account1 = BankAccount()
    account1.deposit(100)
    with self.assertRaises(AttributeError):
        account1.transfer(None, 50)
```
### 8. Ejecutar las pruebas y verificar que pasen correctamente
```bash
python test_bank_account.py
```
### 9. Refactorizar el código si es necesario
Mejoras hechas:
1. Simplificación de las validaciones
2. Comentarios para una mayor claridad

```python
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
```
### 10. Ejecutar todas las pruebas nuevamente
```bash
python test_bank_account.py
```
## Etapa 4: Cobertura completa de pruebas

### 11. Asegurar que todas las funcionalidades del sistema estén cubiertas por pruebas automatizadas

Pruebas actuales:
    
   - Crear una cuenta bancaria
   - Depositar fondos
   - Retirar fondos
   - Transferir fondos
   - Casos excepcionales (retirar más de lo disponible, transferir a cuenta inexistente)

### 12. Examinar los casos límite y situaciones excepcionales

Se agregan algunas pruebas para casos límite y situaciones excepcionales

1. Depositar una cantidad negativa o cero
```python
def test_deposit_zero_or_negative(self):
    account = BankAccount()
    with self.assertRaises(ValueError):
        account.deposit(0)
    with self.assertRaises(ValueError):
        account.deposit(-50)
```
2. Retirar una cantidad negativa o cero
```python
def test_withdraw_zero_or_negative(self):
    account = BankAccount()
    with self.assertRaises(ValueError):
        account.withdraw(0)
    with self.assertRaises(ValueError):
        account.withdraw(-50)
```
3. Transferir una cantidad negativa o cero
```python
def test_transfer_zero_or_negative(self):
    account1 = BankAccount()
    account2 = BankAccount()
    with self.assertRaises(ValueError):
        account1.transfer(account2, 0)
    with self.assertRaises(ValueError):
        account1.transfer(account2, -50)
```
4. Transferir más fondos de los disponibles
```python
def test_transfer_more_than_balance(self):
    account1 = BankAccount()
    account2 = BankAccount()
    account1.deposit(100)
    with self.assertRaises(ValueError):
        account1.transfer(account2, 150)
```

### 13. Ejecutar todas las pruebas y verificar que pasen correctamente

Código completo final con todas las pruebas
```python
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
            account.deposit(-50)

    def test_withdraw_zero_or_negative(self):
        account = BankAccount()
        with self.assertRaises(ValueError):
            account.withdraw(0)
        with self.assertRaises(ValueError):
            account.withdraw(-50)

    def test_transfer_zero_or_negative(self):
        account1 = BankAccount()
        account2 = BankAccount()
        with self.assertRaises(ValueError):
            account1.transfer(account2, 0)
        with self.assertRaises(ValueError):
            account1.transfer(account2, -50)

    def test_transfer_more_than_balance(self):
        account1 = BankAccount()
        account2 = BankAccount()
        account1.deposit(100)
        with self.assertRaises(ValueError):
            account1.transfer(account2, 150)

if __name__ == '__main__':
    unittest.main()
```

Ejecutar todas las pruebas
```bash
python test_bank_account.py
```