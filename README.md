# Challenge-TelecomX-parte-2
Descripción del Proyecto

Este proyecto de Machine Learning busca estimar la probabilidad de que un cliente cancele su servicio (churn) a partir del análisis de datos históricos relacionados con suscripciones, comportamiento de facturación y características demográficas.

Más allá de obtener un buen nivel de precisión en las predicciones, el objetivo principal es maximizar la métrica de Recall (Sensibilidad), con el fin de detectar la mayor cantidad posible de clientes con riesgo de abandono. De esta manera, el modelo puede aportar información útil para diseñar estrategias de retención y reducir la pérdida de clientes.

## 🛠️ TECNOLOGÍAS

Lenguaje de programación: Python 3.x

Análisis y manipulación de datos: pandas, numpy

Visualización de datos: matplotlib, seaborn

Machine Learning: scikit-learn (Random Forest, K-Nearest Neighbors, GridSearchCV)

Tratamiento de clases desbalanceadas: imbalanced-learn (SMOTE, RandomUnderSampler, Pipeline)

## ⚙️ METODOLOGÍA
Análisis Exploratorio de Datos (EDA)
Se realizó un análisis bivariado para examinar visualmente la relación entre diferentes características de los clientes y su probabilidad de cancelar el servicio, lo que permitió identificar patrones relevantes en los datos.

Preprocesamiento de Datos

Transformación de variables categóricas mediante One-Hot Encoding.

Normalización de variables numéricas utilizando StandardScaler.

Manejo del Desbalanceo de Clases (Pipeline Híbrido)
Para evitar problemas de data leakage, se implementó un pipeline estructurado que combina dos técnicas:

SMOTE, para generar ejemplos sintéticos de la clase minoritaria.

RandomUnderSampler, para reducir el número de observaciones de la clase mayoritaria.

Entrenamiento y Optimización de Modelos
Se entrenaron y compararon dos algoritmos principales:

K-Nearest Neighbors (KNN), basado en distancia entre observaciones.

Random Forest, un modelo de ensamble basado en árboles de decisión.

Los hiperparámetros se optimizaron mediante GridSearchCV, utilizando Recall como métrica principal para priorizar la detección de clientes en riesgo de abandono.
