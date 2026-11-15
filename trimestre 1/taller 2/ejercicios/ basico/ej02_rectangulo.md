# Ejercicio 02: Cálculo del Área y Perímetro de un Rectángulo

## Enunciado
Desarrollar un algoritmo que permita calcular el área y el perímetro de un rectángulo a partir de los valores de su base y su altura ingresados por el usuario, mostrando ambos resultados en pantalla.

---

## Análisis
1. **Definición de variables:** Se declaran variables de tipo `Real` para almacenar los datos de entrada (`base`, `altura`) y los resultados de los cálculos (`area`, `perimetro`).
2. **Entrada de datos:** Se solicita al usuario que ingrese primero la altura y luego la base del rectángulo.
3. **Proceso de cálculo:** 
   * Se calcula el área multiplicando la base por la altura (`area <- altura * base`).
   * Se calcula el perímetro sumando todos sus lados (`perimetro <- base + base + altura + altura`, que equivale a la fórmula $2 \times (\text{base} + \text{altura})$).
4. **Salida:** Se imprimen en pantalla los resultados obtenidos tanto para el área como para el perímetro.

---

## Pseudocódigo

```text
Algoritmo Área_de_un_Rectángulo
	// Definición de variables
	Definir altura, base Como Real
	Definir area, perimetro Como Real
	
	// Pedir la altura y base 
	Escribir "Por favor escriba la altura del rectángulo:";
	Leer altura;
	Escribir "Por favor escriba la base del rectángulo:";
	Leer base;
	
	// Calcular el área 
	area <- altura * base;
	
	// Calcular el perímetro
	perimetro <- base + base + altura + altura;
	
	// Escribir el resultado
	Escribir "El área es: ", area;
	Escribir "El perímetro es: ", perimetro;
FinAlgoritmo
