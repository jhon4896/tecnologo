Funcion resultado <- EsPrimo(n)
    Definir resultado Como Logico;
    Definir i, divisores Como Entero;
    
    Si n <= 1 Entonces
        resultado <- Falso;
    Sino
        divisores <- 0;
        Para i <- 1 Hasta n Hacer
            Si n MOD i = 0 Entonces
                divisores <- divisores + 1;
            FinSi
        FinPara
        
        Si divisores = 2 Entonces
            resultado <- Verdadero;
        Sino
            resultado <- Falso;
        FinSi
    FinSi
FinFuncion

Proceso PrimosEnRango
    Definir inicio, fin, num, temp Como Entero;
    Definir hayPrimos Como Logico;
    
    Escribir "Ingrese el numero de inicio del rango: ";
    Leer inicio;
    Escribir "Ingrese el numero de fin del rango: ";
    Leer fin;
    
    // Si el usuario ingresa inicio mayor que fin, se intercambian
    Si inicio > fin Entonces;
        temp <- inicio;
        inicio <- fin;
	fin <- temp;
FinSi

hayPrimos <- Falso;
Escribir "Numeros primos entre ", inicio, " y ", fin, ":";

Para num <- inicio Hasta fin Hacer
	Si EsPrimo(num) Entonces
		Escribir num;
		hayPrimos <- Verdadero;
	FinSi
FinPara

Si No hayPrimos Entonces
	Escribir "No se encontraron numeros primos en este rango."
FinSi
FinProceso
