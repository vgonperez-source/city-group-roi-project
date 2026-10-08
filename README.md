# Minería de Procesos e IA Predictiva para Auditoría y ROI en Redes Multiclub

## Contexto del Proyecto
El crecimiento de las redes multiclub en el mundo del fútbol ha aumentado el volumen de traspasos internos. Este proyecto nace para resolver dos problemas de este modelo. Primero, necesitamos auditar si las operaciones cumplen con las normativas de la FIFA, para ver si tienen sentido deportivo o son pura especulación financiera. Segundo, necesitamos poder predecir si un fichaje será rentable antes de hacerlo, para reducir el riesgo económico.

## Arquitectura y Metodología
El análisis se ha dividido en cuatro fases principales de manera secuencial:

- Ingesta y limpieza de datos: Extraje y crucé más de un millón de registros históricos de Transfermarkt usando Pandas. Esto me permitió aislar los datos del City Group y crear un registro de eventos limpio.
- Descubrimiento de procesos: Utilicé la librería PM4Py para aplicar minería de procesos y modelar la realidad operativa. Pude medir los tiempos que los jugadores pasan en cada equipo y las diferentes rutas que siguen.
- Auditoría de conformidad: Implementé una lógica matemática para comprobar si las cesiones respetan la norma de los 180 días mínimos de permanencia.
- Machine Learning predictivo: Desarrollé un modelo de clasificación comparando algoritmos como SVM, Random Forest y KNN. Usé solo variables previas al fichaje para que la predicción fuera realista y no tuviera sesgos de fuga de datos.

## Resultados Clave
Los resultados obtenidos aportan valor directo tanto al control normativo como a la inteligencia financiera del club:

- Auditoría normativa: El modelo descubrió 251 rutas de cesión distintas y detectó que el nivel de cumplimiento es de apenas un 54%. Se encontraron más de 300 operaciones que se saltan el periodo mínimo de maduración de 180 días.
- Precisión predictiva: El modelo que mejor funcionó fue la Máquina de Vectores de Soporte, alcanzando una precisión del 84.48% y un ROC AUC de 0.91.
- Impacto de negocio: El sistema predictivo funciona como un filtro sin falsos positivos. Esto permite evaluar fichajes asegurando matemáticamente una probabilidad muy alta de conseguir un retorno de inversión neto superior al 10%.

## Reproducibilidad
Para ejecutar este código en tu propio equipo, solo necesitas seguir estos pasos:
1. Clonar este repositorio.
2. Instalar las dependencias ejecutando el comando pip install -r requirements.txt.
3. Abrir y ejecutar el cuaderno principal que está dentro de la carpeta notebooks.

Nota: Por restricciones de tamaño, los datos originales de Transfermarkt no están incluidos en la carpeta de datos, pero sí he dejado el registro de eventos final estructurado que se utiliza para el análisis.
