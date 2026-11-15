# Ejercicio 08: Conteo de Vocales en un Texto

## Enunciado
Desarrollar un algoritmo que permita ingresar una palabra o frase corta por parte del usuario, recorriendo su estructura carácter por carácter para contar e imprimir el número total de vocales contenidas, normalizando las letras a minúsculas para simplificar la validación.

---

## Análisis
1. **Definición de variables:** Se declaran variables de tipo `Cadena` (`texto`, `letra`) para almacenar la frase y el carácter evaluado en cada iteración, y variables de tipo `Entero` (`vuelta`, `longitudTexto`, `contador`). La variable `contador` se inicializa en `0`.
2. **Entrada de datos:** Se solicita al usuario que ingrese una palabra o frase corta.
3. **Proceso iterativo (`Para`):** 
   * Se calcula la longitud total de la cadena usando la función `Longitud`.
   * Se recorre el texto desde la posición 1 hasta el total de la longitud.
   * En cada paso, se extrae el carácter actual con `Subcadena` y se convierte a minúscula usando `Minusculas` para asegurar que el conteo funcione sin importar si se ingresan mayúsculas.
   * Se evalúa mediante una condición lógica si el carácter es igual a 'a', 'e', 'i', 'o' o 'u'. De ser así, se incrementa el acumulador `contador <- contador + 1`.
4. **Salida:** Se imprime en pantalla el número total de vocales encontradas en el texto.

---

## Pseudocódigo

```text
Algoritmo ContarVocales
	Definir texto Como Cadena
	Definir vuelta, longitudTexto, contador Como Entero
	Definir letra Como Cadena
	
	contador <- 0
	
	Escribir "Ingrese una palabra o frase corta:"
	Leer texto
	
	longitudTexto <- Longitud(texto)
	
	Para vuelta <- 1 Hasta longitudTexto Con Paso 1 Hacer
		letra <- Subcadena(texto, vuelta, vuelta)
		letra <- Minusculas(letra)
		
		Si letra == "a" O letra == "e" O letra == "i" O letra == "o" O letra == "u" Entonces
			contador <- contador + 1 
		FinSi
	FinPara
	
	Escribir "-----------------------------------"
	Escribir "El texto contiene ", contador, " vocal(es)."
FinAlgoritmo
