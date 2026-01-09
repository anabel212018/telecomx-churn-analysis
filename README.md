# telecomx-churn-analysis
Telecom X – Análisis de Evasión de Clientes 
Descripción del proyecto

Este proyecto tiene como objetivo analizar la evasión de clientes (churn) en Telecom X, identificando los factores que influyen en la cancelación del servicio.
A través de técnicas de análisis exploratorio de datos (EDA) y modelos de machine learning, se busca generar insights que permitan apoyar estrategias de retención de clientes.

El proyecto forma parte del Challenge de Data Science.

🎯 Objetivos

Comprender la estructura y características del conjunto de datos.

Detectar y corregir inconsistencias en los datos.

Analizar patrones asociados a la evasión de clientes.

Entrenar y evaluar modelos predictivos de churn.

Comparar modelos y seleccionar el más eficiente desde una perspectiva de negocio.

📂 Estructura del proyecto
📁 TelecomX-Churn-Analysis
│
├── 📓 TelecomX_Churn_Analysis.ipynb   # Notebook principal con todo el análisis
├── 📄 README.md                      # Documentación del proyecto

Fuente de datos

Los datos se obtienen desde una API pública en formato JSON:

https://raw.githubusercontent.com/alura-cursos/challenge2-data-science-LATAM/refs/heads/main/TelecomX_Data.json


El dataset contiene información demográfica, contractual y financiera de los clientes, así como la variable objetivo Churn, que indica si el cliente canceló el servicio.

Tecnologías utilizadas

Python 3
Google Colab
Pandas – Manipulación y limpieza de datos
NumPy – Operaciones numéricas
Matplotlib / Seaborn – Visualización de datos
Scikit-learn – Modelado y evaluación


Metodología
Extracción (Extract)
  Carga de datos desde la API en formato JSON.
  Conversión a DataFrame para su análisis.

Transformación de los datos (Transform)
  Exploración de columnas y tipos de datos.
  Detección y tratamiento de valores nulos e inconsistencias.
  Conversión de variables numéricas almacenadas como texto.
  Creación de la variable Cuentas_Diarias a partir de la facturación mensual.
  Estandarización de variables numéricas.
  Codificación de variables categóricas (One-Hot Encoding).

 Carga y Análisis (Load & Analysis)
  Análisis descriptivo de las variables.
  Análisis de la distribución de churn.
  Evaluación de churn según variables categóricas y numéricas.
  Visualización de patrones relevantes.

 Modelado
 Se entrenaron y evaluaron dos modelos de clasificación:
  Regresión Logística
   Utilizada como modelo base.
   Buen desempeño general (accuracy ≈ 0.80).
   Recall moderado para la clase churn.

 Árbol de Decisión
   Profundidad limitada para evitar overfitting.
   Mejor desempeño en recall de la clase Churn (1).
   Seleccionado como el modelo más eficiente desde el punto de vista del negocio.

  Métricas de evaluación

  Accuracy

  Precision

  Recall

  F1-score

  Matriz de confusión

La métrica priorizada fue Recall de la clase Churn (1), ya que permite identificar la mayor cantidad posible de clientes en riesgo de cancelación.

Conclusiones

El churn presenta patrones claros asociados a variables contractuales y de gasto.

Un alto accuracy no garantiza una buena detección de clientes que abandonan.

El Árbol de Decisión mostró mejor capacidad para identificar clientes en riesgo.

Priorizar el recall permite tomar acciones preventivas más efectivas.


Recomendaciones

Implementar modelos orientados a maximizar el recall de churn.

Utilizar los resultados para acciones de retención temprana.

Explorar ajustes de umbral y otros modelos en futuras iteraciones.


Próximos pasos (trabajo futuro)

Optimización de hiperparámetros.

Prueba de modelos adicionales (Random Forest, XGBoost).

Análisis de correlación más profundo.

Implementación de un pipeline de producción.

Autor
Magaly Anabel Hernández
