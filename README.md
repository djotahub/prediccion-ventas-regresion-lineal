# Análisis Predictivo y Optimización del Presupuesto de Marketing
*Un Caso de Estudio de Regresión Lineal Simple y Múltiple sobre el Dataset "Advertising"*

---

## 1. Planteamiento Estratégico (Business Case)

Este proyecto aborda una cuestión fundamental para la optimización del presupuesto de marketing: **cuantificar y comparar el retorno de inversión (ROI) de los diferentes canales publicitarios** para maximizar el impacto en las ventas.

El objetivo es desarrollar un modelo predictivo robusto que permita al liderazgo tomar decisiones informadas sobre la asignación de capital, basándose en evidencia cuantitativa.

---

## 2. Enfoque Analítico y Evolución del Modelo

Se implementó un flujo de trabajo iterativo para construir y refinar el modelo predictivo, garantizando la fiabilidad y la interpretabilidad de las conclusiones.

1.  **Modelo Base (Regresión Simple):** Se estableció una línea base inicial modelando las ventas únicamente en función de la inversión en TV.
2.  **Modelo Extendido (Regresión Múltiple):** Se incorporaron las variables de inversión en `Radio` y `Newspaper` para crear un modelo más completo.
3.  **Diagnóstico y Optimización:** Se realizó un análisis de correlación (multicolinealidad) para identificar predictores redundantes. Basado en los hallazgos, se eliminó la variable `Newspaper` para construir un modelo final más simple y eficiente sin sacrificar poder predictivo.

---

## 3. Hallazgos Cuantitativos: Comparativa de Modelos

La evolución del modelo demuestra una mejora significativa en el rendimiento. Los resultados del conjunto de prueba son los siguientes:

| Modelo | R² (Poder Explicativo) | MAE (Error Promedio) | Conclusión Clave |
| :--- | :--- | :--- | :--- |
| **1. Simple (solo TV)** | 0.67 | ± 2,275 unidades | La TV es un predictor importante, pero insuficiente por sí solo. |
| **2. Múltiple (3 Features)** | 0.90 | ± 1,198 unidades | **El modelo mejora drásticamente.** TV y Radio son drivers clave. |
| **3. Optimizado (TV + Radio)**| **0.90** | **± 1,192 unidades**| **El mejor modelo.** Igual de potente pero más simple y robusto. |

### Coeficientes del Modelo Final (Optimizado):

* **Intercepto:** 2.92 (base de ventas de ~2,920 unidades sin inversión).
* **Coeficiente `tv`:** 0.045
* **Coeficiente `radio`:** 0.188

### Interpretación Ejecutiva del Modelo Ganador:

* Por cada **$1,000** invertidos en **TV**, se espera un aumento promedio de **45 unidades** en ventas.
* Por cada **$1,000** invertidos en **Radio**, se espera un aumento promedio de **188 unidades** en ventas.

**Insight Crítico:** El canal de Radio tiene un ROI aproximadamente **4 veces superior** al de la TV, y la inversión en Periódicos (`Newspaper`) no tiene un impacto estadísticamente significativo cuando ya se consideran los otros dos canales.

---

## 4. Conclusión Estratégica y Recomendaciones

**Conclusión:** Se ha desarrollado un modelo de regresión lineal múltiple optimizado, capaz de explicar el **90% de la variabilidad en las ventas** con un alto grado de precisión.

**Recomendación:** Se recomienda al departamento de marketing reevaluar la asignación de presupuesto, priorizando la inversión en el canal de **Radio** debido a su significativamente mayor retorno de inversión. La inversión en Periódicos debería ser reconsiderada o auditada, ya que no demuestra un impacto directo en las ventas según este modelo.

---

## 5. Detalles Técnicos y Reproducibilidad

El análisis completo y el código se encuentran en el Jupyter Notebook del repositorio. El entorno y las dependencias requeridas para reproducir el análisis están documentadas en el mismo.
