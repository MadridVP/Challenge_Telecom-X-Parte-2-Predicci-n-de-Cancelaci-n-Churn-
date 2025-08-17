## Challenge_Telecom X Challenge – Parte 2: Predicción de Cancelación de Clientes (Churn)

Este proyecto forma parte del **Challenge de Ciencia de Datos** enfocado en el análisis y predicción de la **cancelación de clientes (churn)** en una empresa de telecomunicaciones, para desarrollar modelos predictivos capaces de prever qué clientes tienen mayor probabilidad de cancelar sus servicios.  La empresa quiere anticiparse al problema de la cancelación.

El objetivo es **preprocesar los datos, entrenar distintos modelos de Machine Learning y analizar los factores que más influyen en la decisión de cancelación**, proponiendo estrategias de retención basadas en resultados.

---

## Objetivos del Proyecto
1. **Preprocesamiento y Análisis Exploratorio**
   - Limpieza de datos (eliminación de columnas irrelevantes como IDs).
   - Transformación de variables categóricas con **One-Hot Encoding**.
   - Exploración de desbalance de clases en la variable objetivo.
   - Análisis de correlaciones y visualizaciones (boxplots, scatterplots).

2. **Entrenamiento de Modelos**
   - División en **train/test** (80/20).
   - Modelos seleccionados:
     - **Regresión Logística** (requiere normalización).
     - **Random Forest** (no requiere normalización).
   - Métricas de evaluación:
     - Exactitud (*Accuracy*).
     - Precisión.
     - Recall.
     - F1-score.
     - Matriz de confusión.

3. **Interpretación de Resultados**
   - Análisis de **coeficientes** en Regresión Logística.
   - Análisis de **importancia de variables** en Random Forest.
   - Identificación de los factores principales asociados al churn.
   - Propuestas de **estrategias de retención**.

---

## Estructura del Repositorio
---

## 🔎 Resultados principales

### Rendimiento de modelos
- **Regresión Logística**: 100% de accuracy, precision, recall y F1-score.  
   Posible sobreajuste (validar con cross-validation).
- **Random Forest**: Accuracy ≈ 99.6%, Precision = 100%, Recall ≈ 98.6%, F1 ≈ 99.3%.  
  Más realista y robusto para producción.

### Factores que aumentan la probabilidad de cancelación
- **Cargos mensuales altos**.  
- **Método de pago: Electronic check**.  
- **Facturación electrónica (paperless billing)**.  
- **Servicio de Internet por fibra óptica (Fiber optic)**.  
- **Clientes SeniorCitizen**.

### Factores que reducen la cancelación
- **Mayor antigüedad (tenure)**.  
- **Contratos de 1 o 2 años**.  
- **Servicios adicionales: OnlineSecurity, TechSupport**.  

---

## Estrategias de retención propuestas
- Incentivar **contratos de largo plazo** (bonos, meses gratis).  
- Ofrecer **descuentos o bundles** para clientes con cargos mensuales altos.  
- Migrar clientes de **Electronic check** a **pagos automáticos** con incentivos.  
- Fomentar adopción de **OnlineSecurity y TechSupport** (prueba gratuita inicial).  
- Mejorar comunicación de **facturación electrónica** (recordatorios claros y UX).  

---

## 🛠️ Tecnologías utilizadas
- Python 3
- Pandas, Numpy
- Matplotlib, Seaborn
- Scikit-learn (LogisticRegression, RandomForestClassifier, métricas)

---

## 📌 Conclusión
El análisis confirmó que los factores más determinantes del churn están relacionados con:
- **Precio (cargos altos)**,
- **Método de pago**,
- **Tipo de contrato**,
- **Servicios adicionales**,
- **Antigüedad del cliente**.

Los modelos lograron un desempeño excelente, siendo **Random Forest** el más confiable para producción.  
Con base en los insights obtenidos, se propusieron **acciones de retención específicas** para reducir la tasa de cancelación.

---

*Proyecto desarrollado como parte del Challenge de Ciencia de Datos – Telecom X (Parte 2).*


