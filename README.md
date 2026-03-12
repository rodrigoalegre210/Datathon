<h1 align="center"> 🏠 Datathon: Real Estate Price Prediction (Colombia) </h1>

> **Proyecto Individual Nº2** - Etapa de Laboratorios (Henry Bootcamp)
> 
> **Rol:** Data Scientist / ML Engineer

---

## 📄 Descripción del Proyecto

Este proyecto aborda el desarrollo de un modelo de **Machine Learning de Clasificación** para predecir si el precio de una propiedad inmobiliaria en Colombia entra en la categoría de "Caro" (1) o "Barato" (0). El flujo de trabajo abarca desde la adquisición y limpieza profunda de datos (incluyendo análisis geoespacial) hasta el entrenamiento e interpretación de un modelo predictivo robusto.

---

## 🛠️ Tecnologías Utilizadas

| Categoría | Herramientas |
|-----------|--------------|
| **Lenguaje** | Python (Pandas, Numpy) |
| **Machine Learning** | Scikit-learn (Decision Tree Classifier) |
| **Análisis Geoespacial** | Geopandas, Folium |
| **Visualización** | Seaborn, Matplotlib |

---

## ⚙️ Pipeline del Proyecto & Visualizaciones Clave

El desarrollo se estructuró en fases críticas, apoyadas por análisis visual para la toma de decisiones.

### FASE 1: Análisis Exploratorio y Selección de Features

El primer paso fue entender la relación entre las características físicas de los inmuebles y la variable objetivo (precio). Se utilizó una matriz de correlación para identificar qué variables (como baños, habitaciones o superficie) tenían el mayor poder predictivo para definir si una propiedad es "Cara" o "Barata".

<p align="center">
  <img src="RUTA/A/TU/IMAGEN_1_CORRELACION.png" alt="Matriz de Correlación de Variables" width="500">
  <br>
  <em>Visualización 1: Matriz de calor mostrando la correlación entre características (lat, lon, rooms, etc.) y el target.</em>
</p>

### FASE 2: Limpieza Geoespacial Profunda

Una parte crucial del EDA detectó ruido significativo en los datos de ubicación. Se identificaron **outliers geoespaciales** masivos (coordenadas que ubicaban propiedades de "Colombia" en Chile o Estados Unidos). Usando Geopandas y Folium, se filtraron estos registros para restringir el análisis exclusivamente al territorio colombiano, asegurando la integridad del modelo.

<p align="center">
  <img src="RUTA/A/TU/IMAGEN_2_OUTLIERS_GEO.png" alt="Visualización de Outliers Geográficos" width="800">
  <br>
  <em>Visualización 2: Identificación y remoción de coordenadas erróneas fuera de Colombia.</em>
</p>

### FASE 3: Distribución de Clases Pre-Modelado

Antes de entrenar el modelo, se analizó la relación visual entre las features seleccionadas (ej. `lat`, `lon`, `bathrooms`) y la distribución de la variable `target` recién creada. Esto permitió confirmar visualmente cómo interactúan las variables de ubicación y servicios con la clasificación de precio.

<p align="center">
  <img src="RUTA/A/TU/IMAGEN_3_RELACION_TARGET.png" alt="Relación de Features y Target" width="500">
  <br>
  <em>Visualización 3: Análisis de distribución de las clases 'Barato' (verde) y 'Caro' (naranja) respecto a variables clave.</em>
</p>

---

## 📊 Modelo y Resultados

Se implementó un **Árbol de Decisión (Decision Tree Classifier)** para la tarea de clasificación binaria, dada su alta interpretabilidad y capacidad para manejar relaciones no lineales entre la ubicación y el precio.

Finalizado el entrenamiento, se obtuvieron las siguientes métricas de performance en el set de testeo:

| Métrica | Resultado | Fórmula |
|---------|-----------|---------|
| **Accuracy** | **89.96%** | $$\frac{TP + TN}{TP + TN + FP + FN}$$ |
| **Recall** | **76.76%** | $$\frac{TP}{TP + FN}$$ |

---

## 📂 Estructura del Repositorio

* **`Datathon_Inmuebles.ipynb`**: Notebook con el flujo completo de EDA, Limpieza, Feature Engineering y Modelado.
* **`datasets/`**: Carpeta que contiene los archivos de *train* y *test* originales.
* **`predicciones.csv`**: Archivo final con los resultados de la clasificación sobre el dataset de testeo.

---

<h3 align="center">🚀 Desarrollado por Rodrigo - Data Science & AI Engineer 🚀</h3>
