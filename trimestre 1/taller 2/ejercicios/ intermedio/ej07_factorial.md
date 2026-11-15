# Ejercicio 07: Cálculo del Factorial de un Número

## Enunciado
Desarrollar un algoritmo que permita calcular el factorial de un número entero positivo ingresado por el usuario, incorporando una validación para asegurar que el valor ingresado no sea negativo antes de realizar la operación matemática.

---

## Análisis
1. **Definición de variables:** Se declaran variables de tipo `Entero` (`numeroEntero`, `vuelta`) para el control del número y las iteraciones, y una variable de tipo `Real` (`factorial`) inicializada en `1` para almacenar el resultado acumulado (evitando desbordamientos prematuros por el crecimiento rápido del factorial).
2. **Entrada de datos:** Se solicita al usuario el ingreso de un número entero positivo.
3. **Validación condicional:** Se evalúa si el número es mayor o igual a cero (`numeroEntero >= 0`). 
   * Si es válido, se ejecuta un bucle `Para` desde 1 hasta el número ingresado, multiplicando de forma sucesiva para obtener el factorial (`factorial <- factorial * vuelta`).
   * Si no es válido (número negativo), se muestra un mensaje de error por pantalla.
4. **Salida:** Se imprime en pantalla el resultado final del factorial correspondiente al número evaluado.

---

## Pseudocódigo

```text
Algoritmo CalcularFactorial
	Definir numeroEntero, vuelta Como Entero
	Definir factorial Como Real
	
	factorial <- 1
	
	Escribir "Ingrese un número entero positivo:"
	Leer numeroEntero
	
	Si numeroEntero >= 0 Entonces
		Para vuelta <- 1 Hasta numeroEntero Con Paso 1 Hacer
			factorial <- factorial * vuelta
		FinPara
		
		Escribir "-----------------------------------"
		Escribir "El factorial de ", numeroEntero, "! es: ", factorial
	SiNo
		Escribir "Error: El número debe ser positivo o cero."
	FinSi
FinAlgoritmo
