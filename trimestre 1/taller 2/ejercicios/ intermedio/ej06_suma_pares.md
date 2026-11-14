# Ejercicio 06: Suma de Números Pares

## Enunciado
Desarrollar un algoritmo que permita ingresar un número entero positivo e imprima la suma acumulada de todos los números pares comprendidos entre el 1 y el número introducido por el usuario.

---

## Análisis
1. **Definición de variables:** Se declaran variables de tipo `Entero` (`numeroEntero`, `suma`, `vuelta`). La variable `suma` se inicializa en `0` para que funcione correctamente como acumulador.
2. **Entrada de datos:** Se solicita al usuario que ingrese un número entero límite.
3. **Proceso iterativo (`Para`):** 
   * Se inicia un bucle desde `vuelta <- 1` hasta el `numeroEntero` con un incremento de 1 en cada paso.
   * En cada iteración se evalúa si el número actual (`vuelta`) es par utilizando la operación módulo (`vuelta MOD 2 == 0`).
   * Si la condición se cumple, se suma ese valor al acumulador (`suma <- suma + vuelta`).
4. **Salida:** Se muestra por pantalla el resultado total de la suma de los números pares encontrados en el rango.

---

## Pseudocódigo

```text
Algoritmo SumaNumerosPares
	// Definir variables
	Definir numeroEntero, suma, vuelta Como Entero
	suma <- 0
	
	// Ingreso de datos
	Escribir "Ingrese un número entero:"
	Leer numeroEntero
	
	// Fórmula y ciclo de cálculo
	Para vuelta <- 1 Hasta numeroEntero Con Paso 1 Hacer
		Si vuelta MOD 2 == 0 Entonces
			suma <- suma + vuelta
		FinSi
	FinPara
	
	// Resultado
	Escribir "La suma de los números pares entre 1 y ", numeroEntero, " es: ", suma
FinAlgoritmo
