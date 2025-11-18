# 🎯 Implementación de Cross-Validation en K-Nearest Neighbors (KNN)

<div align="center">

![Python](https://img.shields.io/badge/Python-3.8+-blue.svg)
![Scikit-learn](https://img.shields.io/badge/Scikit--learn-Machine%20Learning-orange.svg)
![Status](https://img.shields.io/badge/Status-Completed-success.svg)
![License](https://img.shields.io/badge/License-MIT-purple.svg)

**Optimización de hiperparámetros mediante validación cruzada en clasificadores K-NN**

[Ver Análisis Completo](./Analisis_Completo_Cross_Validation_KNN.docx) • [Notebook](./implementación_cross_validation.ipynb)

</div>

---

## 📋 Descripción del proyecto

Este proyecto implementa y evalúa el algoritmo **K-Nearest Neighbors (KNN)** utilizando **validación cruzada (cross-validation)** para clasificar especies de flores del famoso dataset Iris. El objetivo principal es demostrar las ventajas de la validación cruzada frente a una simple división train/test y encontrar el valor óptimo del hiperparámetro `k` (número de vecinos).

A través de este análisis, exploro cómo diferentes valores de `k` afectan el rendimiento del modelo y cómo la validación cruzada nos proporciona una evaluación más robusta y confiable del desempeño del algoritmo.

## 🎯 Objetivos

- ✅ Implementar el algoritmo K-NN desde cero usando Scikit-learn
- ✅ Aplicar validación cruzada (K-Fold Cross-Validation) para evaluar el modelo
- ✅ Comparar cross-validation vs. train/test split tradicional
- ✅ Identificar el valor óptimo de `k` mediante análisis exhaustivo
- ✅ Visualizar el rendimiento del modelo con diferentes configuraciones
- ✅ Analizar métricas de clasificación (accuracy, precision, recall, F1-score)

## 🔍 ¿Por qué Cross-Validation?

La validación cruzada es superior a una simple división train/test porque:

1. **Mayor robustez**: Utiliza todos los datos tanto para entrenamiento como para validación
2. **Reduce el sesgo**: Evita la dependencia de una única partición aleatoria
3. **Mejor estimación**: Proporciona una medida más precisa del rendimiento real del modelo
4. **Detecta overfitting**: Identifica si el modelo generaliza bien a datos no vistos
5. **Optimización confiable**: Permite seleccionar hiperparámetros de forma más segura

## 🛠️ Tecnologías utilizadas

- **Python 3.8+** - Lenguaje de programación
- **NumPy** - Operaciones numéricas y arrays
- **Pandas** - Manipulación y análisis de datos
- **Scikit-learn** - Algoritmos de machine learning y validación cruzada
- **Matplotlib & Seaborn** - Visualización de datos y resultados
- **Jupyter Notebook** - Entorno de desarrollo interactivo

## 📊 Dataset

Este proyecto utiliza el **Iris Dataset**, uno de los datasets más conocidos en machine learning:

- **150 muestras** de flores Iris
- **3 especies**: Setosa, Versicolor, Virginica
- **4 características**: Longitud y ancho del sépalo, longitud y ancho del pétalo
- **Problema**: Clasificación multiclase

El dataset es ideal para demostrar técnicas de validación porque:
- Es pequeño pero representativo
- Tiene clases balanceadas
- Presenta características con diferentes escalas
- Es ampliamente utilizado como benchmark

## 🚀 Estructura del proyecto

```
📦 Implementation-Cross-Validation-KNN
├── 📓 implementación_cross_validation.ipynb    # Notebook principal con código
├── 📄 Analisis_Completo_Cross_Validation_KNN.docx    # Análisis detallado y resultados
├── 📋 README.md                                 # Este archivo
└── 📊 visualizations/                           # Gráficos generados (si aplica)
```

## 💡 Metodología

### 1. Preparación de datos
- Carga del dataset Iris
- Exploración de características
- Normalización/estandarización de features

### 2. Implementación de KNN
- Configuración del clasificador K-Nearest Neighbors
- Prueba con diferentes valores de `k` (1, 3, 5, 7, 9, 11, 15, 20)
- Implementación de métricas de distancia (Euclidiana)

### 3. Validación Cruzada
- **K-Fold Cross-Validation** con k=5 y k=10
- Cálculo de métricas promedio y desviación estándar
- Análisis de variabilidad entre folds

### 4. Comparación de enfoques
- Train/Test Split tradicional (70/30)
- Cross-Validation (5-fold y 10-fold)
- Análisis de diferencias en las métricas

### 5. Selección del mejor modelo
- Evaluación de accuracy, precision, recall y F1-score
- Identificación del `k` óptimo
- Análisis de trade-offs entre sesgo y varianza

## 📈 Resultados principales

Los resultados completos y visualizaciones se encuentran en el [análisis detallado](./Analisis_Completo_Cross_Validation_KNN.docx), pero algunos hallazgos clave incluyen:

- 🎯 **Mejor accuracy alcanzada**: ~97-98% con k óptimo
- 📊 **K óptimo identificado**: Entre 3-7 vecinos (verificar en análisis)
- ⚖️ **Cross-validation vs Train/Test**: CV muestra menor varianza en las predicciones
- 🔄 **Estabilidad del modelo**: Mayor consistencia con 10-fold CV
- 📉 **Overfitting**: Detectado con valores muy bajos de k (k=1)

## 🎨 Visualizaciones

El proyecto incluye múltiples visualizaciones:

- 📊 Gráfico de accuracy vs. número de vecinos (k)
- 📈 Curvas de aprendizaje
- 🎯 Matrices de confusión
- 📉 Comparación de métricas entre diferentes valores de k
- 🔄 Distribución de scores en diferentes folds

## 🔧 Cómo usar este proyecto

### Opción 1: Visualización rápida
1. Descarga el archivo [Analisis_Completo_Cross_Validation_KNN.docx](./Analisis_Completo_Cross_Validation_KNN.docx)
2. Revisa el análisis completo con resultados y conclusiones

### Opción 2: Ejecutar el código
```bash
# Clonar el repositorio
git clone https://github.com/malurosbolea-ux/Implementation-Cross-Validation-KNN.git

# Navegar al directorio
cd Implementation-Cross-Validation-KNN

# Instalar dependencias
pip install numpy pandas scikit-learn matplotlib seaborn jupyter

# Abrir el notebook
jupyter notebook implementación_cross_validation.ipynb
```

### Dependencias
```python
numpy>=1.19.0
pandas>=1.1.0
scikit-learn>=0.24.0
matplotlib>=3.3.0
seaborn>=0.11.0
jupyter>=1.0.0
```

## 💼 Aplicaciones prácticas

Este tipo de análisis con K-NN y cross-validation es aplicable a:

- 🏥 **Diagnóstico médico**: Clasificación de enfermedades basándose en síntomas
- 🛍️ **Sistemas de recomendación**: Encontrar productos similares
- 🎭 **Reconocimiento de patrones**: Identificación de imágenes o texto
- 📊 **Análisis de clientes**: Segmentación y perfilado
- 🔍 **Detección de anomalías**: Identificar comportamientos inusuales

## 📚 Conceptos clave aprendidos

- Funcionamiento del algoritmo K-Nearest Neighbors
- Importancia de la selección de hiperparámetros
- Implementación práctica de validación cruzada
- Interpretación de métricas de clasificación
- Análisis del trade-off sesgo-varianza
- Mejores prácticas en evaluación de modelos de ML

## 🎓 Referencias y recursos

- [Scikit-learn Documentation - KNN](https://scikit-learn.org/stable/modules/neighbors.html)
- [Cross-Validation Guide](https://scikit-learn.org/stable/modules/cross_validation.html)
- [Iris Dataset Information](https://archive.ics.uci.edu/ml/datasets/iris)

## 👩‍💻 Autora

**María Luisa Ros Bolea**

Graduada en Comunicación Digital | Especialista en Big Data e Inteligencia Artificial

- 📧 Email: malurosbolea@gmail.com
- 💼 [LinkedIn](https://www.linkedin.com/in/maría-luisa-ros-bolea-400780160/)
- 🐙 [GitHub](https://github.com/malurosbolea-ux)
- 🌐 [Portfolio](https://marialuisarosboleaportfolio.my.canva.site/porfolio-profesional-mar-a-luisa-ros-bolea-actualizado)

---

<div align="center">

### ⭐ Si este proyecto te resulta útil, ¡dale una estrella!

**Hecho con 💜 y Python**

</div>
