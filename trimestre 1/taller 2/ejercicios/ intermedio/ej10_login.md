# Ejercicio 10: Validación de Contraseña de sena

## Enunciado
Desarrollar un algoritmo que simule un sistema de autenticación por contraseña, permitiendo al usuario un máximo de 3 intentos para ingresar la clave correcta. Si acierta, el sistema concede el acceso; si agota los intentos, la cuenta se bloquea.

---

## Análisis
1. **Definición de variables:** Se declara una variable de tipo `Cadena` (`clave`) para capturar la entrada del usuario, una variable de tipo `Entero` (`intentos`) inicializada en `3`, y una variable de tipo `Lógico` (`acceso`) inicializada en `Falso` para controlar el estado de la validación.
2. **Proceso iterativo (`Mientras`):** 
   * El ciclo se ejecuta siempre y cuando queden intentos disponibles (`intentos > 0`) y el acceso siga siendo falso (`NO acceso`).
   * Se solicita al usuario ingresar la contraseña mostrando el contador de intentos restantes.
   * Se valida si la clave ingresada coincide con la contraseña predefinida (`"12345"`). Si es correcta, la bandera `acceso` cambia a `Verdadero`.
   * Si es incorrecta, se descuenta un intento (`intentos <- intentos - 1`) y se notifica el error.
3. **Salida final:** Tras finalizar el ciclo, se evalúa el estado de la variable `acceso`: si es verdadero, se muestra un mensaje de bienvenida; si es falso (se agotaron los intentos), se muestra un aviso de bloqueo de cuenta.

---

## Pseudocódigo

```text
Algoritmo ValidarContrasena
	Definir clave Como Cadena
	Definir intentos Como Entero
	Definir acceso Como Lógico
	
	intentos <- 3
	acceso <- Falso
	
	Mientras intentos > 0 Y NO acceso Hacer
		Escribir "Ingrese la contraseña (Intentos restantes: ", intentos, "):"
		Leer clave
		
		Si clave == "12345" Entonces
			acceso <- Verdadero
		SiNo
			intentos <- intentos - 1
			Escribir "Contraseña incorrecta."
		FinSi
	FinMientras
	
	Si acceso Entonces
		Escribir "¡Bienvenido!"
	SiNo
		Escribir "Cuenta bloqueada."
	FinSi
FinAlgoritmo
