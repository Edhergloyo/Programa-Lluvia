# Programa-Lluvia
El programa que hicimos el lunes 31 de marzo cabrones


semana = ['Lunes', 'Martes', 'Miércoles', 'Jueves', 'Viernes', 'Sábado', 'Domingo']

class Poblacion:
    def __init__(self, nombre):
        self.nombre = nombre
        self.lluvia = []
        self.promedio_lluvia = 0  
        self.sumas = 0

    def pedir_lluvia(self):
        for dia in semana:
            lluvia = float(input(f'Ingrese los mm cúbicos de la población del día {dia}: '))
            self.lluvia.append(lluvia)

    def total_lluvia(self):
        self.sumas = sum(self.lluvia)

    def calcular_promedio(self):  
        self.promedio_lluvia = sum(self.lluvia) / len(self.lluvia)

    def mostrar(self):
        print(f'Nombre: {self.nombre}, Total Lluvia: {self.sumas}, Promedio: {self.promedio_lluvia}')

sjr = Poblacion("San Juan del Rio")
sjr.pedir_lluvia()
sjr.total_lluvia()
sjr.calcular_promedio()
sjr.mostrar()
