Proceso SistemaInventario
    Definir inventario, productoBuscado Como Cadena;
    Definir opcion, cantidad, i Como Entero;
    Definir encontrado Como Logico;
    Dimension inventario[10];
    
    cantidad <- 0;
    opcion <- 0;
    
    Mientras opcion <> 4 Hacer
        Escribir "";
        Escribir "=== SISTEMA DE INVENTARIO ===";
        Escribir "1. Agregar producto";
        Escribir "2. Listar productos";
        Escribir "3. Buscar producto";
        Escribir "4. Salir";
        Escribir "Seleccione una opcion: ";
        Leer opcion;
        
        Segun opcion Hacer
            1:
                Si cantidad < 10 Entonces
                    cantidad <- cantidad + 1;
                    Escribir "Ingrese el nombre del producto: ";
                    Leer inventario[cantidad];
                    Escribir "Producto agregado correctamente (", cantidad, "/10).";
                Sino
                    Escribir "El inventario esta lleno (maximo 10 productos).";
                FinSi
                
            2:
                Si cantidad = 0 Entonces
                    Escribir "El inventario esta vacio.";
                Sino
                    Escribir "--- Lista de productos ---";
                    Para i <- 1 Hasta cantidad Hacer
                        Escribir i, ". ", inventario[i];
                    FinPara
                FinSi
                
            3:
                Si cantidad = 0 Entonces
                    Escribir "No hay productos registrados para buscar.";
                Sino
                    Escribir "Ingrese el nombre del producto a buscar: ";
                    Leer productoBuscado;
                    encontrado <- Falso;
                    
                    Para i <- 1 Hasta cantidad Hacer
                        Si Mayusculas(inventario[i]) = Mayusculas(productoBuscado) Entonces
                            Escribir "Producto encontrado en la posicion ", i, ": ", inventario[i];
                            encontrado <- Verdadero;
                        FinSi
                    FinPara
                    
                    Si No encontrado Entonces
                        Escribir "El producto no se encuentra en el inventario.";
                    FinSi
                FinSi
                
            4:
                Escribir "Saliendo del sistema de inventario...";
                
            De Otro Modo:
                Escribir "Opcion no valida. Intente nuevamente.";
        FinSegun
    FinMientras
FinProceso
