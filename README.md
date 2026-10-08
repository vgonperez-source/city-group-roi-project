# Minería de Procesos & IA Predictiva para Auditoría y ROI (City Football Group) 2026

![Python](https://img.shields.io/badge/Python-3.11-blue)
![Pandas](https://img.shields.io/badge/Pandas-Data_Wrangling-yellow)
![PM4Py](https://img.shields.io/badge/PM4Py-Process_Mining-orange)
![Scikit-Learn](https://img.shields.io/badge/Scikit_Learn-Machine_Learning-green)

## 📌 Contexto y Problema
En el ecosistema del fútbol moderno, las redes multiclub (Multi-Club Ownership) como el **City Football Group** operan con un volumen de traspasos masivo entre sus franquicias satélite. 
El objetivo de este proyecto es doble:
1. **Auditar empíricamente la ingeniería financiera y el acaparamiento especulativo** frente a la normativa de protección de la FIFA.
2. **Predecir la viabilidad económica (ROI)** de los nuevos fichajes en el "Momento Cero" (antes de la firma) para mitigar el riesgo de inversión.

## 🛠 Arquitectura y Pipeline de Datos
1. **Data Wrangling (Pandas):** Ingesta y cruce relacional (*Left Joins*) de +1M de registros históricos de Transfermarkt para construir un *Event Log* unificado de la red City Group.
2. **Process Discovery (PM4Py):** Modelado de la realidad (*Heuristic Nets* y *Directly-Follows Graphs*) evaluando variantes de cesión y tiempos de retención por franquicia.
3. **Auditoría de Conformidad (Compliance):** Reglas matemáticas de validación frente a la normativa de 180 días mínimos por cesión.
4. **Machine Learning Predictivo:** Entrenamiento y optimización vía *GridSearchCV* de un benchmark de clasificadores (SVM, Random Forest, KNN) aislando variables previas al fichaje para evitar fuga de datos (*Data Leakage*).

## 📊 Resultados y Business Impact

- **Auditoría Normativa:** Se aislaron **251 variantes de cesión**, evidenciando un modelo de negocio altamente especulativo con un **54.57% de conformidad**. Se detectaron **333 movimientos "exprés"** (cesiones puente ilegales de menos de 180 días).
- **IA Predictiva:** La Máquina de Vectores de Soporte (SVM) optimizada obtuvo una **precisión global del 84.48%** y un **ROC AUC Score de 0.91**.
- **Impacto Económico:** El modelo actúa como un blindaje financiero operando con **0 Falsos Positivos**, recomendando automáticamente descartar o aprobar operaciones para garantizar matemáticamente un **ROI neto > 10%**.

## 🚀 Cómo reproducir este proyecto
1. Clona el repositorio.
2. Instala las dependencias:
   ```bash
   pip install -r requirements.txt
   ```
3. Ejecuta el Jupyter Notebook interactivo ubicado en la carpeta `notebooks/`.

*(Nota: Los datasets en bruto se obtienen de Kaggle Transfermarkt Data, aquí solo se expone el Event Log final para la minería de procesos).*
