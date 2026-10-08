# Minería de Procesos e IA Predictiva para Auditoría y ROI: Caso City Football Group

## Contexto del Proyecto
El crecimiento de las redes multiclub (Multi-Club Ownership) en el ecosistema del fútbol, como es el caso del City Football Group, ha incrementado significativamente el volumen de traspasos y cesiones internas. Este proyecto aborda dos retos principales de este modelo de negocio:
1. Auditar de manera empírica el cumplimiento normativo frente a las regulaciones de la FIFA, analizando si las operaciones obedecen a un desarrollo deportivo o a modelos de ingeniería financiera especulativa.
2. Predecir la viabilidad económica (Retorno de Inversión) de los fichajes antes de que se formalicen, con el objetivo de mitigar el riesgo de capital.

## Arquitectura y Metodología
El análisis se ha estructurado en cuatro fases principales:

- **Ingesta y Limpieza de Datos:** Extracción y cruce relacional de más de un millón de registros históricos del portal Transfermarkt utilizando Pandas. Se logró estructurar un Event Log unificado focalizado exclusivamente en la red del City Group.
- **Descubrimiento de Procesos:** Aplicación de algoritmos de Process Mining mediante la librería PM4Py para modelar la realidad operativa. Se utilizaron Heuristic Nets y Directly-Follows Graphs para evaluar las distintas rutas de cesión y medir los tiempos de retención por club.
- **Auditoría de Conformidad:** Implementación de lógicas de validación frente a la normativa de protección al jugador, enfocadas en la regla de permanencia mínima de 180 días.
- **Machine Learning Predictivo:** Desarrollo de un modelo de clasificación comparando algoritmos (SVM, Random Forest, KNN) y optimizándolos vía GridSearchCV. Se utilizaron únicamente variables de scouting previas al fichaje para prevenir sesgos de fuga de datos (Data Leakage).

## Resultados Clave
Los resultados del análisis se traducen en hallazgos directos para el control operativo y la inteligencia financiera:

- **Auditoría Normativa:** El modelado identificó 251 variantes de cesiones. La evaluación de conformidad arrojó un nivel de cumplimiento del 54.57%, detectando 333 operaciones de transferencia que incumplen el periodo de maduración de los 180 días.
- **Precisión Predictiva:** La Máquina de Vectores de Soporte (SVM) optimizada obtuvo una precisión global del 84.48% y un ROC AUC de 0.91.
- **Impacto de Negocio:** El sistema predictivo actúa como un filtro de riesgo que opera con cero Falsos Positivos. Esto permite evaluar inversiones garantizando una probabilidad matemática alta de obtener un ROI neto superior al 10%.

## Reproducibilidad
Para ejecutar el código y revisar el análisis:
1. Clona el repositorio en tu entorno local.
2. Instala las dependencias necesarias: `pip install -r requirements.txt`
3. Ejecuta el archivo Jupyter ubicado en la carpeta `notebooks/`.

*Nota: Los datos en bruto originales proceden de Kaggle (Transfermarkt Data). Por restricciones de tamaño, el repositorio incluye únicamente el Event Log final estructurado.*
