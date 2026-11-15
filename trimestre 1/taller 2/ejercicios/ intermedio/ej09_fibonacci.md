# Ejercicio 09: Generación de la Serie de Fibonacci

## Enunciado
Desarrollar un algoritmo que permita generar y mostrar en pantalla los primeros $N$ términos de la clásica secuencia de Fibonacci, donde cada número se calcula sumando los dos anteriores (comenzando habitualmente en 0 y 1), solicitando al usuario la cantidad de términos deseados.

---

## Análisis
1. **Definición de variables:** Se declaran variables de tipo `Entero` (`n` para almacenar el límite de términos, `a` y `b` para los dos primeros valores iniciales de la serie, `temp` como variable temporal de intercambio, y `vuelta` para controlar el bucle).
2. **Entrada de datos:** Se solicita al usuario el número total de términos que desea visualizar.
3. **Inicialización:** Se establecen los valores base de la serie (`a <- 0` y `b <- 1`).
4. **Proceso iterativo (`Para`):** 
   * Se recorre desde 1 hasta `n`.
   * Para el primer término (`vuelta = 1`), se imprime directamente el valor de `a` (0).
   * Para el segundo término (`vuelta = 2`), se imprime el valor de `b` (1).
   * A partir del tercer término, se calcula el siguiente valor sumando los dos anteriores (`temp <- a + b`), se desplazan los valores (`a <- b` y `b <- temp`), y se imprime el nuevo término. Se utiliza la cláusula `Sin Saltar` para mantener la secuencia en una sola línea.
5. **Salida:** Se imprimen los términos de la serie de forma consecutiva seguidos de un salto de línea final.

---

## Pseudocódigo

```text
Algoritmo SerieFibonacci
	Definir n, a, b, temp, vuelta Como Entero
	
	Escribir "Ingrese la cantidad de términos de Fibonacci a mostrar:"
	Leer n
	
	a <- 0
	b <- 1
	
	Escribir "Los primeros ", n, " términos son:"
	
	Para vuelta <- 1 Hasta n Con Paso 1 Hacer
		Si vuelta == 1 Entonces
			Escribir a, " " Sin Saltar
		SiNo
			Si vuelta == 2 Entonces
				Escribir b, " " Sin Saltar
			SiNo
				temp <- a + b
				a <- b
				b <- temp
				Escribir b, " " Sin Saltar
			FinSi
		FinSi
	FinPara
	
	Escribir "" // Salto de línea final
FinAlgoritmo
