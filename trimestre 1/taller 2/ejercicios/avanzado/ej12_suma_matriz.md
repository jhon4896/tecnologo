# Ejercicio 12: Suma de una Matriz de 3x3 y su Diagonal Principal

## Enunciado
Desarrollar un algoritmo que permita poblar una matriz bidimensional (tabla) de $3 \times 3$ con números enteros ingresados por el usuario, para calcular posteriormente la suma total de todos sus elementos y la suma exclusiva de los elementos que componen su diagonal principal.

---

## Análisis
1. **Definición de variables y dimensiones:** 
   * Se declaran variables de tipo `Entero` (`i` para iterar las filas, `j` para iterar las columnas, `sumaTotal` como acumulador global y `sumaDiagonal` como acumulador específico).
   * Se dimensiona la matriz bidimensional con un tamaño de $3 \times 3$ (`Dimension matriz[3, 3]`).
2. **Lectura y procesamiento simultáneo (`Para` anidado):** 
   * Se utiliza un bucle externo para las filas (`i`) y un bucle interno para las columnas (`j`).
   * Por cada posición solicitada, se captura el valor ingresado por el usuario.
   * Se acumula inmediatamente en `sumaTotal`.
   * Mediante una estructura condicional (`Si i = j Entonces`), se valida si el índice de la fila coincide con el de la columna; de ser así, se acumula también en la variable `sumaDiagonal`.
3. **Visualización en formato de tabla:** Se recorre nuevamente la matriz imprimiendo cada elemento separado por espacios (`Sin Saltar`) y realizando un salto de línea al terminar cada fila para mostrarla de forma gráfica en la consola.
4. **Salida final:** Se muestran en pantalla los resultados numéricos de la suma total y de la diagonal principal.

---

## Pseudocódigo

```text
Algoritmo Suma_Matriz_Y_Diagonal
	Definir matriz, i, j, sumaTotal, sumaDiagonal Como Entero;
	Dimension matriz[3, 3];
	
	// Inicializamos las variables acumuladoras en 0
	sumaTotal <- 0;
	sumaDiagonal <- 0;
	
	Escribir "=== LECTURA DE LA MATRIZ 3x3 ===";
	
	// 1. Recorrido por filas (i) y columnas (j) para leer los datos
	Para i <- 1 Hasta 3 Con Paso 1 Hacer
		Para j <- 1 Hasta 3 Con Paso 1 Hacer
			Escribir "Ingrese el número para la posición [", i, ",", j, "]:";
			Leer matriz[i, j];
			
			// 2. Acumulamos la suma de TODOS los elementos
			sumaTotal <- sumaTotal + matriz[i, j];
			
			// 3. Evaluamos si pertenece a la diagonal principal (fila igual a columna)
			Si i = j Entonces
				sumaDiagonal <- sumaDiagonal + matriz[i, j];
			FinSi
		FinPara
	FinPara
	
	// 4. Mostrar la matriz en pantalla en formato de tabla (opcional para verificar)
	Escribir "----------------------------------------";
	Escribir "Matriz ingresada:";
	Para i <- 1 Hasta 3 Con Paso 1 Hacer
		Para j <- 1 Hasta 3 Con Paso 1 Hacer
			Escribir Sin Saltar matriz[i, j], "    ";
		FinPara
		Escribir ""; // Salto de línea al terminar cada fila
	FinPara
	
	// 5. Mostrar los resultados finales
	Escribir "----------------------------------------";
	Escribir "Suma de TODOS los elementos: ", sumaTotal;
	Escribir "Suma de la DIAGONAL PRINCIPAL: ", sumaDiagonal;
FinAlgoritmo
