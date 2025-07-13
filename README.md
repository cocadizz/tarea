# tarea
primer ejercicio donde la actividad se trata de adivinar el numero de 1 al 100
import random

def adivina_el_numero():
    numero_secreto = random.randint(1, 100)
    intentos = 0
    print("¡Adivina el número entre 1 y 100!")

    while True:
        try:
            adivinanza = int(input("Introduce tu número: "))
            intentos += 1

            if adivinanza < 1 or adivinanza > 100:
                print("Por favor, elige un número entre 1 y 100.")
            elif adivinanza < numero_secreto:
                print("Demasiado bajo. Intenta de nuevo.")
            elif adivinanza > numero_secreto:
                print("Demasiado alto. Intenta de nuevo.")
            else:
                print(f"🎉 ¡Correcto! Adivinaste el número en {intentos} intentos.")
                break
        except ValueError:
            print("Por favor, introduce un número válido.")

# Ejecutar el juego
adivina_el_numero()
