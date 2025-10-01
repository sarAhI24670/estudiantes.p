class Estudiante:
    def __init__(self, nombre, matricula, carrera):
        self.nombre = nombre
        self.matricula = matricula
        self.carrera = carrera
        self.calificaciones = []

    def agregar_calificacion(self, nota):
        self.calificaciones.append(nota)

    def calcular_promedio(self):
        if len(self.calificaciones) == 0:
            return 0
        return sum(self.calificaciones) / len(self.calificaciones)

    def mostrar_info(self):
        print(f"Nombre: {self.nombre}")
        print(f"Matrícula: {self.matricula}")
        print(f"Carrera: {self.carrera}")
        print(f"Promedio: {self.calcular_promedio():.2f}")
        print("-" * 30)  # separador visual


# ---- Bloque de prueba ----
if __name__ == "__main__":
    # Primer estudiante
    est1 = Estudiante("Ana Pérez", "A12345", "Ingeniería en Sistemas")
    est1.agregar_calificacion(90)
    est1.agregar_calificacion(85)
    est1.agregar_calificacion(100)

    # Segundo estudiante
    est2 = Estudiante("Luis Gómez", "B67890", "Administración")
    est2.agregar_calificacion(75)
    est2.agregar_calificacion(80)
    est2.agregar_calificacion(70)

    # Mostrar información de ambos
    est1.mostrar_info()
    est2.mostrar_info()
