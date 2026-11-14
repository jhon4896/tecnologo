# Ejercicio 11: Búsqueda del Número Mayor y Menor en un Vector

## Enunciado
Desarrollar un algoritmo que permita almacenar 10 números enteros en un vector (arreglo unidimensional), para posteriormente recorrerlo y determinar cuál es el número mayor y cuál es el menor, indicando además en qué posición exacta del vector se encuentran.

---

## Análisis
1. **Definición de variables y dimensiones:** 
   * Se declaran variables de tipo `Entero` (`ciclo` para los bucles, `mayor`, `menor` para almacenar los valores límite, y `posicionMayor`, `posicionMenor` para registrar los índices).
   * Se dimensiona el vector con un tamaño de 11 (`Dimension vector[11]`) para trabajar cómodamente con los índices del 1 al 10.
2. **Entrada de datos (`Para`):** Se implementa un bucle iterativo que recorre del 1 al 10 solicitando al usuario que ingrese un número entero por cada posición del vector.
3. **Inicialización:** Se asigna el primer elemento del vector (`vector[1]`) como el valor inicial tanto para `mayor` como para `menor`, fijando sus posiciones iniciales en `1`.
4. **Proceso de comparación (`Para`):** Se realiza un segundo recorrido a partir de la posición 2 hasta la 10:
   * Si el número evaluado es mayor que el valor actual almacenado en `mayor`, se actualiza la variable `mayor` y se guarda su posición.
   * Si el número evaluado es menor que el valor actual almacenado en `menor`, se actualiza la variable `menor` y se guarda su posición.
5. **Salida:** Se imprimen en pantalla los valores límite encontrados junto con sus respectivas posiciones dentro del vector.

---

## Pseudocódigo

```text
Algoritmo Mayor_Y_Menor_Vector
	Definir vector, ciclo, mayor, menor, posicionMayor, posicionMenor Como Entero;
	Dimension vector[11];
	
	// 1. Lectura de los 10 números
	Para ciclo <- 1 Hasta 10 Con Paso 1 Hacer
		Escribir "Ingrese el número entero para la posición ", ciclo, ":";
		Leer vector[ciclo];
	FinPara
	
	// 2. Inicializamos mayor y menor con el primer elemento
	mayor <- vector[1];
	menor <- vector[1];
	posicionMayor <- 1;
	posicionMenor <- 1;
	
	// 3. Recorremos desde la posición 2 hasta la 10 para comparar
	Para ciclo <- 2 Hasta 10 Con Paso 1 Hacer
		Si vector[ciclo] > mayor Entonces
			mayor <- vector[ciclo];
			posicionMayor <- ciclo;
		FinSi
		
		Si vector[ciclo] < menor Entonces
			menor <- vector[ciclo];
			posicionMenor <- ciclo;
		FinSi
	FinPara
	
	// 4. Mostrar resultados
	Escribir "----------------------------------------";
	Escribir "El número MAYOR es: ", mayor, " y está en la posición: ", posicionMayor;
	Escribir "El número MENOR es: ", menor, " y está en la posición: ", posicionMenor;
FinAlgoritmo
