

Ejercicios sobre punteros arreglos y la declaración Struct
=====


---
**Antes de comenzar**

* Abra el Visual Studio Code y abra una nueva ventana
* En el explorador ponga la opción para clonar repositorio y clone **este repositorio**
* Sólo puede modificar el archivo `exercises.c` 
* Para testear sus códigos debe abrir un terminal *git bash* y ejecutar el comando `./test.sh`
* Verifique que sus cambios se hayan subido al repositorio en github
* No está permitido usar comandos de git (a menos que el profesor lo indique)
---

1. Programe la función `void swap(int *a, int *b)`, la cual
intercambia los valores de las variables apuntadas por a y b.

2. Programe la función `void arrayMaxMin(int *a, int n, int *max, int *min)`,
la cual encuentra el máximo y el mínimo valor del arreglo `a` y los
almacena en las variables apuntadas por `max` y `min`.

3. Considere la siguiente `struct Persona`: 
````c
typedef struct {
  char nombre[30];
  char rut[11];
  int edad;
} Persona; 
````

Programe la función `Persona *crearPersona(...)`, la cual crea una nueva persona con los datos correspondientes y retorna un puntero al dato recién creado. 

4. Considere la siguiente `struct Vector`:
````c
typedef struct {
   int * datos; // arreglo dinámico
   int capacidad; // capacidad del arreglo
} Vector;
````
Escriba la función `Vector* crearVector(int n)`, la cual crea un vector con capacidad `n`, reserva la memoria correspondiente para el arreglo con `n` datos inicializados en 0 y luego retorna el vector creado.

5. Programe las función void `asignarValor(Vector * v, int i, int valor)`, 
la cual asigna `valor` a la posición `i` del vector `v`.

6. Programe la función `int obtenerDato(Vector * v, int i)`, la cual retorna el dato en la posición `i` del vector `v`.

7. Programe la función void `sumaV(Vector * a, Vector * b, Vector * c)`, la cual suma los vectores `a` y `b` y actualiza el vector `c` con el resultado de la suma. Asuma que los vecotres tienen el mismo tamaño.

Por ejemplo, si:

````
a: [0 4  8 12 16 20 24 28 32 36]
b: [0 8 16 24 32 40 48 56 64 72]
````
, entonces:
````
c: [0 12 24 36 48 60 72 84 96 108 ]
````

8. Implemente la función `sumaV2(int a1, int a2, int b1, int b2, Vector *c)`. Esta función realiza la suma de vectores `(a1,a2)+(b1,b2)` y almacena el resultado en el vector `c`. Utilice las operaciones de vectores implementadas anteriormente!
