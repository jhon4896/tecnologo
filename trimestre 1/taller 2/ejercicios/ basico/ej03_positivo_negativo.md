# Ejercicio 03: Determinar si un Número es Positivo, Negativo o Cero

## Enunciado
Desarrollar un algoritmo que permita leer un número entero ingresado por el usuario y determinar si dicho valor es positivo, negativo o exactamente igual a cero, mostrando el mensaje correspondiente en pantalla.

---

## Análisis
1. **Definición de variables:** Se declara una variable de tipo `Entero` (`Numero`) para almacenar el valor numérico que provea el usuario.
2. **Entrada de datos:** Se solicita por pantalla el ingreso de un número entero.
3. **Proceso de evaluación lógica (Condicionales anidadas):** 
   * Se evalúa si el número es mayor estrictamente a cero (`Numero > 0`). De cumplirse, se indica que es positivo.
   * Si la primera condición no se cumple, se ejecuta una segunda validación para comprobar si el número es menor a cero (`Numero < 0`). De cumplirse, se indica que es negativo.
   * Si ninguna de las dos condiciones anteriores se cumple (es decir, no es mayor ni menor que cero), por lógica el número es cero.
4. **Salida:** Se imprime en pantalla el resultado indicando la clasificación del número ingresado.

---

## Pseudocódigo

```text
Algoritmo Positivo_Negativo_o_Cero
	// Definición de variables
	Definir Numero Como Entero
	
	// Entrada de datos
	Escribir "Ingrese un número entero:"
	Leer Numero
	
	// Revisión del número para saber si es positivo, negativo o es 0
	Si Numero > 0 Entonces
		Escribir "El número ", Numero, " es Positivo."
	SiNo
		Si Numero < 0 Entonces
			Escribir "El número ", Numero, " es Negativo."
		SiNo
			Escribir "El número es Cero."
		FinSi
	FinSi
FinAlgoritmo
