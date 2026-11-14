# Ejercicio 01: Cálculo de Promedio de Notas

## Enunciado
Desarrollar un algoritmo que permita calcular el promedio de tres notas (ingresadas en un rango de 10 a 100), determinando si el estudiante aprueba o desaprueba con base en una nota mínima de 60. Además, el programa debe identificar y notificar de manera especial si el estudiante aprueba exactamente con la nota mínima (raspando).

---

## Análisis
1. **Definición de variables:** Se declaran variables de tipo `Real` para almacenar las tres notas individuales (`nota1`, `nota2`, `nota3`), la sumatoria total (`suma`) y el resultado del promedio (`promedio`). También se define una constante o variable de control (`notaminima = 60`) y variables lógicas (`aprobado`, `desaprobado`) para las evaluaciones de condición.
2. **Entrada de datos:** Se solicita al usuario el ingreso de las tres calificaciones.
3. **Proceso de cálculo:** 
   * Se suman las tres notas (`suma <- nota1 + nota2 + nota3`).
   * Se divide la suma entre 3 para obtener la nota media (`promedio <- suma / 3`).
4. **Estructura condicional:** 
   * Se evalúa si el promedio es mayor o igual a 60.
   * Si es aprobado, se evalúa mediante una condición anidada si el promedio es exactamente igual a 60 (`promedio == notaminima`) para arrojar un mensaje especial ("Aprobado raspando"). En caso contrario, se muestra un mensaje de aprobación general.
   * Si no cumple la condición principal, se indica que el estudiante se encuentra desaprobado.
5. **Salida:** Se imprimen en pantalla el estado correspondiente del estudiante junto con su promedio final.

---

## Pseudocódigo

```text
Algoritmo Cálculo_de_Promedio
	// Definición de variables
    Definir suma, promedio Como Real
	Definir nota1, nota2, nota3, notaminima Como Real
	Definir aprobado, desaprobado Como logico
	
	// Pedir las notas
	Escribir "Por favor ingrese las 3 notas que desea saber el promedio entre 10 a 100";
	Leer nota1;
	Leer nota2;
	Leer nota3;
	
	// Suma de notas y saber el promedio
	suma <- nota1 + nota2 + nota3
	promedio <- suma / 3
	
	// Evaluación lógica para saber el estado del estudiante
	aprobado <- promedio >= 60
	notaminima <- 60
	desaprobado <- promedio < 60
	
	// Mostrar resultado
	Si aprobado Entonces
        // Verificamos si pasó exactamente con el mínimo
        Si promedio == notaminima Entonces
            Escribir "¡Estado: Aprobado raspando con la nota mínima!"
			Escribir "Su promedio es: ", promedio
        Sino
            Escribir "¡Estado: Aprobado!"
			Escribir "Su promedio es: ", promedio
        FinSi
    SiNo
        Escribir "Estado: Desaprobado"
		Escribir "Su promedio es: ", promedio
    FinSi
FinAlgoritmo
