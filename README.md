# Proyecto Final UTN — Predicción de Churn en Telecomunicaciones (Grupo H)

Este proyecto corresponde al **Trabajo Final de la Diplomatura en Ciencia de Datos (UTN)**.  
El objetivo es **predecir la baja de clientes (churn)** en una empresa de telecomunicaciones mediante **modelos de machine learning** y evaluar la solución tanto desde el punto de vista **técnico** como de **negocio**.

---

## Objetivo

Desarrollar un modelo de **clasificación supervisada** que estime la probabilidad de baja de un cliente y permita a la empresa **priorizar acciones de retención**.  
Se implementaron métricas técnicas (ROC-AUC, PR-AUC, F1, Recall) y de negocio (Top-N, ROI proxy).

---

## Estructura del repositorio



---

## Dataset

- Fuente: [IBM Telco Customer Churn](https://www.kaggle.com/blastchar/telco-customer-churn)  
- Filas: 7043  
- Columnas: 21  
- Variable target: `Churn` (Yes/No)  

---

## Metodología

1. **EDA y limpieza**: tratamiento de valores faltantes, tipos de datos y unificación de categorías.  
2. **Preprocesamiento**: pipelines con imputación, escalado, codificación categórica y features de negocio (`services_count`, `tenure_band`, etc.).  
3. **Modelado**: Logistic Regression, Decision Tree, Random Forest, XGBoost.  
4. **Evaluación**: accuracy, precision, recall, F1, ROC-AUC, PR-AUC.  
5. **Interpretabilidad**: SHAP values.  

---

## Resultados

- Modelo final: **Regresión Logística**  
- Métricas (holdout, umbral calibrado ≈ 0,599):  
  - ROC-AUC ≈ 0,862   
  - Precisión ≈ 0,687  
  - Recall ≈ 0,6
  - F1 ≈ 0,641  

---

## Ejecución

### Local
```bash
pip install -r requirements.txt
jupyter notebook notebooks/Proyecto_final_grupo_H.ipynb
