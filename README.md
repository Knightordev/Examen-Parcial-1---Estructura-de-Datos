# Examen-Parcial-1---Estructura-de-Datos

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
