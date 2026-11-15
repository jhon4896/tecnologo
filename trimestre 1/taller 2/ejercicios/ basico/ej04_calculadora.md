# Ejercicio 04: Calculadora Básica con Menú de Opciones

## Enunciado
Desarrollar un algoritmo que funcione como una calculadora básica, permitiendo al usuario ingresar dos números enteros, seleccionar una operación aritmética mediante un menú interactivo (Suma, Resta, Multiplicación o División) y mostrar el resultado correspondiente en pantalla, incluyendo validaciones de seguridad para la operación de división.

---

## Análisis
1. **Definición de variables:** Se declaran variables de tipo `Entero` (`numero1`, `numero2`, `opcion`) para capturar los operandos y la selección del usuario, y una variable de tipo `Real` (`resultado`) para almacenar con precisión el valor arrojado por la operación.
2. **Entrada de datos:** Se solicitan y leen los dos números enteros por consola.
3. **Menú de opciones:** Se despliegan en pantalla las alternativas disponibles numeradas del 1 al 4 para que el usuario elija la operación deseada.
4. **Estructura de selección múltiple (`Segun`):** 
   * **Opción 1 (Suma):** Suma ambos números.
   * **Opción 2 (Resta):** Resta el segundo número al primero.
   * **Opción 3 (Multiplicación):** Multiplica ambos números.
   * **Opción 4 (División):** Incluye una validación condicional previa para evitar errores matemáticos, procediendo con la división si los valores son aptos, o notificando un error en caso contrario.
   * **De Otro Modo:** Captura cualquier selección fuera del rango establecido e informa que la opción no es válida.
5. **Salida:** Se imprime en pantalla el mensaje con el resultado final de la operación seleccionada.

---

## Pseudocódigo

```text
Algoritmo Calculadora_Básica
	// Definición de variables
    Definir numero1, numero2, opcion Como Entero
    Definir resultado Como Real
	
    // Entrada de números
    Escribir "Por favor ingrese el primer número entero:"
    Leer numero1
    Escribir "Por favor ingrese el segundo número entero:"
    Leer numero2
	
    // Mostrar el menú de opciones
    Escribir "Seleccione la operación a realizar:"
    Escribir "1: Suma"
    Escribir "2: Resta"
    Escribir "3: Multiplicación"
    Escribir "4: División"
    Leer opcion
	
    // Estructura para evaluar la opción seleccionada
    Segun opcion Hacer
        1:
            resultado <- numero1 + numero2
            Escribir "El resultado de la suma es: ", resultado
        2:
            resultado <- numero1 - numero2
            Escribir "El resultado de la resta es: ", resultado
        3:
            resultado <- numero1 * numero2
            Escribir "El resultado de la multiplicación es: ", resultado
        4:
            // Validación para evitar errores en división
            Si numero1 = 0 o numero2 = 0 Entonces
                Escribir "Error: No se puede dividir entre cero."
            SiNo
                resultado <- numero1 / numero2
                Escribir "El resultado de la división es: ", resultado
            FinSi
        De Otro Modo:
            Escribir "Opción no válida. Debe elegir un número del 1 al 4."
    FinSegun
FinAlgoritmo
