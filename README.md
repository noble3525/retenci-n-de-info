#hacer ejercicios con datos n,s, y m que tenga una curva rock y que tenga una tabla de resultados, espero que sea asi ajjajaj;V
import numpy as np
import matplotlib.pyplot as plt
import pandas as pd 
import seaborn as sns
#poner el estilo de seaborn
sns.set(style="whitegrid")
#pedir al usuario que ingrese los valores de n, s y m, si los ingresa mal puñalada pirobo
n = int(input("Ingrese el valor de n:"))
s = int(input("Ingrese el valor de s:"))
m = int(input("Ingrese el valor de m:"))
#crear una funcion que genere una curva rock, matematicas no puede ser borki 
def generar_curva_rock(n, s, m):
    x = np.linspace(0, n, 100)
    y = s * np.sin(m * x)
    return x, y
#generar la curva rock, genero la curva de esto pero no el amor de ella ;(
x, y = generar_curva_rock(n, s, m)
#crear una tabla de resultados
resultados = pd.DataFrame({'x': x, 'y': y})
#mostrar la tabla de resultados, de que tanto migajee este año ajjajaja;V
print(resultados)
#graficar la curva rock, no se que poner.-. culpa de carlos y abelardo HP
plt.plot(x, y)
plt.title('Curva Rock')


plt.xlabel('x')
plt.ylabel('y')
plt.show()
Apuntes mejorados: Predicción con Machine Learning
1. Regresión lineal (fundamentos)
Para aprender, primero hay que definir matemáticamente qué significa equivocarse.
La solución matemática directa calcula los parámetros óptimos que minimizan el error (por ejemplo, el error cuadrático medio).
Un modelo lineal simple puede predecir la satisfacción de vida según el PIB. Al cambiar los parámetros, la línea de predicción también cambia.
2. Método del gradiente (Gradient Descent)
Se calculan las derivadas parciales de la función de costo.
El descenso consiste en dar un paso en la dirección en la que el costo disminuye.
Analogía: La única forma de bajar al valle es mirar hacia el norte e ir bajando “a ciegas”. Con las matemáticas, el proceso se vuelve seguro y controlado.
Existen tres variantes principales, que se diferencian por el tamaño del lote (batch size) y la velocidad:

Batch Gradient Descent: usa todo el conjunto de datos.
Mini-batch Gradient Descent: usa lotes pequeños. Optimiza la velocidad y aprovecha mejor la GPU.
Stochastic Gradient Descent (SGD): usa un solo ejemplo cada vez. “Rebota” mucho, lo que ayuda a escapar de mínimos locales.

Las rutas de los tres algoritmos en el espacio de parámetros son diferentes. El mini-batch avanza de forma más elegante y estable, y es el estándar de oro actual.
3. Regresión polinomial
Es un modelo lineal adaptado a datos más complejos mediante características elevadas (potencias) o combinaciones de las características existentes.
4. Curvas de aprendizaje
Son una herramienta diagnóstica muy útil:

Mesetas altas y muy juntas → diagnostican claramente subajuste (underfitting). El modelo es demasiado simple.
Gran brecha entre la curva de entrenamiento y la de validación → evidencia un sobreajuste grave (overfitting).

5. Regularización y parada temprana
Son técnicas para poner límites al modelo:

Regularización: fuerza a que los parámetros sean lo más pequeños posibles (L1, L2, etc.).
Parada temprana (Early Stopping): detiene el entrenamiento en el punto óptimo de error de validación (antes de que empiece a sobreajustar).

Ambas son tácticas muy usadas a nivel empresarial.

La parada temprana, en particular, es un “hermoso almuerzo gratis”: ahorra tiempo de cómputo y evita el sobreajuste sin necesidad de técnicas más complejas.
6. Modelos de clasificación
¿Cómo adaptar la optimización a clases discretas?
Se usan:

Regresión logística (clasificación binaria)
Softmax (clasificación multiclase)

Ambos permiten que un modelo lineal (o no lineal) produzca probabilidades y se entrene con funciones de costo adecuadas para clasificación.
