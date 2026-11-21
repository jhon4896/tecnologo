Algoritmo  OrdenamientoBurbuja
    Definir vec, i, j, aux Como Entero;
    Dimension vec[8];
    
    // Lectura de los 8 elementos
    Para i <- 1 Hasta 8 Hacer
        Escribir "Ingrese el numero entero en la posicion ", i, ": ";
        Leer vec[i];
    FinPara
    
    // Metodo de burbuja (menor a mayor)
    Para i <- 1 Hasta 7 Hacer
        Para j <- 1 Hasta 8 - i Hacer
            Si vec[j] > vec[j + 1] Entonces
                aux <- vec[j];
                vec[j] <- vec[j + 1];
            FinSi
        FinPara
    FinPara
    
    // Mostrar vector ordenado
    Escribir "Vector ordenado de menor a mayor:";
    Para i <- 1 Hasta 8 Hacer
        Escribir Sin Saltar vec[i], " ";
    FinPara
    Escribir "";
FinAlgoritmo
