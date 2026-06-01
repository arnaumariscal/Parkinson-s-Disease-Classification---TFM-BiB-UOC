# **Detección de Parkinson a partir de registros de voz utilizando aprendizaje supervisado**

Este repositorio peretenece al TFM del Máster en Bioestadística y Bioinformática (UOC), realizado por Arnau Mariscal Puig.

## 📑 Resumen:

La enfermedad de Parkinson (EP) es una enfermedad neurodegenerativa progresiva en la cual las alteraciones del habla llegan a afectar el 90% de los pacientes.
Distintos estudios han buscado procesar registros de voz mediante modelos de aprendizaje automático (ML) para apoyar un diagnóstico precoz de la EP.
Además, bases de datos como “Parkinson’s Disease Classification”, presentan desafíos metodológicos, como riesgo de fuga de datos, desbalance de clases y alta dimensionalidad del conjunto de datos. 

El objetivo principal de este estudio fue desarrollar y evaluar modelos supervisados de ML para la clasificación de sujetos con EP o sanos a partir de características acústicas.
Se evaluaron los algoritmos de clasificación: Regresión Logística, K-Nearest Neighbors, Support Vector Machines (kernels lineal y rbf), Random Forest y XGBoost.

## 🔬 Metodología:

Para afrontar la presencia de tres registros por individuo, se exploraron dos unidades de análisis: el conjunto de datos completo mediante validación cruzada Leave-One-Person-Out y un conjunto agregado que combinaba las tres muestras por paciente.
También se evaluaron estrategias de reducción de dimensionalidad, incluyendo mRMR, LinearSVC, PCA y selección de grupos de variables acústicas.
El desbalance de clases se abordó mediante el uso de MCC y F1-score como métricas principales, junto con la consideración de estrategias de sobremuestreo SMOTE y ponderación de clases

## 📚 Resultados:

El mejor rendimiento se obtuvo con Regresión Logística, alcanzando una exactitud de 0.873, F1-score de 0.918, MCC de 0.646 y AUC-ROC de 0.866.
Los grupos MFCC y TQWT proporcionaron la mayor capacidad discriminativa, mostrando un carácter complementario. 
El análisis SHAP confirmó que ambos grupos de características acústicas tuvieron también la mayor contribución.

## ⚙️ Ejecución:

Para clonar el repositorio, configurar el entorno y ejecutar el proyecto:

```bash
# 1. Clonar el repositorio 
git clone https://github.com/arnaumariscal/Parkinson-s-Disease-Classification---TFM-BiB-UOC
cd Parkinson-s-Disease-Classification---TFM-BiB-UOC

# 2. Instalación de dependencias
pip install -r requirements.txt

# 3. Ejecutar archivo ipynb principal
jupyter notebook "Parkinson's Disease Classification.ipynb"
```
