# hacer una simulacion o una grafica del machine learning model para visualizar los resultados y el rendimiento del modelo. Esto puede incluir graficos de precision, recall, F1-score, curvas ROC, y otras metricas de evaluacion. Ademas, se pueden generar visualizaciones de los datos de entrenamiento y prueba para entender mejor el comportamiento del modelo y detectar posibles problemas como verificar si hay desbalance de clases, outliers, o correlaciones entre variables. Se pueden utilizar librerias como Matplotlib, Seaborn, Plotly o Scikit-Learn para crear estas visualizaciones. y que muetre los resultados de manera clara y comprensible para los usuarios.
import matplotlib.pyplot as plt
import seaborn as sns
from sklearn.metrics import classification_report, confusion_matrix, roc_curve, auc

x = [0.1, 0.4, 0.35, 0.8]
plt.plot(x)
plt.title("Simulacion del modelo de Machine Learning")
plt.xlabel("Iteraciones")
plt.ylabel("Precision")
plt.show()
# simulacion de la curva ROC
y_true = [0, 0, 1, 1]
y_scores = [0.1, 0.4, 0.35, 0.8]
fpr, tpr, thresholds = roc_curve(y_true= y_true, y_score=y_scores)
plt.plot(fpr, tpr, color='blue', label='Curva ROC')
plt.xlabel('Tasa de falsos positivos ')
plt.ylabel('Tasa de verdaderos positivos ')
plt.title('Curva ROC')
plt.legend()
plt.show()
# simulacion de la matriz de confusion
y_pred = [0, 0, 1, 1]
cm = confusion_matrix(y_true=y_true, y_pred=y_pred)
sns.heatmap(cm, annot=True, fmt='d', cmap='blues')
plt.title('Matriz de confusion')
plt.show()
# simulacion del reporte de clasificacion
report = classification_report(y_true=y_true, y_pred=y_pred)
print("Reporte de clasificacion \n", report)
print("Simulacion de la curva ROC, matriz de confusion y reporte de clasificacion completada.")
# simulacion de la distribucion de los datos de entrenamiento y prueba
import numpy as np
#generar datos de ejemplo
x_train = np.random.normal(loc=0, scale=1, size=1000)
x_test = np.random.normal(loc=0, scale=1, size=1000)
plt.figure(figsize=(12, 6))
sns.histplot(x_train, color='blue', label='Datos de entrenamiento', kde=True, stat="density", linewidth=0)
sns.histplot(x_test, color='orange', label='Datos de prueba', kde=True, stat="density", linewidth=0)
plt.xlabel('valores')
plt.ylabel('Densidad')
plt.title('Distribucion de los datos de entrenamiento y prueba')
plt.legend()
plt.show()
print("Simulacion de la distribucion de los datos de entrenamiento y prueba completada.")
# simulacion de la correlacion entre variables
import pandas as pd
# generar un DataFrame de ejemplo
data = {
    'variable 1': np.random.normal(loc=0, scale=1, size=1000),
    'variable 2': np.random.normal(loc=0, scale=1, size=1000),
    'variable 3': np.random.normal(loc=0, scale=1, size=1000),

}
df = pd.DataFrame(data)
correlation_matrix = df.corr()
sns.heatmap(correlation_matrix, annot=True, cmap='coolwarm')
plt.title('Matriz de correlacion entre variables')
plt.show()
print("Simulacion de la correlacion entre variables completada.")
