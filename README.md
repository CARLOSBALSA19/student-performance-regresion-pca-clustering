# Predicción de Rendimiento Académico: Enfoque Híbrido de Regresión, PCA y Clustering

Este proyecto aborda un problema de **regresión supervisada** utilizando el dataset `enhanced_student_habits_performance_dataset.csv`. El objetivo principal es predecir variables numéricas vinculadas al rendimiento académico y hábitos de los estudiantes, evaluando una hipótesis metodológica clave: **¿Mejora el rendimiento de los modelos si segmentamos los datos en clústeres y entrenamos un modelo específico para cada uno, en comparación con un único modelo global?**

## 🛠️ Stack Tecnológico & Técnicas
* **Lenguaje:** Python (Jupyter Notebook `.ipynb`).
* **Manipulación de Datos & EDA:** `pandas`, `numpy`.
* **Visualización Avanzada:** `matplotlib`, `seaborn`.
* **Machine Learning No Supervisado:** Reducción de Dimensionalidad con **PCA (Análisis de Componentes Principales)** y Clustering con **K-Means**.
* **Machine Learning Supervisado (Regresión):** Árboles de Decisión para Regresión y **Redes Neuronales Artificiales (ANN)**.

---

## Arquitectura Metodológica del Proyecto

El flujo de trabajo se divide en dos fases principales bien diferenciadas para contrastar la estrategia de modelado:

### Fase A: Ingeniería de Características, Reducción Dimensional y Clustering
1. **Análisis Exploratorio (EDA):** Revisión de distribuciones numéricas, medias, medianas, tratamiento de variables categóricas y análisis de correlación inicial para entender los factores que impactan al estudiante.
2. **Reducción de la Dimensión (PCA):** Aplicación de PCA para condensar la varianza del conjunto de datos en componentes principales, eliminando problemas de multicolinealidad y reduciendo el ruido.
3. **Segmentación mediante K-Means:** Aplicación del algoritmo de clustering sobre el espacio transformado por el PCA para agrupar a los estudiantes en subgrupos homogéneos según sus perfiles de hábitos y rendimiento.

### Fase B: Modelado Predictivo y Validación Comparativa
Con los clústeres definidos, se implementan y evalúan dos estrategias de entrenamiento:
* **Estrategia Global:** Entrenamiento de un único modelo predictivo utilizando la totalidad del conjunto de datos.
* **Estrategia Segmentada (Por Clúster):** Entrenamiento de modelos independientes para cada uno de los clústeres generados en la Fase A, permitiendo que el algoritmo se especialice en los patrones de cada subgrupo.
* **Modelos Evaluados:** Implementación, ajuste y optimización de **Árboles de Decisión** y **Redes Neuronales (ANN)**, comparando sus métricas de error para validar la efectividad de la segmentación previa.
