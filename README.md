# Predicción de Ventas con Regresión Lineal Simple

## Resumen del Problema de Negocio

Este proyecto busca responder a una pregunta clave del departamento de marketing: **¿Cuál es el impacto cuantificable de la inversión en publicidad de TV sobre las ventas de nuestro producto?**

El objetivo es construir un modelo de Machine Learning que no solo prediga las ventas futuras basadas en la inversión, sino que también proporcione una interpretación clara del retorno de inversión (ROI) de este canal publicitario.

---

## Metodología

El análisis se realizó siguiendo un flujo de trabajo estándar de ciencia de datos:

1.  **Análisis Exploratorio de Datos (EDA):** Se cargó el dataset "Advertising" y se visualizó la relación entre la inversión en TV y las Ventas para confirmar la existencia de una tendencia lineal.
2.  **Modelado:** Se construyó un modelo de **Regresión Lineal Simple** utilizando `scikit-learn`, separando los datos en conjuntos de entrenamiento (70%) y de prueba (30%) para asegurar la generalización del modelo.
3.  **Evaluación:** El rendimiento del modelo se midió en el conjunto de prueba utilizando las métricas de Error Absoluto Medio (MAE) y Coeficiente de Determinación (R²).

---

## Resultados Clave

El modelo entrenado arrojó la siguiente ecuación:

`Ventas = 7.24 + 0.046 * Inversión_TV`

### Interpretación de Negocio:

* **Base de Ventas:** El modelo estima una base de ventas de **~7,240 unidades** sin ninguna inversión en publicidad de TV.
* **Retorno de Inversión (ROI):** Por cada **$1,000 adicionales** invertidos en anuncios de TV, se espera un aumento promedio de **46 unidades** en las ventas.

### Rendimiento del Modelo:

* **R² (R-squared):** `0.60` - El modelo es capaz de explicar el **60% de la variabilidad** en las ventas, lo cual indica que la TV es un predictor significativo pero no el único factor.
* **MAE (Error Absoluto Medio):** `2.2` - En promedio, las predicciones del modelo tienen un margen de error de **2,200 unidades**.

---

## Conclusiones y Próximos Pasos

El modelo de Regresión Lineal Simple confirma que la inversión en publicidad de TV tiene un impacto positivo y cuantificable en las ventas. Sin embargo, el R² de 0.60 sugiere que hay un 40% de la variabilidad que no estamos explicando.

El siguiente paso lógico es desarrollar un modelo de **Regresión Lineal Múltiple** que incorpore otras variables como la inversión en `Radio` y `Newspaper` para construir un predictor más robusto y completo.

---

## Cómo Ejecutar el Código

1.  Clonar este repositorio.
2.  Crear y activar un entorno virtual (se recomienda `conda`).
3.  Instalar las dependencias: `pip install pandas scikit-learn matplotlib seaborn jupyterlab`
4.  Ejecutar el Jupyter Notebook.
