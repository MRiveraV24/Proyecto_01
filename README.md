# Detección de Neumonía Pediátrica mediante Inteligencia Artificial

## Introducción

Este proyecto desarrolla un sistema de Inteligencia Artificial (IA) para la detección de neumonía en radiografías de tórax pediátricas. La neumonía es una de las principales causas de mortalidad infantil a nivel mundial, y el diagnóstico temprano es crucial para mejorar los resultados clínicos. Sin embargo, en regiones con recursos médicos limitados, la falta de médicos especializados puede dificultar este proceso. El objetivo de este proyecto es proporcionar una herramienta basada en técnicas de aprendizaje profundo para asistir a los profesionales de la salud en la detección temprana y precisa de neumonía, mejorando la velocidad y precisión del diagnóstico.

---

## Contexto

La neumonía es una infección respiratoria aguda que afecta los pulmones, causando una alta tasa de mortalidad infantil, particularmente en países en desarrollo donde los recursos médicos son limitados. Tradicionalmente, el diagnóstico depende del análisis de radiografías por médicos capacitados, lo cual no siempre es accesible. 

Las redes neuronales convolucionales (CNN) han demostrado un alto desempeño en la clasificación de imágenes médicas, igualando o incluso superando la precisión de los médicos en ciertos escenarios. Estas herramientas no buscan reemplazar a los especialistas, sino actuar como un apoyo en la toma de decisiones clínicas.

---

## Objetivo

Desarrollar un modelo de reconocimiento de imágenes utilizando redes neuronales convolucionales (CNN) para detectar neumonía en radiografías de tórax pediátricas. Este sistema busca:
- Ayudar a los médicos en la detección rápida y precisa de la enfermedad.
- Mejorar el acceso a diagnósticos en áreas con recursos limitados.
  
---

## Conjunto de Datos

El proyecto utiliza un conjunto de datos público que incluye 5,863 radiografías de tórax pediátricas en formato JPEG, extraídas del Centro Médico de Mujeres y Niños de Guangzhou. Los pacientes tienen edades comprendidas entre uno y cinco años.

### Estructura del Conjunto de Datos:
- **Entrenamiento (5,216 imágenes):** Utilizadas para entrenar los modelos.
- **Validación (16 imágenes):** Empleadas para verificar el rendimiento durante el entrenamiento.
- **Prueba (624 imágenes):** Evaluación final del modelo.

### Etiquetas:
- **Normal (sin neumonía):** 1,341 imágenes.
- **Neumonía (con neumonía):** 3,875 imágenes.

### Características:
- Los conjuntos de datos de entrenamiento presentan un desbalance significativo entre clases.
- Todas las imágenes fueron revisadas por médicos expertos para garantizar la calidad y precisión de los diagnósticos.
- Fuente de datos: [Kaggle Dataset](https://www.kaggle.com/datasets/paultimothymooney/chest-xray-pneumonia).

---

## Metodología

El desarrollo del modelo incluyó los siguientes pasos:

1. **Exploración de Modelos:** Se probaron tres arquitecturas de CNN: `model1`, `model2` y `model3`.
2. **Aprendizaje por Transferencia:** Aprovechando datos de dominios similares para mejorar la precisión en un conjunto de datos limitado.
3. **Preprocesamiento de Datos:** 
   - Aumento de datos y normalización con `ImageDataGenerator`.
4. **Optimización de Hiperparámetros:** Uso de `Keras Tuner` para encontrar configuraciones óptimas.
5. **Modelo Ensamblado:** Combinación de los tres modelos entrenados para mejorar la precisión.
6. **Evaluación:** Análisis del rendimiento mediante métricas, matrices de confusión y gráficos de pérdida/precisión.

### Tecnologías y Librerías:
- **Deep Learning:** TensorFlow, Keras.
- **Manipulación de Datos:** NumPy, Pandas.
- **Visualización de Datos:** Matplotlib, Seaborn.
- **Evaluación:** Scikit-learn.
- **Optimización:** Keras Tuner.

---

## Resultados

- Los modelos individuales lograron una precisión promedio del **60%**.
- El modelo ensamblado mejoró el rendimiento general, alcanzando un **74% de exactitud**.
- Desafíos identificados:
  - Dificultades para identificar instancias de la clase "Normal" debido al desbalance de clases.
  - Alta tasa de falsos positivos, como se observó en las matrices de confusión.
- Los gráficos de pérdida y precisión mostraron un comportamiento consistente durante el entrenamiento, destacando el potencial de la metodología.

---

## Conclusiones

1. **Viabilidad:** Este proyecto demostró que los modelos de aprendizaje profundo son efectivos para clasificar radiografías pediátricas y detectar neumonía.
2. **Desempeño:** El modelo ensamblado mostró una mejora significativa en comparación con modelos individuales.
3. **Áreas de Mejora:**
   - Reequilibrar el conjunto de datos.
   - Explorar arquitecturas más avanzadas.
   - Ajustar hiperparámetros para mejorar el rendimiento.
4. **Aplicación:** Estas herramientas pueden apoyar el diagnóstico temprano de neumonía, especialmente en regiones con acceso limitado a recursos médicos.

*Nota:* La IA es una herramienta complementaria y no reemplaza el juicio clínico de los profesionales de la salud.

---

## Herramientas Utilizadas

- **Lenguaje de Programación:** Python.
- **Deep Learning:** TensorFlow, Keras.
- **Manipulación de Datos:** NumPy, Pandas.
- **Visualización:** Matplotlib, Seaborn.
- **Evaluación y Métricas:** Scikit-learn.
- **Optimización:** Keras Tuner.
