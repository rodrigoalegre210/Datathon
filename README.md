<h1 align="center"> 🏠 Datathon: Real Estate Price Prediction (Colombia) </h1>

> **Proyecto Individual Nº2** - Etapa de Laboratorios (Henry Bootcamp)
> 
> **Rol:** Data Scientist / ML Engineer

---

## 📄 Descripción del Proyecto

Este proyecto consiste en el desarrollo de un modelo de **Machine Learning de Clasificación** para predecir si el precio de un inmueble en Colombia se categoriza como "Caro" o "Barato" en función de sus características físicas y ubicación geográfica. El reto principal fue el tratamiento de datos espaciales y la optimización de un modelo de clasificación para obtener métricas de precisión competitivas.

### Objetivos Clave:
* **Feature Engineering:** Creación de una variable objetivo (target) basada en el umbral de precios.
* **Geospatial Cleaning:** Detección y eliminación de outliers geográficos (coordenadas fuera del territorio colombiano).
* **Modelado Predictivo:** Implementación y entrenamiento de un clasificador basado en árboles de decisión.

---

## 🛠️ Tecnologías Utilizadas

| Categoría | Herramientas |
|-----------|--------------|
| **Lenguaje** | Python (Pandas, Numpy) |
| **Machine Learning** | Scikit-learn |
| **Análisis Geoespacial** | Geopandas, Folium |
| **Visualización** | Seaborn, Matplotlib |

---

## ⚙️ Pipeline del Proyecto

### 1. Limpieza y Análisis Exploratorio (EDA)
Se realizó una limpieza profunda enfocada en la integridad de los datos:
- **Tratamiento de Outliers:** Identificación de errores de carga en coordenadas (`lat`, `lon`) que ubicaban propiedades fuera de Colombia.
- **Análisis de Correlación:** Estudio de la relación entre variables dimensionales (habitaciones, baños, superficie) y el precio.

<p align="center">
  <img src="https://user-images.githubusercontent.com/105827215/199972744-6556c126-b30f-4bfb-8aaa-3575069be97f.png" alt="Matriz de Correlación" width="450">
</p>

### 2. Ingeniería de Características
- **Variable Target:** Se transformó la variable continua `price` en una categoría binaria: **1 (Caro)** y **0 (Barato)**.
- **Codificación:** Aplicación de técnicas de transformación para la columna `property_type`, permitiendo al modelo procesar variables categóricas.

### 3. Modelo de Clasificación (Decision Tree)
Se optó por un **Árbol de Decisión** debido a su capacidad para manejar relaciones no lineales y su alta interpretabilidad. El modelo evalúa atributos en nodos de decisión hasta llegar a una clasificación final en las hojas.



---

## 📈 Resultados y Métricas

El modelo fue evaluado bajo las métricas de **Accuracy** y **Recall** para asegurar un equilibrio entre la precisión global y la capacidad de detectar correctamente las propiedades "caras".

| Métrica | Resultado |
|---------|-----------|
| **Accuracy** | **89.95%** |
| **Recall** | **76.76%** |

$$\text{Accuracy} = \frac{TP + TN}{TP + TN + FP + FN}$$

---

<h3 align="center">🚀 Desarrollado por Rodrigo - Data Science & AI Engineer 🚀</h3>
