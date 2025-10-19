# Archivo README.md
# Guardalo como README.md

# Proyecto Parte III – Análisis y Modelado de Canciones en Spotify 2023

## 1. Descripción del proyecto
Este repositorio contiene el desarrollo del análisis y modelado sobre el dataset de canciones de la plataforma Spotify durante el año 2023. El objetivo es comprender y predecir la popularidad de una canción (medida por la cantidad de *streams*) a partir de sus características musicales y contextuales.

## 2. Estructura del repositorio
```
ProyectoParteIII+Gutierrez/
│
├── data/
│   └── spotify‑2023.csv        ← Dataset original (se recomienda conservar copia)
│
├── resultados/                 ← Carpeta con gráficos, tablas y exportaciones
│   ├── hist_streams.png
│   ├── dist_streams_vs_log.png
│   ├── top_artists.png
│   ├── heatmap_corr_extended.png
│   ├── feature_selection_summary.csv
│   ├── rf_feature_importances.csv
│   ├── linear_coefs.csv
│   └── conclusiones.txt
│
└── ProyectoParteIII+Gutierrez.ipynb  ← Notebook principal (análisis + modelado)
```

## 3. Tecnologías y dependencias
Las principales librerías utilizadas son:
- `pandas`, `numpy` para manipulación de datos
- `matplotlib`, `seaborn` para visualización
- `scikit‑learn` para selección de características y modelado
- `reportlab` para exportar informes en PDF (opcional)

Recomendación: instalar todas las dependencias mediante:
```bash
pip install -r requirements.txt
```

## 4. Flujo de trabajo (notebook)
1. Preparación del entorno y definición de rutas.
2. Carga y limpieza del dataset: conversión de tipos, manejo de valores nulos, creación de variable transformada `log_streams`.
3. Análisis exploratorio ampliado: distribución de streams, artistas más frecuentes, mapa de correlación.
4. Ingeniería de variables y preprocesamiento: selección de predictores, escalado, etc.
5. Selección de características (feature selection) mediante varios métodos (correlación, SelectKBest, LassoCV, Random Forest).
6. Modelado comparativo: Regresión Lineal y Random Forest, entrenados y evaluados con métricas como MAE, RMSE y R².
7. Validación y robustez: Cross‑validation y —opcional— búsqueda de hiperparámetros.
8. Interpretación, conclusiones y recomendaciones para trabajo futuro.

## 5. Hipótesis del estudio
Se plantea que las canciones con mayores niveles de energía, bailabilidad y presencia de artistas populares tienden a generar más reproducciones (streams). Asimismo, se espera que el modelo basado en árboles capture mejor las relaciones complejas que una regresión lineal.

## 6. Cómo ejecutar
1. Verificar que el archivo `spotify‑2023.csv` esté dentro de la carpeta `data/`.
2. Abrir el notebook `ProyectoParteIII+Gutierrez.ipynb` en Jupyter Lab / Jupyter Notebook.
3. Ejecutar todas las celdas de arriba hacia abajo. Se generarán los gráficos y los archivos dentro de `resultados/`.
4. Subir este repositorio a GitHub como entrega final.

## 7. Resultados esperados
Al finalizar, encontrarás:
- Gráficos de distribución y correlación que muestran relaciones entre métricas musicales y streams.
- Un archivo `feature_selection_summary.csv` que resume qué variables tienen mayor impacto según distintos métodos.
- Una comparación cuantitativa de desempeño entre modelos (Lineal vs Random Forest).
- Un archivo `conclusiones.txt` que recoge las interpretaciones de los resultados y posibles mejoras.

## 8. Contacto
Autor: **Pablo Gutierrez**  
Repositorio GitHub: [Enlace a tu repositorio](https://github.com/)  
(Completar con tu perfil y contacto si lo deseas)


# Archivo requirements.txt
# Guardalo como requirements.txt
pandas==2.2.0
numpy==1.26.5
matplotlib==3.8.1
seaborn==0.12.3
scikit-learn==1.3.2
reportlab==4.0.2

