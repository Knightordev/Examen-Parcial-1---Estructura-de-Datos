# Examen-Parcial-1---Estructura-de-Datos
EJERCICIO 1
Este ejercicio cuenta con dos arreglos, el primero almacena los nombres y el segundo la longitud  de los mismos, después en un ciclo While el programa te pide ingresar la cantidad de nombres a escribir, en ese mismo ciclo evalúa con las funciones Try y Except que el valor ingresado sea un entero, después de salir del ciclo While inicia un ciclo for que se repite tantas veces como nombres vas a digitar, dicho ciclo for te pide los ya mencionados nombres y a su vez calcula su longitud y las guarda en el arreglo longitud y al final, con ayuda de un ciclo for se imprimen los nombres y sus longitudes.

EJERCICIO 2
Se creo una clase llamada temperatura el cual tiene
una lista de temperaturas no añadidas,

método privado de añadir temperatura insertando una temperatura a la lista de temperaturas

método privado promedio de temperatura
donde se suma la lista de temperaturas utilizando sum dividiendo entre  el tamaño de esa misma temperatura (con 2 decimales)

método privado obtener temperatura máxima la cual devuelve la temperatura máxima, utiliza max que devuelve el valor máximo de un arreglo

método privado obtener temperatura mínima la cual devuelve la temperatura mínima, utiliza min que devuelve el valor mínimo de un arreglo

método privado días arriba del promedio, el cual crea una lista en donde se agregan cada una de las temperaturas mayores al promedio, y devuelve el tamaño de esa lista

método privado que agrega temperaturas 7 veces siendo las temperaturas flotantes de 2 decimales y utilizando el método privado de añadir temperatura

método privado para obtener información que imprime los valores devueltos de los métodos privados, temperatura promedio, temperatura máxima, temperatura mínima, y días arriba de la temperatura promedio

método publico main el cual usa el método privado de agregar 7 temperaturas y el método privado de obtener información

EJERCICIO 4:
import random 

longitud = int(input("Ingresa la longitud del vetor: "))

a = [None] * longitud     se crean vectores vacíos con una cantidad de espacios definidos según haya ingresado el usuario
b = [None] * longitud
sumando = [None] * longitud 
restando = [None] * longitud

for i in range(longitud):                                       Se llenan los vectores usando la cantidad de espacios definidos y un rango de -100 a 100
    a[i]=random.randint (-100,100)

    b[i]=random.randint (-100,100)

for i in range(longitud):                        Se suma y se resta a y b usando[i] para que se recorrer y sumar los valores individualmente
    sumando[i] = a[i] + b[i]
    restando[i] = a[i] - b[i]

opciones = int(input("Seleccione que vector desea ver,elija entre 1=a, 2=b, 3=c sumando a y b, 4=c restando a y b: ")) se le asignan números a cada letra y se usan if para imprimir lo q pide y validando si esta pidiendo una opción posible

if opciones == 1:
    print("vector A:",a)

elif opciones == 2:
    print("vector B:", b)

elif opciones == 3:
    print("vector c sumando a y b:", sumando)

elif opciones == 4:
    print("vector c restando a y b:", restando)
    exit()

else:
    print("no es valida esta opcion")
    exit()
