El plano del machine learning
¿Cuál es su valor?
Automatización: permite automatizar tareas que antes requerían intervención humana.
Predicción: puede analizar datos históricos para predecir comportamientos futuros, como ventas, demanda o riesgos.
Toma de decisiones: ayuda a las empresas a tomar decisiones basadas en datos.
Detección de patrones: encuentra relaciones o comportamientos difíciles de identificar manualmente.
Personalización: permite ofrecer recomendaciones adaptadas a cada usuario, como Netflix, YouTube o Spotify.
Eficiencia: puede procesar grandes cantidades de información rápidamente.
Innovación: permite desarrollar aplicaciones como reconocimiento facial, asistentes virtuales, detección de fraude y vehículos autónomos.
El machine learning puede excavar tan profundo entre los datos que puede encontrar tendencias ocultas
Puede encontrar patrones invisibles para los humanos
1. Flujos de datos

Un flujo de datos (data stream) es cuando los datos llegan continuamente, en lugar de tenerlos todos disponibles desde el principio.

Ejemplo:
Una aplicación recibe constantemente datos de usuarios:

Usuario → dato → modelo → predicción → nuevo dato → modelo...

Esto es útil cuando los datos cambian constantemente, como precios, sensores, tráfico o transacciones.
2. Ritmo de aprendizaje (Learning Rate)

El ritmo de aprendizaje indica qué tan grandes son los cambios que hace el modelo al aprender.

Ritmo alto: aprende rápidamente, pero puede pasarse de la solución adecuada.
Ritmo bajo: aprende lentamente, pero puede ser más estable.
Ritmo adecuado: permite llegar progresivamente a un buen modelo.

Por ejemplo, si el modelo tiene un error:

Error → ajuste → menor error → ajuste → menor error

El learning rate determina qué tan grande es cada ajuste.
3. Aprendizaje por lotes (Batch Learning)

En Batch Learning, el modelo recibe un conjunto de datos completo y aprende utilizando ese lote.

Ejemplo:

10.000 registros → entrenamiento → modelo actualizado

Después se puede volver a entrenar cuando se tengan nuevos datos.

Ventaja: puede ser eficiente para grandes conjuntos de datos almacenados.
Desventaja: no se adapta inmediatamente a nuevos datos.
4. Aprendizaje en línea (Online Learning)

En Online Learning, el modelo aprende poco a poco conforme llegan los datos.

Ejemplo:

Dato 1 → aprende
Dato 2 → aprende
Dato 3 → aprende
Dato 4 → aprende

Es especialmente útil cuando existe un flujo continuo de información.

Ventaja: se adapta rápidamente a cambios.
Desventaja: si recibe datos incorrectos o problemáticos, estos pueden afectar el modelo
