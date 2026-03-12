<h1 align="center"> 🏠 Datathon: Real Estate Price Prediction (Colombia) </h1>

> **Proyecto Individual Nº2** - Etapa de Laboratorios (Henry Bootcamp)
> 
> **Rol:** Data Scientist / ML Engineer

---

## 📄 Descripción del Proyecto

Este proyecto consiste en el desarrollo de un modelo de **Machine Learning de Clasificación** para predecir si el precio de una propiedad inmobiliaria en Colombia entra en la categoría de "Caro" (1) o "Barato" (0), basándose en sus características físicas y ubicación geográfica. El flujo de trabajo abarca desde la limpieza profunda y el tratamiento de datos geoespaciales hasta el entrenamiento e interpretación de un modelo de clasificación robusto.

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

El desarrollo se estructuró en fases críticas, apoyadas por análisis visual para la toma de decisiones.

### FASE 1: Análisis Exploratorio y Correlación
Se realizó un estudio detallado de las características físicas de los inmuebles (baños, habitaciones, superficie, etc.) para entender su relación con el precio y seleccionar las *features* con mayor poder predictivo. La matriz de correlación fue fundamental en este paso.

<p align="center">
  <img src="https://user-images.githubusercontent.com/105827215/199972744-6556c126-b30f-4bfb-8aaa-3575069be97f.png" alt="Matriz de Correlación de Variables" width="450">
  <br>
  <em>Visualización 1: Mapa de calor mostrando la correlación entre características (lat, lon, rooms, bathrooms, etc.) y el target.</em>
</p>

### FASE 2: Limpieza y Tratamiento de Outliers Geoespaciales
Una parte crucial del EDA detectó ruido significativo en los datos de ubicación. Se identificaron **outliers geoespaciales** masivos (coordenadas erróneas situando propiedades de "Colombia" en Chile o Estados Unidos). Usando Geopandas y Folium, se filtraron estos registros para restringir el análisis exclusivamente al territorio colombiano, asegurando la integridad del modelo.

<p align="center">
  <img src="https://user-images.githubusercontent.com/105827215/199974696-1da94790-f421-4f84-817b-b96ff2ff9e88.png" alt="Outliers Geoespaciales" width="700">
  <br>
  <em>Visualización 2: Distribución geográfica antes y después de remover outliers de ubicación.</em>
</p>

### FASE 3: Distribución de Clases Pre-Modelado
Analizamos visualmente cómo interactúan las variables clave seleccionadas (`lat`, `lon`, `bathrooms`) con nuestra variable objetivo. Esto nos permitió confirmar visualmente cómo interactúan las variables de ubicación y servicios con la clasificación de precio.

<p align="center">
  <img src="https://user-images.githubusercontent.com/105827215/199975657-434b82d5-c798-4080-8620-4368edffbb63.png" alt="Relación de Features y Target" width="450">
  <br>
  <div style="background-color: #f9f9f9; padding: 10px; border-radius: 5px; border: 1px solid #ddd; display: inline-block;">
    <em>Visualización 3: Análisis de distribución de las clases 'Barato' (verde) y 'Caro' (naranja) respecto a variables clave. <br> (Texto sobre fondo claro para visibilidad en temas oscuros)</em>
  </div>
</p>

---

## 📊 Modelo y Resultados

Se implementó un **Árbol de Decisión (Decision Tree Classifier)** para la tarea de clasificación binaria. Este modelo evalúa atributos secuencialmente en nodos de decisión hasta llegar a una hoja que contiene la etiqueta correspondiente a esa instancia.

El modelo fue evaluado bajo las siguientes métricas de performance en el set de testeo:

| Métrica | Resultado | Fórmula |
|---------|-----------|---------|
| **Accuracy** | **89.96%** | $$\text{Accuracy} = \frac{TP + TN}{TP + TN + FP + FN}$$ |
| **Recall** | **76.76%** | $$\text{Recall} = \frac{TP}{TP + FN}$$ |

> [!IMPORTANT]
> Se obtuvieron resultados consistentes tanto en entrenamiento como en testeo, indicando un buen equilibrio sin *overfitting*.

---

## 📂 Estructura del Repositorio

* **`Analisis_ML_Colombia.ipynb`**: Notebook con el flujo completo de EDA, Limpieza, Feature Engineering y Modelado.
* **`datasets/`**: Carpeta que contiene los archivos de *train* y *test* originales (.csv).
* **`predicciones.csv`**: Archivo final con los resultados de la clasificación sobre el dataset de testeo.

---

<h3 align="center">🚀 Desarrollado por Rodrigo - Data Science & AI Engineer 🚀</h3>
