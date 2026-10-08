# Minería de Procesos e IA Predictiva para Auditoría y ROI: Caso City Football Group

El crecimiento de las redes multiclub en el mundo del fútbol ha aumentado mucho el volumen de traspasos internos. Este proyecto nace para resolver dos problemas de este modelo: auditar si las operaciones cumplen con las normativas de la FIFA, para ver si tienen sentido deportivo o son simple especulación financiera, y poder predecir si un fichaje será rentable antes de hacerlo, reduciendo el riesgo económico.

Para llevar a cabo el análisis, primero extraje y crucé más de un millón de registros históricos de Transfermarkt usando Pandas. Esto me permitió aislar los datos específicos del City Group y crear un registro de eventos limpio. Después, utilicé la librería PM4Py para aplicar minería de procesos y descubrir cómo operan realmente, midiendo los tiempos que los jugadores pasan en cada equipo y las diferentes rutas que siguen. 

Con esos datos, implementé una auditoría para comprobar si se respeta la norma de los 180 días mínimos por cesión. Finalmente, desarrollé un modelo predictivo comparando varios algoritmos (SVM, Random Forest y KNN) y usando solo variables previas al fichaje para que la predicción fuera realista y no tuviera sesgos.

Los resultados fueron muy reveladores. En la parte normativa, el modelo descubrió 251 rutas de cesión distintas y detectó que el nivel de cumplimiento es de apenas un 54%, encontrando más de 300 operaciones que se saltan el periodo mínimo de maduración. 

Por otro lado, el modelo predictivo que mejor funcionó fue la Máquina de Vectores de Soporte (SVM), alcanzando una precisión del 84% y un ROC AUC de 0.91. Lo más interesante a nivel de negocio es que el sistema funciona como un filtro sin falsos positivos, lo que significa que permite evaluar fichajes asegurando matemáticamente una probabilidad muy alta de conseguir un retorno de inversión neto superior al 10%.

Si quieres ejecutar el código en tu equipo, solo necesitas clonar el repositorio e instalar las dependencias con el archivo requirements.txt. Luego puedes abrir y ejecutar el cuaderno principal que está en la carpeta notebooks. Por temas de tamaño, los datos originales de Transfermarkt no están incluidos, pero sí he dejado el registro de eventos final que se usa para el análisis.
