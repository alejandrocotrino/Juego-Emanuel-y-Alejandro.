# Juego Batalla Naval

## Descripción
Este proyecto consiste en el desarrollo de un videojuego de batalla naval como trabajo final de la asignatura. El juego será implementado en los lenguajes de programación Python y C++.

## Objetivo
Desarrollar un juego funcional basado en las estrategias de programación vistas en clase, en el cual los jugadores puedan ubicar barcos en un tablero y realizar disparos por turnos hasta determinar un ganador.

## Características principales
- Tablero representado mediante matrices
- Sistema de turnos
- Ubicación de barcos
- Validación de disparos (impacto o fallo)
- Condición de victoria

## Tecnologías utilizadas
- Python
- C++
- GitHub para control de versiones

## Estado del proyecto
En desarrollo.
##  Avance del proyecto

En esta segunda entrega se implementó el uso de matrices, funciones y estructuras repetitivas (for) para comenzar el desarrollo del videojuego de batalla naval. Tambien logramos avanzar en la apertura de la ventana emergente para que el juego pueda ser ejecutado sin ningún problema. 

Se creó una función que permite generar y mostrar el tablero del juego utilizando una matriz, lo que facilita la organización de las posiciones y el control del estado del juego.

---

##  Código 

# Crear tablero vacío
def crear_tablero(tamano):
    tablero = []
    for i in range(tamano):
        fila = []
        for j in range(tamano):
            fila.append("~")  # agua
        tablero.append(fila)
    return tablero

# Mostrar tablero
def mostrar_tablero(tablero):
    for fila in tablero:
        print(" ".join(fila))

# Programa principal
tamano = 5
tablero = crear_tablero(tamano)

print("TABLERO INICIAL:")
mostrar_tablero(tablero)
#Juego del trabajo final
#Comenzaremos con la programación de la pantalla en la que se va a ver el juego
import pygame
pygame.init()
screen=pygame.display.set_mode((1280,720))
clock=pygame.time.Clock()
running = True
while running:
    for event in pygame.event.get():
        if event.type == pygame.QUIT:
            running =False 
    screen.fill((255,0,0))
    pygame.display.flip()
    clock.tick(60)
pygame.quit()
