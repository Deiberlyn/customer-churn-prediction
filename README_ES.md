🌐 **Idioma:** [English](README.md) | Español

# Predicción de Abandono de Clientes

Proyecto de Machine Learning enfocado en predecir el abandono de clientes (*customer churn*) e identificar segmentos de clientes con mayor riesgo de abandono.

Este proyecto fue desarrollado como parte del **programa de Data Science de Henry** y combina análisis exploratorio de datos, aprendizaje supervisado, optimización de modelos, aprendizaje no supervisado e ingeniería de características para abordar un problema de negocio relacionado con la retención de clientes.

## Problema de Negocio

El proyecto se basa en un escenario ficticio de banca digital con **10,000 clientes activos** y una tasa anual de abandono de clientes de aproximadamente **20%**.

El objetivo es desarrollar un enfoque predictivo capaz de identificar a los clientes con mayor probabilidad de abandonar el banco, proporcionando información útil para apoyar estrategias de retención de clientes.

## Flujo del Proyecto

El proyecto fue desarrollado en tres etapas principales:

### 1. Análisis Exploratorio de Datos y Regresión Logística

- Análisis Exploratorio de Datos (EDA)
- Análisis de calidad de los datos
- Análisis del desbalance de clases
- Codificación de variables categóricas
- División de los datos en entrenamiento y prueba
- Escalado de características
- Regresión Logística como modelo base (*baseline*)
- Evaluación mediante métricas de clasificación

### 2. Modelos de Machine Learning y Optimización

Se entrenaron y compararon diferentes algoritmos de clasificación:

- Logistic Regression
- Random Forest
- XGBoost
- LightGBM
- CatBoost

El rendimiento de los modelos fue evaluado utilizando:

- Accuracy
- Precision
- Recall
- F1-Score
- ROC-AUC
- Matriz de Confusión

También se realizó optimización de hiperparámetros utilizando **Optuna**.

### 3. Aprendizaje No Supervisado e Ingeniería de Características

Se exploraron técnicas de segmentación de clientes utilizando:

- K-Means
- DBSCAN
- PCA
- t-SNE

El análisis de clustering se utilizó para identificar grupos de clientes con diferentes comportamientos de abandono.

Se creó una nueva característica, `cluster_risk_priority`, para incorporar información obtenida de la segmentación de clientes al análisis.

## Resultados Principales

El modelo base de Regresión Logística obtuvo:

- **Accuracy:** 80.80%
- **ROC-AUC:** 77.48%
- **Recall:** 18.67%

Después de comparar y optimizar modelos más avanzados:

- **XGBoost alcanzó un ROC-AUC de 86.79%**
- **LightGBM obtuvo el Recall más alto con 49.63%**

El análisis de importancia de características de XGBoost identificó las siguientes variables entre los predictores más relevantes:

- `IsActiveMember`: 27.39%
- `NumOfProducts`: 26.75%
- `Age`: 22.54%

La segmentación de clientes también permitió identificar un grupo de mayor riesgo asociado con clientes de Alemania, con una tasa de abandono de **32.44%**.

Estos resultados muestran cómo las técnicas de Machine Learning supervisado y no supervisado pueden complementarse para analizar el abandono de clientes y apoyar el desarrollo de estrategias de retención.

## Tecnologías

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- Statsmodels
- XGBoost
- LightGBM
- CatBoost
- Optuna
- Jupyter Notebook

## Estructura del Proyecto

```text
customer-churn-prediction/
│
├── data/
│   ├── Churn_Modelling.csv
│   └── datasets procesados
│
├── notebooks/
│   ├── 1_EDA_RegresionLogistica.ipynb
│   ├── 2_GradientBoosting_Optimizacion.ipynb
│   └── 3_AprendizajeNoSupervisado.ipynb
│
├── reports/
│   ├── Reporte_Modelos.pdf
│   └── Recomendaciones_Reporte_Modelos.pdf
│
├── .gitignore
├── requirements.txt
├── README.md
└── README_ES.md
```

## Instalación

Clona el repositorio:

```bash
git clone https://github.com/Deiberlyn/customer-churn-prediction.git
```

Crea y activa un entorno virtual y luego instala las dependencias necesarias:

```bash
pip install -r requirements.txt
```

Después, los notebooks pueden ejecutarse en orden desde el directorio `notebooks/`.

## Autora

**Deiberlyn Nin**

Data Science Junior  
Python | SQL | Machine Learning

- GitHub: https://github.com/Deiberlyn
- LinkedIn: https://www.linkedin.com/in/deiberlyn-nin-b893b1432/