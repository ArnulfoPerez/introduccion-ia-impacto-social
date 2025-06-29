# 🧠 Resumen Ejecutivo – Sesión 2
Historia y taxonomía de la IA: de la cibernética a la explosión algorítmica

## 🎯 Objetivo de la sesión
Comprender el desarrollo histórico y filosófico de la inteligencia artificial (IA), identificar sus principales categorías funcionales y algorítmicas, y reconocer los hitos culturales, técnicos e institucionales que marcaron su evolución.

## 🕰️ I. Trayectoria histórica de la IA
Pioneros y contexto fundacional (décadas 1940–1950)
Alan Turing propuso la idea de una máquina que piense, introduciendo la prueba de Turing (1950).

Norbert Wiener, junto con Arturo Rosenblueth, desarrolló la cibernética: estudio de sistemas que se autorregulan mediante retroalimentación.

El surgimiento de la IA estuvo vinculado a avances técnicos de posguerra, optimismo científico y la metáfora computacional de la mente.

Conferencia de Dartmouth (1956)
Marca el inicio formal del campo de la IA.

Principales figuras: John McCarthy, Marvin Minsky, Claude Shannon, Herbert Simon, Allen Newell.

Expectativas: lograr razonamiento automático, comprensión del lenguaje, planificación, e incluso conciencia artificial en pocas décadas.

## ❄️ II. IA simbólica y sus límites
Predominó por décadas: reglas lógicas, motores de inferencia, representaciones simbólicas.

Minsky y Papert (1969) demostraron las limitaciones de los perceptrones (modelo neuronal simple), frenando el entusiasmo por las redes neuronales.

Primer invierno de la IA (años 70–80): desilusión ante el estancamiento técnico.

## 📸 III. Auge del aprendizaje profundo (Deep Learning)
Visión artificial y el desafío de ImageNet
ILSVRC (2010–2017): competencia impulsada por Stanford y Princeton para mejorar el reconocimiento visual.

En 2012, AlexNet (Hinton, Krizhevsky, Sutskever) introduce redes profundas con GPU → salto cualitativo en precisión.

### Anécdotas clave
“Los gatitos de Ng”: red neuronal sin supervisión identifica rostros y gatos sin ser entrenada explícitamente.

Google Translate mejora cuando se prescinde de expertos lingüistas y se entrenan modelos con grandes corpus.

Sam Altman (OpenAI): pasó de escéptico a promotor clave tras el éxito inesperado de modelos de lenguaje.

## ♟️ IV. Reinforcement Learning y dominio de juegos
IBM Deep Blue (1997) derrota a Kasparov con fuerza bruta + heurística.

AlphaGo (DeepMind, 2016) vence a campeones de Go combinando redes profundas y reinforcement learning.

Abre camino a la IA como herramienta de toma de decisiones adaptativas.

## 🧭 V. Taxonomía de la IA
### A. Según alcance o capacidad
| Tipo de IA             | Descripción                                                                 |
|------------------------|------------------------------------------------------------------------------|
| **Estrecha (narrow)**  | Tareas específicas (ej. traducción automática, recomendación de productos).  |
| **General (AGI)**      | Capacidad cognitiva similar a la de un ser humano (aún hipotética).          |
| **Superinteligente**   | IA hipotética que supera a los humanos en todas las áreas del conocimiento. |

### B. Según enfoque técnico
| Enfoque                   | Características                                                   |
|---------------------------|--------------------------------------------------------------------|
| **Simbólico (GOFAI)**     | Reglas explícitas y lógica formal; alta interpretabilidad.         |
| **Aprendizaje automático (ML)** | Modelado estadístico basado en datos; requiere entrenamiento supervisado o no supervisado. |
| **Aprendizaje profundo (DL)**   | Redes neuronales con muchas capas; detecta representaciones jerárquicas complejas.           |
| **Aprendizaje por refuerzo**    | Agentes que aprenden mediante prueba y error optimizando recompensas en un entorno.         |
| **Neuro-simbólico**             | Combina estructuras simbólicas con redes neuronales; busca razonamiento interpretable con flexibilidad adaptativa. |

> 📌 Deep Learning es un subcampo dentro del ML, que a su vez es una rama dentro de la IA.

# 🧭 Taxonomía técnica ampliada de la Inteligencia Artificial

Esta tabla resume cómo se ubican algunos enfoques y técnicas contemporáneas dentro de la arquitectura general de la IA.

---

## 📚 Clasificación general

| Enfoque técnico               | Subcategorías / Ejemplos clave                                            |
|-------------------------------|----------------------------------------------------------------------------|
| **IA simbólica (GOFAI)**      | Sistemas expertos, lógica formal, planificación automática                |
| **Aprendizaje automático (ML)** | Supervisado / No supervisado / Semi-supervisado                         |
| → **Aprendizaje profundo (DL)** | CNNs (visión), RNNs (texto), Transformers                               |
|    → **LLMs (Large Language Models)** | GPT, BERT, LLaMA, PaLM (basados en Transformers)               |
| **Aprendizaje por refuerzo (RL)** | Q-learning, SARSA, políticas adaptativas                               |
| → **Deep RL**                 | AlphaGo, AlphaZero, Codex, robótica autónoma                             |
| **Neuro-simbólico**           | Redes neuronales + reglas estructuradas; razonamiento interpretativo      |

---

## 🔍 Ubicación específica

- **LLMs (Large Language Models)**  
  - Subtipo de **Aprendizaje profundo (DL)**  
  - Usan arquitectura **Transformer**  
  - Entrenamiento auto-supervisado con grandes corpus de texto  
  - Ejemplos: GPT, Claude, BERT, LLaMA, Gemini

- **Reinforcement Learning (RL)**  
  - Enfoque distinto al aprendizaje supervisado  
  - El agente aprende por ensayo y error en un entorno dinámico  
  - Usado en juegos, navegación, robótica, optimización de procesos  
  - **Deep RL** combina RL con redes neuronales profundas para tareas complejas

---

## 🤖 Analogía conceptual

- **LLMs**: “Aprenden leyendo libros, textos y conversaciones” → uso masivo de texto digital
- **RL**: “Aprende actuando y cometiendo errores” → agente adaptativo que explora su entorno

---

# ⚙️ ¿Qué es la arquitectura Transformer?

La arquitectura **Transformer** es un tipo de modelo de red neuronal profunda diseñado para procesar secuencias de datos (como texto, audio o código) de forma eficiente y paralela. Se ha convertido en la **base técnica dominante** para modelos de lenguaje natural como GPT, BERT, T5, LLaMA y Gemini, así como para aplicaciones en visión, traducción automática, música, proteínas y más.

---

## 📜 Origen: ¿Quién la propuso y por qué?

- Fue introducida en 2017 por investigadores de Google Brain en el artículo seminal titulado  
  **"Attention is All You Need"** (*Vaswani et al., 2017*).
- Su motivación fue reemplazar arquitecturas anteriores —como las redes recurrentes (RNN) y LSTM— que eran lentas y difíciles de paralelizar.

> ✅ La clave de los Transformers es su mecanismo de **self-attention**, que permite al modelo enfocarse dinámicamente en distintas partes de una secuencia al mismo tiempo.

---

## 🧠 ¿Por qué era necesaria esta arquitectura?

### Limitaciones de arquitecturas previas (RNN, LSTM):

- Procesaban las secuencias de forma **lineal paso a paso**, lo que dificultaba el paralelismo y la escalabilidad.
- Dificultades para **aprender relaciones a largo plazo** en secuencias largas (problema del gradiente).
- Alto costo de entrenamiento en tareas multilingües o multisentencia.

### Ventajas del Transformer:

- **Paralelización completa:** permite procesar todos los tokens a la vez.
- **Self-attention:** capta relaciones de dependencia entre palabras **sin importar la distancia** en la secuencia.
- Escalable: permite modelos de **miles de millones de parámetros** con entrenamiento distribuido.
- Modular: sirve para tareas muy diversas (clasificación, generación, resumen, traducción).

---

## 🎯 Aplicaciones objetivo

- **Procesamiento de lenguaje natural (NLP):** traducción automática, chatbots, análisis de sentimientos, generación de texto, respuesta a preguntas.
- **Visión por computadora:** clasificación de imágenes, generación visual (ViT, DALL·E).
- **Código y matemáticas:** modelos como Codex o AlphaCode generan código fuente desde lenguaje natural.
- **Audio y música:** modelos como Whisper procesan audio y reconocen voz multilingüe.
- **Ciencias biológicas:** AlphaFold usa arquitecturas derivadas para predecir estructuras de proteínas.

---

## 🧬 ¿Cómo funciona un Transformer? (vista simplificada)

1. Convierte una secuencia de entrada (palabras, píxeles, etc.) en una representación vectorial (*embedding*).
2. Usa capas de **self-attention**, donde cada parte de la secuencia se compara con las demás para determinar su relevancia relativa.
3. Aplica capas de normalización, proyección y funciones no lineales.
4. Genera una representación procesada (codificada o decodificada) para realizar la tarea deseada.

---

## 🏗️ Otras arquitecturas alternativas (pasadas o emergentes)

| Arquitectura         | Descripción breve | Limitaciones / comparación |
|----------------------|-------------------|-----------------------------|
| **RNN (Recurrent Neural Network)** | Procesa secuencias paso a paso | No paralelizable; memoria corta |
| **LSTM (Long Short-Term Memory)** | Variante mejorada de RNN | Mejor memoria, pero entrenamiento lento |
| **GRU (Gated Recurrent Unit)** | Simplificación del LSTM | Similar rendimiento con menos parámetros |
| **CNN (Convolutional Neural Network)** | Muy usada en visión y texto corto | Menor capacidad de representación jerárquica |
| **Perceptrón multicapa (MLP)** | Base histórica de las redes neuronales | No capta estructura secuencial |
| **Retentive Network / Mamba (2023–2024)** | Nuevas arquitecturas sin atención | Buscan eficiencia a gran escala |

---

## 🧠 Reflexión final

La arquitectura Transformer representa un **cambio de paradigma**: no solo mejoró el rendimiento, sino que también desbloqueó una nueva era de modelos de lenguaje y multimodales. Gracias a su flexibilidad y escalabilidad, se ha vuelto la columna vertebral de los sistemas de IA más avanzados de la actualidad.

> **"Attention" ya no es solo una técnica: es la clave de una nueva forma de aprendizaje distribuido.**

---



## 🚀 VI. Estado actual y perspectivas
Predominio de modelos grandes de lenguaje (LLMs): razonamiento, codificación, traducción.

Desarrollo de IA multimodal (texto, imagen, voz).

Desafíos en ética, transparencia, alineamiento y regulación.

Aún no se alcanza una IA general, pero las aplicaciones son cada vez más amplias e impactantes.

## 📎 Recursos sugeridos
Documental: AlphaGo: The Movie (DeepMind, 2017)

Video introductorio (EDteam): ¿Qué es y cómo funciona la IA?
