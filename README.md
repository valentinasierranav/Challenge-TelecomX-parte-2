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

## Datos
El dataset incluye información de clientes, como:
- Antigüedad y tipo de contrato.
- Servicios contratados (Internet, Telefonía, etc.).
- Método de pago y cargos mensuales.
- Variables categóricas y numéricas relevantes para el análisis.

Se aplicó **preprocesamiento**, incluyendo limpieza de datos, creación de variables dummy y balanceo de la clase minoritaria usando **SMOTE + RandomUnderSampler**.

---

## Modelos Utilizados
1. **Random Forest**
   - Modelo principal por su equilibrio entre Recall y Precisión.
   - Maneja variables categóricas y continuas, y es robusto ante ruido.

2. **K-Nearest Neighbors (KNN)**
   - Buen Recall, pero baja Precisión, menos práctico para campañas costosas.

**Optimización de Hiperparámetros:**  
- Random Forest: `n_estimators`, `max_depth`, `min_samples_split`, `min_samples_leaf`  
- KNN: `n_neighbors`, `weights`, `p`

## Resultados
- **Random Forest** obtuvo el mejor desempeño general (F1-score y AUC más altos).  
- **Factores clave de cancelación**:
  - Contrato y antigüedad
  - Servicio de fibra óptica
  - Método de pago (Electronic check)
  - Sensibilidad al precio (Cargo total y mensual)

- **Visualizaciones incluidas**:
  - Curvas ROC con AUC
  - Gráficos de importancia de variables (Random Forest y KNN, con paleta `coolwarm`)

---

## Estrategias de Retención Propuestas
- Incentivar la migración a contratos de 1 o 2 años para clientes “Mes a mes” con más de 3 meses de antigüedad.
- Auditoría y mejora del servicio de fibra óptica, revisando caídas de red, velocidad y satisfacción de usuarios.
- Fomentar la domiciliación de pagos para reducir fricción y minimizar la probabilidad de cancelación.
- Gestionar los primeros 90 días de los nuevos clientes con llamadas de bienvenida, tutoriales y soporte prioritario.

