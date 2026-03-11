🔄 Actualización V2 (Febrero 2026)

## Identificando Estrellas: Machine Learning y NBA 🏀🤖
Autor: Juan Pedro Zorrilla, D.A.-D.S.

Fecha: 11 de febrero de 2026

Este proyecto es una evolución directa de mi primer modelo de predicción. En esta Versión 2, implementé las siguientes mejoras:

Pipeline Robusto: Integración de StandardScaler y RandomForestClassifier en un Pipeline de Scikit-Learn.
Ajuste de Umbral: Reducción del umbral de decisión a 0.3 para capturar mejor a los jugadores "en la burbuja".
Descubrimiento del "Sesgo de Eficiencia": Se detectó y documentó cómo el modelo evalúa a los jugadores de alto uso (High Usage Rate) vs. alta eficiencia.


# 📋 Resumen del Proyecto
Este proyecto desarrolla un sistema de auditoría predictiva para las selecciones del NBA All-Star. Utilizando técnicas de Machine Learning, el modelo evalúa el rendimiento de los jugadores entre las temporadas 2014 y 2024 para determinar quién merece ser una "estrella" basándose exclusivamente en métricas de impacto y eficiencia, eliminando sesgos de popularidad o narrativa mediática.

__________________________________________
# 🎯 Objetivo
Construir un modelo de clasificación que asigne una probabilidad de All-Star a cada jugador, permitiendo identificar:

- Métricas clave: Qué estadísticas separan realmente a la élite del resto.

- Snubs (Omisiones): Jugadores con alto rendimiento estadístico que no fueron seleccionados.

- Sesgos del Modelo: Analizar por qué ciertos perfiles de alto volumen (como bases creativos) son evaluados de forma distinta a los perfiles de alta eficiencia.
_____________________________________________
# 🛠️ Stack Tecnológico
* Lenguaje: Python 3.x

* Bibliotecas: * nba_api: Extracción de datos en tiempo real.

* Pandas & NumPy: Procesamiento y limpieza de datos (ETL).

* Scikit-Learn: Construcción del modelo (Random Forest) y Pipelines de preprocesamiento.

* Visualización: Tableau (Dashboard interactivo).

______________________________________________
# 🧠 Metodología y Modelo
1. Extracción y ETL
Se recolectaron datos históricos utilizando el endpoint leaguedashplayerstats. Se realizó una limpieza profunda manejando valores nulos y filtrando jugadores con tiempo de juego poco representativo.

2. Ingeniería de Características (Feature Engineering)
Se seleccionaron métricas de Volumen (PTS, REB, AST) y de Impacto/Eficiencia (Plus-Minus, Porcentajes de tiro, Pérdidas).

3. El Algoritmo: Random Forest
* Se implementó un Random Forest Classifier dentro de un Pipeline de Scikit-Learn.

* Balanceo de Clases: Manejo de la disparidad entre All-Stars (aprox. 24 por año) y el resto de la liga (>400 jugadores).

* Umbral de Decisión: Se ajustó el umbral de probabilidad a 0.3 para capturar con mayor precisión a los candidatos "en la burbuja".

_________________________________________________
# 🔍 Hallazgos Críticos: El "Sesgo de Eficiencia"
Uno de los resultados más interesantes del modelo fue su comportamiento ante jugadores de alto uso de balón (Usage Rate):

* Líderes de Probabilidad: El modelo favorece a perfiles como Jayson Tatum, Giannis Antetokounmpo y Kevin Durant, quienes combinan alto puntaje con una eficiencia defensiva y de tiro excepcional.

* La Paradoja de los Generadores: Jugadores como Nikola Jokić y Luka Dončić obtuvieron probabilidades menores a las esperadas (10% - 25%).

* Análisis: El modelo actúa como un "crítico severo" que penaliza fuertemente las pérdidas de balón (TOV) y valora el Plus-Minus neto. Esto revela que la IA prioriza la "limpieza" estadística, mientras que el voto humano valora la creatividad y el volumen de juego.
__________________________________________

# 📊 Visualizaciones (Tableau)
El análisis se complementa con una Historia en Tableau que incluye:

* Scatter Plot: Relación entre volumen de puntos e impacto real en el juego.

* Duelo de Perfiles: Comparativa directa entre predicciones del modelo y selecciones históricas.

* Heatmap de Consistencia: Seguimiento de la jerarquía de las estrellas a través de las temporadas.

_______________________________________
# 🚀 Cómo ejecutarlo
Clona el repositorio:

Bash
git clone https://github.com/tu-usuario/nba-allstar-ml.git
Instala las dependencias:

Bash
pip install pandas numpy nba_api scikit-learn
Ejecuta el notebook NBA_v2.ipynb para generar el archivo de predicciones nba_allstar_predictions_FINAL.csv.

________________________________________
# 👨‍💻 Autor
Juan Pedro Zorrilla 
Analista de Datos apasionado por el deporte y la tecnología.

-- LinkedIn: [https://www.linkedin.com/in/jp-zorrilla-it/]

-- GitHub: [https://github.com/jp-zorrilla]



