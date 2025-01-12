# Diagnóstico Temprano de Neumonía Infantil: Una Perspectiva Innovadora desde la Inteligencia Artificial

## Introducción
Este proyecto utiliza inteligencia artificial para abordar uno de los mayores retos en la salud infantil: la detección temprana de neumonía. Mediante redes neuronales convolucionales (CNN), se busca mejorar la precisión y la eficiencia en el diagnóstico de esta enfermedad, contribuyendo así a una atención médica más eficaz y accesible.

## Contexto
La neumonía es una de las principales causas de mortalidad infantil a nivel mundial, especialmente en niños menores de 5 años. El diagnóstico temprano es crucial para mejorar las tasas de supervivencia, pero los recursos limitados y los errores humanos pueden retrasar el tratamiento.

## Objetivo General
Desarrollar un modelo de inteligencia artificial basado en redes neuronales convolucionales para detectar neumonía en radiografías de tórax, incrementando la precisión y reduciendo el tiempo requerido para el diagnóstico.

## Objetivos Específicos
1. Implementar un modelo para identificar neumonía en niños menores de 5 años utilizando CNN.
2. Evaluar la precisión del modelo mediante conjuntos de datos clasificados como "Normal" y "Neumonía".
3. Optimizar el modelo para lograr un equilibrio entre precisión y eficiencia computacional.

## Conjunto de Datos
Se utilizaron radiografías de tórax clasificadas en dos categorías: “Normal” y “Neumonía”. Estas fueron divididas en conjuntos de entrenamiento, prueba y validación, asegurando una distribución equilibrada entre las clases.

## Metodología
1. **Preprocesamiento de Imágenes**: Ajuste de dimensiones, normalización y mejora de calidad.
2. **Creación de Modelos**: Desarrollo de tres modelos individuales con diferentes configuraciones.
3. **Evaluación y Ensamblaje**: Combinación de los modelos individuales para crear un modelo ensamblado con mejores resultados.
4. **Validación**: Uso de métricas de rendimiento como la precisión y la matriz de confusión para evaluar el modelo.

## Resultados
- **Modelo Ensamblado**: Alcanzó una precisión del 74%, superando a los modelos individuales.
- **Matriz de Confusión**: Clasificación correcta de 72 casos normales y 388 con neumonía, con solo 2 falsos negativos y 162 falsos positivos.
- **Curvas de Aprendizaje**: Se observó una mejora consistente en la pérdida y la precisión a lo largo de las épocas de entrenamiento.

## Ajustes del Modelo
El modelo ensamblado fue ajustado iterativamente para optimizar el equilibrio entre precisión y generalización, utilizando técnicas como regularización y ajuste de hiperparámetros.

## Conclusiones
- **Beneficios**: Mejora en la precisión del diagnóstico, reducción del tiempo de análisis, accesibilidad incrementada y apoyo a la toma de decisiones.
- **Limitaciones**: Falta de datos, interpretabilidad del modelo, sesgo algorítmico y eficiencia computacional.
- **Impacto Futuro**: Este proyecto no reemplazará a los profesionales de radiología, sino que complementará su trabajo, mejorando los diagnósticos y la atención a pacientes.

## Visualizaciones
Se incluyen:
- **Curvas de Aprendizaje**: Pérdida y precisión durante el entrenamiento.
- **Matriz de Confusión**: Visualización de clasificaciones correctas e incorrectas.
- **Distribución de Clases**: Proporción de casos normales y con neumonía en los datos.

## Herramientas y Tecnologías
- **Lenguajes de Programación**: Python
- **Bibliotecas**: TensorFlow, Keras, NumPy, Matplotlib
- **Plataforma de Desarrollo**: Jupyter Notebook
- **Técnicas**: Redes Neuronales Convolucionales (CNN), preprocesamiento de imágenes, validación cruzada

---
Este proyecto demuestra cómo la inteligencia artificial puede marcar una diferencia significativa en el diagnóstico temprano de enfermedades críticas como la neumonía infantil. Para explorar el código y los detalles del análisis, visita el repositorio.
