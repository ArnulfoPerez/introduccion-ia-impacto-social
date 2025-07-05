# Taxonomía de la Inteligencia Artificial en 2025: Casos de Uso y Ciclo de Vida

## Introducción: ¿Qué es la IA hoy?
La inteligencia artificial (IA) en 2025 es un ecosistema de técnicas que permiten a las máquinas **aprender de datos** y **automatizar decisiones**. Su núcleo común es el **aprendizaje automático (ML)**, un proceso de optimización donde algoritmos ajustan parámetros para minimizar errores (ej: predecir el precio de una casa o clasificar imágenes). 

### Fundamentos Conceptuales Clave
1. **Datos como geometría**: Los datos viven en un *espacio de características* (feature space). Por ejemplo, en un sistema de recomendación de películas, cada usuario y película es un punto en un espacio multidimensional.
2. **Learning = Optimización**: Aprender es encontrar parámetros (ej: pesos en una red neuronal) que minimicen una *función de pérdida* (error entre predicciones y valores reales).
3. **Estadística subyacente**: Media, varianza, y distribuciones probabilísticas describen patrones en los datos. La regresión (predecir valores continuos) y clasificación (etiquetar categorías) son las tareas básicas.

---

## Taxonomía de la IA y sus Modalidades
### 1. **Machine Learning (ML) Tradicional**
- **Qué hace**: Modelos estadísticos para patrones "simples" (ej: árboles de decisión, SVM).
- **Casos de uso**:
  - *Regresión logística*: Riesgo crediticio en bancos.
  - *Random Forest*: Detección de fraude en transacciones.
- **Implementación**: Requiere *feature engineering manual* (seleccionar variables relevantes).

### 2. **Deep Learning (DL)**
- **Qué hace**: Redes neuronales que automatizan el *feature engineering* (ej: CNN para imágenes, RNN para texto).
- **Casos de uso**:
  - *Computer Vision*: Autos autónomos (detección de peatones).
  - *Procesamiento de lenguaje natural (NLP)*: Traducción automática.
- **Ventaja**: Escala con grandes volúmenes de datos.

### 3. **Large Language Models (LLMs)**
- **Qué hace**: Redes neuronales (transformers) entrenadas en texto masivo (ej: GPT-5, Gemini).
- **Casos de uso**:
  - *Asistentes virtuales*: Soporte al cliente automatizado.
  - *Generación de contenido*: Resúmenes de documentos legales.
- **Desafío**: Requieren fine-tuning para dominios específicos.

### 4. **Reinforcement Learning (RL)**
- **Qué hace**: Agentes que aprenden por prueba/error con recompensas (ej: AlphaFold para plegamiento de proteínas).
- **Casos de uso**:
  - *Robótica*: Optimización de movimientos en almacenes logísticos.
  - *Videojuegos*: NPCs con comportamientos adaptativos.

---

## Ciclo de Vida de un Proyecto de IA
1. **Captura de datos**: 
   - Sensores, APIs, o bases de datos. 
   - *Ejemplo*: Imágenes de cámaras para un sistema de reconocimiento facial.
2. **Limpieza y preprocesamiento**:
   - Eliminar outliers, normalizar valores (ej: escalar ingresos entre 0 y 1).
3. **Entrenamiento**:
   - División en datos de entrenamiento/validación. Uso de GPUs/TPUs para DL.
4. **Despliegue (Deployment)**:
   - APIs (FastAPI), edge computing (ej: modelos en teléfonos móviles).
5. **Evaluación y monitoreo**:
   - Métricas: *Accuracy*, *F1-score* (clasificación), *MAE* (regresión).
   - *Drift de datos*: Reentrenar modelos si la distribución de datos cambia.

---

## ¿Cómo se Relacionan Estas Modalidades?
- **LLMs usan DL** (transformers son redes neuronales profundas).
- **RL puede combinar DL** (Deep Q-Learning para juegos).
- **ML tradicional sigue siendo útil** cuando los datos son pequeños o interpretables.

---

## Conclusión: IA como Herramienta Versátil
En 2025, la IA no es "una sola cosa", sino un conjunto de herramientas seleccionables según:
- **Volumen de datos** (DL para grandes datasets).
- **Interpretabilidad** (ML tradicional para regulaciones estrictas).
- **Tipo de problema** (RL para sistemas interactivos).

> "El futuro no es IA vs humanos, sino humanos usando IA para amplificar su potencial." — Adaptado de Andrew Ng.

## Referencias recomendadas

- [An Observation on Generalization](https://www.youtube.com/live/AKMuA_TVz3A?si=Z5OMDxkLhmlIRO1R)
- [AlphaGo - The Movie | Full award-winning documentary](https://youtu.be/WXuK6gekU1Y?si=zc2FPQadoreKA7uP)
- [Debates actuales sobre la naturaleza de la conciencia](https://youtu.be/2cvkyU0YTIU?si=C9KZkuvEdEFcrvfE)
- [La teoría de la información integrada de Giulio Tononi](https://youtu.be/zovH3vkxneU?si=kwwhCLvNKeNTGI9C)
- [LA TEORÍA DE LA INFORMACIÓN INTEGRADA Φ - ¿Se puede estudiar la consciencia matemáticamente?](https://youtu.be/g9kKcpgU-qo?si=YUPEi-B25kjtCDKt)
