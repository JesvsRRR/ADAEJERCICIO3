# 1. Formulación del problema

<p align="center">
  <img src="image.png" alt="Imagen del ejercicio n°3" />
</p>

# 2. Resolución

> I) Entrada del valor de la variable "dimension"

- Utilizando la libreria java `Scanner` para ingresar datos de entrada, se ingresa el valor correspondiente a la variable `"d"`.

```bash
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.println("Ingresar dimension [d]: ");
        int d = sc.nextInt();
        
        if(d <= 0){
           d = sc.nextInt();;
        }
```
> II) Inicialización de la variable almacenadora de sumatoria, impresión de la matriz e ingreso de numeros en la matriz

- Se hace un llamado a la función `"Suma_perimetro`, la cual usara la variable `"d"`.
- Se inicializa una `Matriz` tamaño dxd y una variable almacenadora que sumara todos los numeros del perimetro de la matriz cuadratica.
- Se procede a ingresar los valores numericos a cada elemento de la matriz mediante un recorrido en doble bucle

```bash
int Suma_perimetro = Sumatoria(d);
```

```bash
    public static int Sumatoria(int d){
    Scanner sc = new Scanner(System.in);      
    int[][]Matriz = new int[d][d];
    int salida = 0;
    
    for(int i=0; i < d; i++){
        for(int j=0; j < d;j++){
            System.out.print("["+i+"]"+"[" + j+"]");
            Matriz[i][j] = sc.nextInt();           
        }
    } 
```

> III) Impresión de la matriz cuadrada, calculo de la sumatoria del perimetro de la matriz cuadrada dXd e impresión de salida de la variable "Suma_perimetro"



```bash

    for(int i=0; i < d; i++){
        for(int j=0; j < d;j++){
            System.out.print("["+Matriz[i][j]+"]");
           
        }
        System.out.println("");
    }

    for(int i=0; i < d; i++){
        if(i == 0 || i == d-1){
        for(int j=0; j < d; j++){
        salida += Matriz[i][j];    
        }
        }
        else{
        salida += Matriz[i][0];
        salida += Matriz[i][d-1];
        }
    }
    
    return salida;
    }
```

```bash
    System.out.println("SUMATORIA TOTAL: " + Suma_perimetro);
```

### Codigo completo

```bash
import java.util.Scanner;

public class Main {
    
    public static int Sumatoria(int d){
    Scanner sc = new Scanner(System.in);      
    int[][]Matriz = new int[d][d];
    int salida = 0;
    
    for(int i=0; i < d; i++){
        for(int j=0; j < d;j++){
            System.out.print("["+i+"]"+"[" + j+"]");
            Matriz[i][j] = sc.nextInt();           
        }
    }  
    
    for(int i=0; i < d; i++){
        for(int j=0; j < d;j++){
            System.out.print("["+Matriz[i][j]+"]");
           
        }
        System.out.println("");
    } 
    
    for(int i=0; i < d; i++){
        if(i == 0 || i == d-1){
        for(int j=0; j < d; j++){
        salida += Matriz[i][j];    
        }
        }
        else{
        salida += Matriz[i][0];
        salida += Matriz[i][d-1];
        }
    }
    
    return salida;
    }
   
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.println("Ingresar dimension [d]: ");
        int d = sc.nextInt();
        
        if(d <= 0){
           d = sc.nextInt();;
        }

        int Suma_perimetro = Sumatoria(d);
        System.out.println("SUMATORIA TOTAL: " + Suma_perimetro);
    }
    
}
```

# 3. Complejidad

> I) Entrada del valor de la variable "dimension"

- Complejidad de tiempo: 𝑂(1)
- Complejidad de espacio: 𝑂(1)

> II) Inicialización de la variable almacenadora de sumatoria, impresión de la matriz e ingreso de numeros en la matriz

- Complejidad de tiempo: 𝑂(d²)
- Complejidad de espacio: 𝑂(d²)

>III) Impresión de la matriz cuadrada, calculo de la sumatoria del perimetro de la matriz cuadrada dXd e impresión de salida de la variable "Suma_perimetro"

- Complejidad de tiempo: 𝑂(d²)
- Complejidad de espacio: 𝑂(d²)

