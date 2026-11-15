# Ejercicio 05: Conversión de Temperatura (Celsius a Fahrenheit)

## Enunciado
Desarrollar un algoritmo que permita recibir una temperatura expresada en grados Celsius (°C) por parte del usuario, aplicar la fórmula de conversión matemática correspondiente y mostrar el resultado equivalente en grados Fahrenheit (°F) en pantalla.

---

## Análisis
1. **Definición de variables:** Se declaran variables de tipo `Real` (`celsius`, `fahrenheit`) para almacenar con precisión decimal tanto el valor ingresado como el resultado de la conversión.
2. **Entrada de datos:** Se solicita al usuario que ingrese la temperatura numérica en grados Celsius.
3. **Proceso de cálculo:** Se aplica la fórmula estándar de conversión multiplicando los grados Celsius por 9/5 y sumando 32 (`fahrenheit <- (celsius * 9 / 5) + 32`).
4. **Salida:** Se imprimen en pantalla los datos indicando claramente la equivalencia de la temperatura original en su nueva unidad Fahrenheit.

---

## Pseudocódigo

```text
Algoritmo Conversión_de_Temperatura
	// Definición de variables
    Definir celsius, fahrenheit Como Real
    
    // Entrada de datos
    Escribir "Ingrese la temperatura en grados Celsius (°C):"
    Leer celsius
    
    // Proceso: Aplicar la fórmula de conversión
    fahrenheit <- (celsius * 9 / 5) + 32
    
    // Mostrar el resultado
    Escribir "-----------------------------------"
    Escribir celsius, " °C equivalen a ", fahrenheit, " °F."	
FinAlgoritmo
