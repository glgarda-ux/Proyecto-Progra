def main():
    print(" CALCULADORA HORA DE SALIDA ")

    # Entradas
    distancia = float(input("¿A cuántos km vives de tu destino? (ej: 8) "))
    hora, minuto = map(int, input("¿A qué hora entra tu clase? (ej: 7:30) ").split(":"))
    trafico = float(input("¿Cuántos minutos de tráfico? (ej: 20) "))

    # Cálculos
    tiempo_total = distancia * 2 + 5 + trafico
    minutos_clase = hora * 60 + minuto
    minutos_salida = minutos_clase - tiempo_total

    if minutos_salida < 0:
        print(" Deberías salir el día anterior ")
        return

    hora_salida = int(minutos_salida // 60)
    minuto_salida = int(minutos_salida % 60)

    print(f" Debes salir a las {hora_salida:02d}:{minuto_salida:02d}")
    print(f" Tiempo total de viaje: {int(tiempo_total)} minutos")


if __name__ == "__main__":
    main()

