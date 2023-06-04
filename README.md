# Python_clase_1
Crear una matriz 3x3


import random

# Crear arreglo de 3x3 con elementos aleatorios del 0 al 100
arreglo = [[random.randint(0, 100) for _ in range(3)] for _ in range(3)]

# Funciones solicitadas
def promedio_elementos(arreglo):
    suma = sum(sum(fila) for fila in arreglo)
    elementos = len(arreglo) * len(arreglo[0])
    promedio = suma / elementos
    return promedio

def suma_elementos(arreglo):
    suma = sum(sum(fila) for fila in arreglo)
    return suma

def elemento_mayor(arreglo):
    mayor = max(max(fila) for fila in arreglo)
    return mayor

def elemento_menor(arreglo):
    menor = min(min(fila) for fila in arreglo)
    return menor

def mostrar_diagonal_principal(arreglo):
    diagonal = [arreglo[i][i] for i in range(len(arreglo))]
    return diagonal

# Imprimir el arreglo
for fila in arreglo:
    print(fila)

# Calcular y mostrar los resultados
print("Promedio de los elementos:", promedio_elementos(arreglo))
print("Suma de los elementos:", suma_elementos(arreglo))
print("Elemento mayor:", elemento_mayor(arreglo))
print("Elemento menor:", elemento_menor(arreglo))
print("Elementos de la diagonal principal:", mostrar_diagonal_principal(arreglo))
