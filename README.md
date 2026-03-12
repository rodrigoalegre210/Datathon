<h1 align="center"> 🏠 Datathon: Real Estate Price Prediction (Colombia) </h1>

> **Proyecto Individual Nº2** - Etapa de Laboratorios (Henry Bootcamp)
> 
> **Rol:** Data Scientist / ML Engineer

---

## 📄 Descripción del Proyecto

Este proyecto se enfoca en el desarrollo de un modelo de **Machine Learning de Clasificación** para predecir si el precio de una propiedad inmobiliaria en Colombia se categoriza como "Caro" (1) o "Barato" (0). El flujo de trabajo abarca desde la limpieza profunda de datos geoespaciales hasta el entrenamiento de un modelo de clasificación robusto.

---

## 🛠️ Tecnologías Utilizadas

| Categoría | Herramientas |
|-----------|--------------|
| **Lenguaje** | Python (Pandas, Numpy, cmath) |
| **Machine Learning** | Scikit-learn (Decision Tree Classifier) |
| **Análisis Geoespacial** | Geopandas, Folium |
| **Visualización** | Seaborn, Matplotlib |

---

## ⚙️ Pipeline del Proyecto & Visualizaciones

### FASE 1: Análisis Exploratorio y Correlación
<p align="center">
  <img src="https://user-images.githubusercontent.com/105827215/199972744-6556c126-b30f-4bfb-8aaa-3575069be97f.png" alt="Matriz de Correlación" width="450">
  <br>
  <em>Visualización 1: Mapa de calor de correlación entre variables técnicas y el target.</em>
</p>

### FASE 2: Limpieza y Tratamiento de Outliers Geoespaciales
<p align="center">
  <img src="https://user-images.githubusercontent.com/105827215/199974696-1da94790-f421-4f84-817b-b96ff2ff9e88.png" alt="Outliers Geoespaciales" width="700">
  <br>
  <em>Visualización 2: Distribución geográfica antes y después de remover outliers de ubicación.</em>
</p>

### FASE 3: Distribución de Clases (Features vs Target)
<p align="center">
  <img src="https://user-images.githubusercontent.com/105827215/199975657-434b82d5-c798-4080-8620-4368edffbb63.png" alt="Relación Features y Target" width="450">
  <br>
  <em>Visualización 3: Dispersión de variables clave segmentadas por categoría de precio (Verde: Barato, Naranja: Caro).</em>
</p>

---

## 📊 Modelo y Resultados

Se implementó un **Árbol de Decisión (Decision Tree)** para la tarea de clasificación.

| Métrica | Resultado |
|---------|-----------|
| **Accuracy** | **89.96%** |
| **Recall** | **76.76%** |

---

<h3 align="center">🚀 Desarrollado por Rodrigo - Data Science & AI Engineer 🚀</h3>
