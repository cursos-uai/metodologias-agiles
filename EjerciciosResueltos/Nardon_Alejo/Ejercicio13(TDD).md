## Ejercicio 13 - TDD


### Etapa 1

1).

Requisitos básicos de la aplicación bancaria, esta deberá: 

- Permitir a los usuarios poder registrar una cuenta e iniciar sesión
- Una vez dentro del sistema, el usuario podrá:
    - Consultar saldo
    - Realizar un depósito
    - Hacer retiros de montos que no superen al saldo
    - Transferir saldo entre cuentas, para enviar dinero a otra cuenta la cantidad del dinero deberá ser igual o menor al saldo disponible.



2).
```
Función test_crear_cuenta (datos){
		Verificar si datos del usuario son correctos
		Verificar datos de usuario únicos 
		Verificar si realizo depósito inicial
		Sí realizo depósito
				Verificar el monto del saldo inicial = al depósito
		Si no 
				Verificar que el depósito inicial sea igual a 0
	
}
Función test_deposito(){
		Verificar saldo inicial 
		Verificar que todos los datos del depósito fueron correctos
		Verificar que el monto del depósito sea mayor a 0 
		Verificar que el saldo actual deberá ser mayor al saldo inicial 
}

Función test_retiro(){
		Verificar saldo inicial 
		Verificar que todos los datos del depósito fueron correctos
		Verificar que el monto del depósito sea mayor a 0 
		Verificar que el saldo actual deberá ser mayor al saldo inicial 
}
Función test_tranferir_fondo(){
		Verificar saldo inicial
		verificar que la cuenta a transferir sea válida
		verificar que el monto a transferir sea ≤ al saldo
		verificar que la transferencia ha llegado 
		Verificar que el saldo sea igual al saldo inicial - monto transferido
}
```
### Etapa 2 
3).
```
Función crear_cuenta(){
		Solicitar datos de la persona
		verificar que los datos sean correctos
		verificar que no esté previamente registrado
		Consultar si desea realizar un depósito inicial
		Si
				ingresar monto del depósito
				saldo inicial = monto depositado
		Si no 
				saldo inicial = 0
}
```
4).
```
Función depósito(){
		Verificar que el usuario se haya identificado
		Solicitar monto a depositar
		Verificar que el monto sea válido
		Solicitar el depósito
		Verificar que el depósito sea igual al monto introducido
		saldo  = saldo inicial + monto depositado
}
```
5).
```
Función retiro(){
		Verificar que el usuario se haya identificado
		solicitar monto a retirar
		Verificar que el monto a retirar sea menor o igual al saldo inicial
		Entregar el dinero
		saldo = saldo inicial - monto retirado
}
```
6).
```
Función tranferir_fondos(){
		Verificar que el usuario se haya identificado
		solicitar cuenta a transferir dinero
		Verificar que la cuenta sea válida
		solicitar monto a transferir
		Verificar que el monto a transferir sea ≤ saldo inicial 
		Transferir dinero 
		saldo (cuenta usuario) = saldo inicial - monto transferido
		saldo (cuenta a transferir) = saldo inicial (cuenta a transferir) + monto transferido 
}
```
7).
```
funcion test_monto_retirar(saldoInicial, montoRetirar){
    if (montoRetirar≤ saldoInicial){
        return true
    }else{
        return false
    }
}

funcion test_cuenta_valida(datosCuenta){
    if (Cuentas.includes(datosCuenta) ){
        return true
    }else{
        return false
    }
}
```

8). Las pruebas pasan correctamente.


9). 
**Refactorización**
```

Función crear_cuenta(){
    datosCuentaNueva = Input (”ingresa tus datos”)
    if(verificarDatos(datosCuentaNueva)){
        if (Cuentas.includes(datosCuenta) ){
            dep= Input (”Desea ingresar un depósito”)
            if(dep){
                SaldoInicial = input (”Ingrese el monto del deposito”)
            }else{
                saldoInicial = 0
            }
        } else return false
    } else return false
}

Función depósito(){
		if(SesionIniciada()){
				saldo =Saldo()
				montoDepositar = input (”Ingrese el monto del deposito:”)
				if(montoDepositar>0){
						NuevoSaldo(saldo += montoDespositar)
				}else return false
		} else return false
}
Función retiro(){
		if(SesionIniciada()){
				saldoInicial=Saldo()
				montoRetirar= input (”Ingrese el monto a retirar:”)
				if(montoRetirar<=saldoInicial AND montoRetirar>0){
						entregaDinero(montoRetirar)
						NuevoSaldo(saldoInicial-montoRetirar)
				}else return false
		} else return false
}
Funcion tranferir_fondos(){
		if(SesionIniciada()){
				cuentaTranferir = input("ingrese cuenta a tranferir:")
				if(verificarDatos(datosCuenta)){
						saldoInicial=Saldo()
						saldoInicialCuentaTranferir=Saldo(cuentaTranferir)
						montoTranferir = input("ingrese monto a tranferir:")
						if (montoTranferir<= saldoInicial AND montoTranferir >0){
								Tranferir(cuentaTranferir,montoTranferir)
								NuevoSaldo(saldoInicial-montoTranferir)
								NuevoSaldo(saldoInicialCuentaTranferir+montoTranferir,cuentaTranferir)
						}else return false
				}else return false
		} else return false
}
```
10). Las pruebas pasan correctamente

11). Todas las funcionalidades descritas en el punto 1 están desarrolladas

12).
### Casos límite :
* Que se quiera crear una cuenta ya existente
* Que se quiera crear una cuenta con datos vacíos
* Que se quiera realizar un depósito, retiro o transferencia igual a 0
* Que se quiera realizar una transferencia a una cuenta inexistente
* Que se quiera realizar un retiro o transferencia con montos mayores a los del saldo

13). Las pruebas pasan correctamente
