# Implementation Cross Validation in K Nearest Neighbors KNN

Este documento presenta un análisis exhaustivo de la implementación de cross-validation en el algoritmo K-Nearest Neighbors (KNN) utilizando el dataset Iris. Nuestro objetivo principal fue demostrar las ventajas de la validación cruzada frente al método tradicional de train/test split, identificar el número óptimo de vecinos (k) y evaluar la estabilidad del modelo.
Hallazgos principales:
Cross-validation identifica k=6 como valor óptimo con un accuracy de 97.33%
La desviación estándar baja (±0.0143) confirma la estabilidad del modelo
Cross-validation proporciona evaluaciones más robustas que train/test split
El modelo final alcanza 91.11% de accuracy en el conjunto de prueba

En el campo del machine learning, la evaluación correcta de modelos es fundamental para garantizar su capacidad de generalización. El método tradicional de train/test split, aunque ampliamente utilizado, presenta limitaciones importantes: depende de una única división aleatoria de datos y puede generar estimaciones sesgadas del rendimiento real del modelo.
Este estudio implementa cross-validation (validación cruzada) como alternativa más robusta, evaluando su efectividad en la clasificación de especies del dataset Iris utilizando el algoritmo K-Nearest Neighbors (KNN).

Preguntas de investigación:
¿Cuál es el valor óptimo de k para el clasificador KNN en el dataset Iris?
¿Qué ventajas ofrece cross-validation sobre el train/test split tradicional?
¿Qué tan estable es el rendimiento del modelo seleccionado?
