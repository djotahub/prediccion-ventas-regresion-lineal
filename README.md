# Análisis Predictivo del Impacto Publicitario en Ventas
*Análisis de Regresión Lineal Simple sobre el Dataset "Advertising"*

---

## 1. Planteamiento Estratégico (Business Case)

El presente análisis aborda una cuestión fundamental para la optimización del presupuesto de marketing: **cuantificar el retorno de inversión (ROI) del canal de publicidad en televisión**.

El objetivo es desarrollar un modelo predictivo que permita al liderazgo tomar decisiones informadas sobre la asignación de capital, transformando el gasto publicitario de un centro de coste a una inversión medible y predecible.

---

## 2. Enfoque Analítico

Se implementó un flujo de trabajo riguroso, abarcando desde la exploración de datos hasta la evaluación del modelo, para garantizar la fiabilidad de las conclusiones.

* **Análisis Exploratorio (EDA):** Se validó la hipótesis de una correlación positiva entre la inversión en TV y las ventas mediante visualización de datos.
* **Modelado Estadístico:** Se aplicó un modelo de **Regresión Lineal Simple** utilizando la biblioteca `scikit-learn` para modelar la relación matemática entre las variables.
* **Validación del Modelo:** Para asegurar la capacidad de generalización del modelo a datos futuros, el dataset fue particionado en conjuntos de entrenamiento (70%) y de prueba (30%).

---

## 3. Hallazgos Cuantitativos y su Impacto en el Negocio

El modelo resultante proporciona insights claros y accionables, encapsulados en la siguiente ecuación predictiva:

> **Ventas** = 7.24 + 0.046 × **Inversión en TV**

### Interpretación Ejecutiva:

* **Línea Base de Ventas (Intercepto):** Se estima una base de ventas de **~7,240 unidades** que es independiente de la inversión en TV, atribuible a otros factores como la reputación de la marca y otros canales de marketing.

* **Retorno de Inversión del Canal (Coeficiente):** El hallazgo más crítico es que por cada **$1,000** adicionales invertidos en publicidad televisiva, el modelo predice un aumento promedio de **46 unidades** en las ventas.

### Fiabilidad del Modelo:

* **Poder Explicativo (R²):** **60%**. El modelo explica el 60% de la variabilidad en las ventas, confirmando que la inversión en TV es un motor significativo del rendimiento comercial.
* **Precisión Predictiva (MAE):** **± 2,200 unidades**. Las predicciones del modelo tienen un margen de error promedio de 2,200 unidades, un factor a considerar en la planificación de inventario y objetivos.

---

## 4. Conclusión Estratégica y Recomendaciones

**Conclusión:** La inversión en publicidad televisiva es un driver de ventas efectivo y su impacto es ahora cuantificable. El modelo actual sirve como una herramienta sólida para la planificación presupuestaria inicial.

**Recomendación:** Dado que el 40% de la variabilidad de las ventas aún no se explica, se recomienda proceder con el desarrollo de un **modelo de Regresión Múltiple**. La inclusión de datos de inversión en `Radio` y `Newspaper` permitirá una visión holística del ecosistema de marketing y, previsiblemente, aumentará la precisión y el poder explicativo de nuestros pronósticos.

---

## 5. Detalles Técnicos y Reproducibilidad

El análisis completo está disponible en el Jupyter Notebook (`tu_notebook.ipynb`). Para reproducir los resultados, se requiere un entorno Python 3.9+ con las siguientes dependencias principales:

* `pandas`
* `scikit-learn`
* `matplotlib`
* `seaborn`
