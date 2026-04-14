
# 🚑 Predicción de la Gravedad de Accidentes de Tráfico en Madrid

## 📂 Estructura del repositorio

El repositorio está organizado en diferentes carpetas que reflejan las principales fases del proyecto de análisis y modelado:
├── datasets/
├── informes/
├── notebooks/
├── Final model-*.zip


### 📁 `datasets/`
Contiene todos los datos utilizados en el proyecto:

- **Raw data**: datos originales sin procesar  
- **Processed data**: datos limpios y transformados para el modelado  
- **Datos para Power BI**: datasets específicos preparados para la visualización en el dashboard  


### 📁 `informes/`
Incluye toda la documentación y entregables del proyecto:

- 📊 Presentación final  
- 📄 Informe técnico  
- 📈 Dashboard de Power BI  


### 📁 `notebooks/`
Contiene los notebooks desarrollados en Python:

- Procesamiento y limpieza de datos  
- Feature engineering  
- Análisis exploratorio  
- Preparación de datos para modelado  


### 📦 `Final model-*.zip`
Archivo comprimido que contiene el modelo final entrenado, listo para su uso o despliegue.


## 📌 Descripción del proyecto

Este proyecto tiene como objetivo predecir la gravedad de los accidentes de tráfico en Madrid utilizando técnicas de Machine Learning.

El propósito principal es aportar valor desde el punto de vista de negocio, permitiendo:

Optimizar la asignación de recursos médicos
Mejorar la capacidad de respuesta ante emergencias
Identificar zonas y condiciones de mayor riesgo

## 🎯 Objetivo
Desarrollar un modelo predictivo capaz de estimar la gravedad de un accidente en función de variables como:

- Condiciones meteorológicas
- Hora y fecha
- Tipo de vehículo
- Ubicación
- Factores contextuales del accidente

## 📊 Dataset
Los datos utilizados provienen de:

- Portal de datos abiertos del Ayuntamiento de Madrid (accidentes de tráfico) (https://datos.madrid.es/)
- API de clima (OpenWeather) (https://openweathermap.org/)

## 🔧 Feature Engineering
Se han creado nuevas variables para enriquecer el dataset:

- festivo / no festivo
- fin de semana
- hora punta
- mes
- estación
- franja horaria
- día / noche
- Variables derivadas del clima
- Codificación de variables categóricas (One-Hot, Target Encoding)

## ⚙️ Tecnologías utilizadas
- Python
- Pandas / NumPy
- Scikit-learn
- Imbalanced-learn (SMOTE)
- Power BI
- Jupyter Notebook

## 🧠 Modelado
Se han utilizado modelos de tipo ensemble basados en árboles:

- Random Forest
- Gradient Boosting
  
## 🔍 Técnicas aplicadas
- Validación cruzada
- Grid Search (optimización de hiperparámetros)
- Balanceo de clases con SMOTE
- Ajuste del umbral de decisión
- Evaluación con métricas robustas (especialmente F1-score)
- 
## ⚖️ Comparación de modelos
Se compararon ambos modelos en base a su rendimiento:
- Gradient Boosting	tiene una capacidad predictiva ligeramente mejor

👉 El modelo seleccionado fue Gradient Boosting, ya que obtuvo mejores resultados en términos de F1-score, especialmente en clases minoritarias.

## 📈 Resultados
El modelo logra capturar patrones relevantes en la gravedad de los accidentes
Variables como:
- Tipo de vehículo (especialmente motocicletas)
- Hora del día
- Condiciones específicas del entorno
tienen mayor impacto del esperado

💡 Se detectaron diferencias entre el análisis exploratorio (Power BI) y el modelo, lo que sugiere:

- Relaciones no lineales
- Interacciones complejas entre variables

## 📊 Visualización
Se desarrolló un dashboard en Power BI que permite:

- Analizar la distribución de accidentes
- Explorar variables clave
- Detectar patrones visuales
- Apoyar la toma de decisiones
## 🏗️ Arquitectura del proyecto
- Extracción de datos
- Limpieza y preprocesamiento
- Visualización (Power BI)
- Feature Engineering
- Modelado
- Evaluación
  
## 🚀 Posibles mejoras
- Incorporar más años de datos
- Añadir variables geoespaciales más precisas
- Modelos más avanzados (XGBoost, LightGBM)
- Integración en tiempo real con APIs
- Despliegue del modelo como servicio

## 👩‍💻 Autor
Proyecto desarrollado por Rebeca
