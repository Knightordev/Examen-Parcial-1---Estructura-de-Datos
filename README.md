#  Examen Parcial 1 - Estructura de Datos

---

## EJERCICIO 1
Este ejercicio cuenta con dos arreglos:  
- El primero almacena los nombres.  
- El segundo almacena la longitud de los mismos.  

El programa:  
1. Usa un ciclo **While** para pedir la cantidad de nombres.  
2. Con **Try** y **Except** valida que el valor ingresado sea un número entero.  
3. Después, en un **ciclo For**, solicita los nombres, calcula su longitud y guarda estos valores en el arreglo.  
4. Finalmente, imprime los nombres con sus longitudes.  

---

## EJERCICIO 2
Se creó una clase llamada **Temperatura** con los siguientes elementos:  

- Lista de temperaturas.  
- **Método privado** para añadir una temperatura.  
- **Método privado promedio de temperatura**: suma la lista y divide entre el tamaño (2 decimales).  
- **Método privado obtener temperatura máxima**: usa `max`.  
- **Método privado obtener temperatura mínima**: usa `min`.  
- **Método privado días arriba del promedio**: lista de temperaturas mayores al promedio y devuelve su tamaño.  
- **Método privado para agregar 7 temperaturas**: números flotantes de 2 decimales.  
- **Método privado para obtener información**: muestra promedio, máximo, mínimo y días arriba del promedio.  
- **Método público main**: ejecuta el agregado de temperaturas y obtiene la información.  

---

##  EJERCICIO 3
El programa convierte números positivos a **binario** usando **recursividad**.  

### Funciones:
- **D_B_E**: Convierte la parte entera dividiendo entre 2 y guardando residuos hasta llegar a 0.  
- **D_B**: Maneja decimales. Separa parte entera (mandada a la función recursiva) y multiplica la parte decimal por 2, tomando los enteros sucesivos.  

La recursividad ocurre en la parte entera (`n // 2` hasta el caso base `n == 0`).  
En cada retorno se agrega el residuo (`n % 2`) construyendo el binario en orden correcto.  

En conclusión: convierte **enteros y decimales** a binario con recursividad en la parte entera e iteración en la parte decimal.  

---

##  EJERCICIO 4
```
import random 

longitud = int(input("Ingresa la longitud del vetor: "))

a = [None] * longitud     # Se crean vectores vacíos según lo ingresado
b = [None] * longitud
sumando = [None] * longitud 
restando = [None] * longitud

for i in range(longitud):   # Se llenan con números aleatorios de -100 a 100
    a[i]=random.randint (-100,100)
    b[i]=random.randint (-100,100)

for i in range(longitud):   # Se suman y restan los valores
    sumando[i] = a[i] + b[i]
    restando[i] = a[i] - b[i]

opciones = int(input("Seleccione qué vector desea ver (1=a, 2=b, 3=suma, 4=resta): "))

if opciones == 1:
    print("vector A:", a)

elif opciones == 2:
    print("vector B:", b)

elif opciones == 3:
    print("vector C (sumando a y b):", sumando)

elif opciones == 4:
    print("vector C (restando a y b):", restando)
    exit()

else:
    print("No es válida esta opción")
    exit()
````
## EJERCICIO 5

El programa tiene como objetivo identificar qué palabras de una lista son palíndromas, es decir, aquellas que se leen igual de izquierda a derecha que de derecha a izquierda. Para lograrlo, se pide al usuario cuántas palabras quiere ingresar y luego se almacenan dentro de un arreglo o lista.

Se crea una función llamada es_palindromo que recibe una palabra y la compara con su versión invertida usando un truco muy común en el lenguaje (palabra[::-1]). Si ambas coinciden, la función devuelve verdadero. Después, se recorren todas las palabras ingresadas y se muestran únicamente aquellas que cumplen la condición de ser palíndromas.

En ambos lenguajes se normalizan las palabras a minúsculas para que las mayúsculas no afecten la comparación (por ejemplo, “Ana” y “ana” se detectan igual). Gracias a este procedimiento, el programa puede trabajar con cualquier lista de palabras que el usuario introduzca y mostrar de manera clara cuáles cumplen la característica de palíndromas.

## EJERCICIO 6

Este programa sirve para calcular cómo se reparte un terreno a lo largo de varias generaciones. La lógica es simple: se empieza con un terreno de cierto tamaño y, en cada generación, ese terreno se divide en partes iguales entre un número fijo de herederos. Cada vez que pasa una generación, la superficie que recibe cada heredero se reduce, porque se vuelve a dividir entre los nuevos descendientes.

Cuando se ejecuta, el programa pide tres datos al usuario: el tamaño inicial del terreno, la cantidad de generaciones que se quieren calcular y el número de herederos por generación. Con esta información, primero revisa que los datos sean correctos, es decir, que el número de generaciones esté entre 0 y 50 y que el número de herederos sea mayor que cero. Después de esa validación, se realizan los cálculos.

El programa muestra dos resultados importantes. En primer lugar, indica cuál será la superficie final que recibirá cada heredero después de todas las generaciones. En segundo lugar, imprime una lista con la evolución del reparto, generación por generación, para que se vea claramente cómo va disminuyendo la superficie conforme se divide.
