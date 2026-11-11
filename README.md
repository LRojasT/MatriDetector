# 🚗 MatriDetector - Sistema Inteligente ALPR

Este repositorio contiene la implementación de un sistema inteligente diseñado para localizar y reconocer matrículas de vehículos a partir de imágenes estáticas, desarrollado como proyecto académico en la Universidad Politécnica de Madrid (UPM).

El proyecto aborda el desafío de la detección en entornos no controlados (variaciones de iluminación, ángulo y ruido) y la implementación de un **Reconocimiento Óptico de Caracteres (OCR) desarrollado desde cero sin recurrir a librerías externas (cajas negras)**.

## 🛠️ Arquitectura y Tecnologías
La solución propuesta se basa en un enfoque híbrido clásico (Visión Artificial tradicional + Machine Learning supervisado).

### 1. Módulo de Visión Artificial (Localización y Segmentación)
* **Preprocesamiento:** Conversión a escala de grises y aplicación de filtro Gaussiano.
* **Detección de bordes:** Algoritmo de Canny.
* **Análisis de contornos:** Detección de regiones con forma de matrícula.
* **Segmentación:** Extracción de caracteres mediante umbralización.

### 2. Módulo de Aprendizaje Automático (OCR Propio)
* **Extracción de características:** HOG o imágenes normalizadas.
* **Clasificación:** Implementación de modelos KNN y SVM para clasificar entre 36 clases posibles (dígitos 0-9 y letras A-Z).
* **Dataset generado:** Entrenamiento realizado con imágenes de 20x20 píxeles, combinando recortes de matrículas reales y caracteres generados sintéticamente para balancear las clases (80% train / 20% test).

## 📂 Contenido del Repositorio
* `Matridetector.ipynb`: Código fuente completo del proyecto con la implementación de los algoritmos y entrenamiento de los modelos.
* `Memoria_MatriDetector.pdf`: Documento detallado con la justificación del diseño, análisis del estado del arte, descripción de la arquitectura secuencial y evaluación de resultados.

---
*Proyecto desarrollado por Lucas Rojas Tena y Jorge Sánchez Campelo.*
