# Detección de Neumonía Pediátrica mediante Inteligencia Artificial

## Introducción

Este proyecto se enfoca en el desarrollo de un sistema de Inteligencia Artificial (IA) para la detección de neumonía en radiografías de tórax pediátricas. La neumonía es una de las principales causas de mortalidad infantil a nivel mundial. El diagnóstico temprano es crucial, pero requiere análisis de radiografías por médicos expertos, lo cual puede ser un problema en áreas con recursos médicos limitados. Este proyecto busca mejorar la precisión y velocidad del diagnóstico de neumonía mediante el uso de técnicas de aprendizaje profundo. El objetivo es proporcionar una herramienta complementaria para los profesionales de la salud en la toma de decisiones clínicas.

## Contexto

La neumonía es una infección respiratoria aguda que afecta los pulmones y es una de las principales causas de muerte infantil a nivel mundial. Más del 90% de los casos se diagnostican en países en desarrollo, donde los recursos médicos son limitados. El diagnóstico tradicional requiere análisis de radiografías por médicos capacitados, lo cual dificulta la detección temprana. Las redes neuronales convolucionales (CNN) han demostrado ser muy eficaces en la clasificación de imágenes médicas y pueden igualar o superar la precisión de un médico especialista en la detección de neumonía. Sin embargo, estas herramientas no reemplazan a los médicos, sino que actúan como un apoyo para el personal médico. Este proyecto utiliza datos de radiografías de tórax pediátricas para entrenar un sistema de IA que ayude en este proceso.

## Objetivo

El objetivo principal de este proyecto es desarrollar e implementar un modelo de reconocimiento de imágenes utilizando técnicas de aprendizaje profundo, específicamente redes neuronales convolucionales (CNN). El modelo tomará como entrada una radiografía de tórax pediátrica y predecirá si hay presencia de neumonía. Se busca que esta herramienta pueda ayudar a los médicos a hacer diagnósticos más rápidos y precisos, especialmente en lugares con recursos limitados.

## Conjunto de Datos

El conjunto de datos utilizado en este proyecto consiste en 5,863 imágenes de radiografías de tórax pediátricas en formato JPEG. Las imágenes fueron obtenidas del Centro Médico de Mujeres y Niños de Guangzhou, de pacientes entre uno y cinco años.

•	Las imágenes se dividen en tres conjuntos: 
o	Entrenamiento (5216 imágenes): utilizadas para entrenar los modelos de IA.
o	Validación (16 imágenes): empleadas para validar el rendimiento de los modelos durante el entrenamiento.
o	Prueba (624 imágenes): usadas para evaluar el rendimiento final del modelo.
•	Las imágenes están etiquetadas como "Normal" (sin neumonía) o "Neumonía" (con neumonía).
•	El conjunto de entrenamiento tiene un desbalance entre las clases (1341 normales y 3875 con neumonía), mientras que el conjunto de validación está balanceado (8 imágenes por clase).
•	Se realizó un control de calidad para asegurar que las imágenes fueran legibles y de alta calidad. Adicionalmente, los diagnósticos fueron revisados por dos médicos expertos y un tercer experto revisó el conjunto de datos de prueba para asegurar la precisión de los diagnósticos.
•	Los datos fueron descargados de: https://www.kaggle.com/datasets/paultimothymooney/chest-xray-pneumonia.

## Metodología

•	Se exploraron diferentes arquitecturas de redes neuronales convolucionales (CNN), denominadas model1, model2 y model3.
•	Se empleó la técnica de aprendizaje por transferencia para entrenar los modelos, aprovechando datos de dominios similares para abordar la escasez de datos.
•	Los datos fueron preprocesados usando ImageDataGenerator para aumentar la cantidad de datos y normalizar las imágenes.
•	Se empleó la librería Keras Tuner para buscar los hiperparámetros óptimos.
•	Se creó un modelo ensamblado combinando los tres modelos entrenados para mejorar la precisión.
•	Se evaluó el rendimiento de los modelos utilizando métricas de rendimiento, informes de clasificación y matrices de confusión.

Las librerías utilizadas incluyen:
•	TensorFlow y Keras para la construcción e implementación de los modelos de deep learning.
•	NumPy y Pandas para la manipulación de datos.
•	Matplotlib y Seaborn para la visualización de datos.
•	Scikit-learn para métricas y evaluación de modelos.

## Resultados

•	Se evaluó el rendimiento de cada modelo individualmente, y también el modelo ensamblado.
•	Los tres modelos individuales (model1, model2 y model3) lograron una exactitud (accuracy) de alrededor del 60%, con una precisión y recall variables según la clase.
•	El modelo ensamblado mejoró la exactitud general a 74%. Sin embargo, este modelo mostró un buen rendimiento en la clasificación de la clase 1 (neumonía), pero tuvo dificultades para identificar correctamente las instancias de la clase 0 (normal), lo cual sugiere un desbalance de clases en el entrenamiento.
•	Las matrices de confusión revelaron que los modelos tenían una cantidad significativa de falsos positivos.
•	Se generaron gráficos de pérdida y precisión durante el entrenamiento para cada modelo, permitiendo visualizar su comportamiento durante las diferentes épocas.
•	El modelo ensamblado mostró un buen desempeño en la identificación de casos positivos (neumonía), pero con una cantidad notable de falsos positivos.

## Conclusiones

•	El proyecto demostró la viabilidad de usar modelos de aprendizaje profundo para clasificar radiografías de tórax con el fin de detectar neumonía.
•	El modelo ensamblado mejoró la precisión en comparación con los modelos individuales.
•	Se identificaron áreas de mejora, como equilibrar el conjunto de datos, explorar nuevas arquitecturas de redes neuronales y ajustar los hiperparámetros para mejorar el rendimiento del modelo.
•	Se destaca el potencial de estos sistemas de IA para ayudar en el diagnóstico temprano de neumonía, especialmente en entornos con recursos limitados.
•	Se subraya la importancia de la IA como herramienta de apoyo para los médicos, pero no como un reemplazo para los profesionales de la salud.
•	La IA tiene un papel prometedor en la detección y el tratamiento de la neumonía infantil.

## Herramientas

•	Lenguaje de Programación: Python
•	Librerías de Deep Learning: TensorFlow y Keras
•	Librerías de Manipulación de Datos: NumPy y Pandas
•	Librerías de Visualización de Datos: Matplotlib y Seaborn
•	Librería de Métricas y Evaluación: Scikit-learn
•	Optimizador de Hiperparámetros: Keras Tuner
