# Fundamentos de los LLMs y la Arquitectura Transformer

## Introducción
Los **Modelos de Lenguaje de Gran Escala (LLMs)** como GPT-4 o Gemini han revolucionado el procesamiento de lenguaje natural (NLP). Este reporte explica:
1. **Qué es un LLM** y su arquitectura básica.
2. **El Transformer**: Motivo de su desarrollo y componentes clave.
3. **Mecanismo de atención** y su importancia.
4. Capacidades y limitaciones actuales.

---

## 1. ¿Qué es un LLM?
Un **Large Language Model (LLM)** es un modelo de inteligencia artificial entrenado para entender, generar y predecir texto.  
- **Entrada/Salida**: Procesa secuencias de texto (frases, documentos) y genera respuestas coherentes.  
- **Base estadística**: Aprende patrones de grandes corpus de texto (ejemplo: libros, artículos científicos).  

### Capacidades clave:
✅ Generación de texto humano.  
✅ Traducción automática.  
✅ Resumen de documentos.  

### Limitaciones:
❌ **Alucinaciones**: Inventa información no verificada.  
❌ **Sesgos**: Refleja prejuicios presentes en los datos de entrenamiento.  
❌ **Costo computacional**: Entrenar un LLM requiere miles de GPUs/TPUs.  

---

## 2. El Transformer: Arquitectura Revolucionaria
### ¿Por qué se desarrolló?
Antes del Transformer (2017), los modelos usaban **RNNs/LSTMs**, que tenían:
- **Problemas de largo alcance**: Dificultad para captar dependencias en textos largos.  
- **Ineficiencia**: Procesamiento secuencial (lento en entrenamiento).  

### Solución: Arquitectura Transformer
Propuesta por Vaswani et al. en *"Attention is All You Need"*, se basa en:  
1. **Auto-atención**: Analiza todas las palabras en paralelo (no secuencial).  
2. **Capas Feedforward**: Procesa información localmente.  
3. **Normalización y residuos**: Estabiliza el entrenamiento.  

#### Componentes principales:
- **Encoder**: Codifica la entrada (ejemplo: texto fuente en traducción).  
- **Decoder**: Genera la salida (ejemplo: texto traducido).  

---

## 3. Mecanismo de Atención (Attention)
### ¿Qué es?
Es un sistema que **pesa la importancia de cada palabra** en una secuencia respecto a otras.  

### ¿Por qué es crucial?
1. **Capta contexto global**: Ejemplo: En *"El banco financiero está junto al río"*, el modelo asigna más peso a *"financiero"* para definir *"banco"*.  
2. **Eficiencia**: Procesa texto en paralelo (vs. RNNs que lo hacen paso a paso).  

### Tipos de atención:
- **Auto-atención (Self-Attention)**: Relaciona palabras dentro de una misma secuencia.  
- **Atención cruzada (Cross-Attention)**: Usada en decodificadores para conectar con el encoder.  

---

## 4. Procesamiento de Texto en Transformers
### Flujo típico:
1. **Embedding**: Convierte palabras en vectores numéricos.  
2. **Capas de atención**: Calcula relaciones entre palabras.  
3. **Feedforward**: Refina representaciones.  
4. **Generación**: Predice la siguiente palabra (token).  

### Ejemplo práctico:
Para traducir *"Hello world"* al español:  
1. El encoder analiza *"Hello"* y *"world"* con atención.  
2. El decoder genera *"Hola"* y luego *"mundo"*, usando el contexto del encoder.  

---

## 5. Capacidades y Limitaciones en la Práctica
### Aplicaciones empresariales:
- **Chatbots**: Atención al cliente 24/7.  
- **Análisis de documentos**: Extracción de contratos.  

### Riesgos:
- **Éticos**: Propagación de desinformación.  
- **Técnicos**: Requiere fine-tuning para dominios específicos (ejemplo: legal, médico).  

---

## Conclusión
- **Transformer** es la arquitectura detrás de los LLMs modernos, gracias a su **mecanismo de atención** y paralelización.  
- **LLMs** son poderosos pero requieren gestión cuidadosa para mitigar sesgos y errores.  
- **Futuro**: Modelos más eficientes (ejemplo: Mixture of Experts) y regulación ética.



### Componentes Explicados:
1. **Queries (Q)**, **Keys (K)**, **Values (V)**:
   - Representaciones aprendidas de cada palabra.
   - Ejemplo: Para "banco", Q busca información relevante; K y V proveen contexto.

2. **Producto QKᵀ**:
   - Mide compatibilidad entre palabras.
   - Ejemplo: Alta puntuación entre "banco" y "financiero".

3. **Escalado por √dₖ** (dₖ = dimensión de las claves):
   - Evita que softmax genere gradientes demasiado pequeños.

4. **Softmax**:
   - Normaliza pesos a valores entre 0 y 1 (probabilísticos).

5. **Producto con V**:
   - Combina los valores según los pesos calculados.


---



# Fundamentos de los Modelos de Lenguaje de Gran Escala (LLMs) y la Arquitectura Transformer

## Introducción: La Revolución del Lenguaje Digital

Los **Modelos de Lenguaje de Gran Escala (LLMs)**, como los que impulsan GPT-4 o Gemini, han transformado radicalmente la forma en que las máquinas interactúan y procesan el lenguaje humano. No son solo programas; son "prodigios matemáticos de la inteligencia artificial" que, a través de complejos cálculos de probabilidad, pueden predecir la siguiente palabra en una secuencia, generando respuestas que se asemejan al pensamiento humano.

Esta presentación busca desmitificar los LLMs y su arquitectura central, el Transformer, para entender:
1.  **Qué son** los LLMs y su funcionamiento básico.
2.  **Por qué el Transformer** fue una innovación clave.
3.  **El mecanismo de atención**, el "corazón" de estos modelos.
4.  Sus **capacidades y limitaciones** actuales, y cómo nos impactan en el mundo real.

### Un Vistazo Rápido a los LLMs

La historia de los LLMs se remonta a la teoría de la información de Claude Shannon en 1948, que ya veía el lenguaje como una serie de eventos probabilísticos. Modelos tempranos como Eliza (en los años 60) simulaban conversaciones, pero carecían de una verdadera comprensión contextual. Los LLMs modernos superan esto al calcular probabilidades estadísticas basadas en miles de millones de ejemplos, permitiéndoles predecir palabras en su contexto.

Para lograr esto, los LLMs procesan el lenguaje en varias etapas:
* **Tokenización:** El texto se divide en unidades fundamentales, llamadas tokens, que pueden ser palabras completas o partes de palabras. Por ejemplo, "increíble" podría dividirse en "in-", "creíble". Esto permite a la máquina interpretar el lenguaje.
* **Embeddings:** Estos tokens se transforman en representaciones numéricas, llamadas vectores. Las palabras con significados similares se agrupan en un "espacio" de alta dimensión, lo que permite a la máquina entender las relaciones profundas entre ellas.
* **Codificación Posicional:** Ayuda a los modelos a entender el orden de las palabras en una frase, un aspecto crucial para el significado.
* **Aprendizaje y Mejora:** Los modelos aprenden y se refinan continuamente ajustando sus parámetros internos mediante técnicas matemáticas avanzadas, reduciendo errores de predicción.

Estos modelos se integran en nuestra vida diaria, desde las sugerencias de texto en nuestros teléfonos hasta asistentes virtuales, diagnósticos médicos y *chatbots* de servicio al cliente.

---

## 1. ¿Qué es un LLM?

Un **Modelo de Lenguaje de Gran Escala (LLM)** es un tipo de inteligencia artificial diseñado para procesar, entender y generar texto. Su funcionamiento se basa en el aprendizaje de patrones a partir de enormes volúmenes de datos textuales (libros, artículos científicos, páginas web, etc.).

* **Funcionamiento Básico:** Un LLM recibe una secuencia de texto (una pregunta, una frase, un documento) y, basándose en los patrones que ha aprendido, genera una respuesta coherente y contextualmente relevante.
* **Naturaleza Estadística:** Su "inteligencia" reside en su capacidad para identificar las relaciones estadísticas y probabilísticas entre palabras y frases, permitiéndoles predecir la secuencia más probable de palabras que sigue a una entrada dada.

### Capacidades Clave:
* **Generación de Texto Coherente:** Producen texto que puede ser indistinguible del escrito por humanos en estilo y fluidez.
* **Traducción Automática:** Realizan traducciones de texto entre diferentes idiomas.
* **Resumen de Documentos:** Son capaces de condensar textos largos en versiones más cortas y concisas, extrayendo la información esencial.
* **Razonamiento y Comprensión:** Pueden inferir, responder preguntas complejas y, hasta cierto punto, "razonar" con el lenguaje, mostrando una comprensión de conceptos y relaciones.

### Limitaciones Actuales:
* **Alucinaciones:** Pueden inventar información que suena plausible pero es incorrecta, no verificada o completamente falsa. Esto requiere supervisión humana en aplicaciones críticas.
* **Sesgos:** Reflejan y, en ocasiones, pueden amplificar los prejuicios y estereotipos presentes en los enormes conjuntos de datos con los que fueron entrenados.
* **Costo Computacional Elevado:** El entrenamiento de estos modelos es extremadamente intensivo en recursos. Requiere vastas infraestructuras con miles de unidades de procesamiento gráfico (GPUs) o tensorial (TPUs), lo que implica un consumo energético y una inversión económica considerables.

---

## 2. El Transformer: La Arquitectura que lo Cambió Todo

Antes de la llegada del Transformer en 2017, los modelos de lenguaje utilizaban arquitecturas como las Redes Neuronales Recurrentes (RNNs) o las Redes de Memoria a Largo Corto Plazo (LSTMs). Estas funcionaban procesando el texto de forma secuencial, palabra por palabra. Este enfoque presentaba dos desafíos importantes:
* **Problemas con Dependencias a Largo Alcance:** Les costaba recordar y relacionar información que se encontraba muy distante en un texto largo. Esto limitaba su comprensión del contexto global.
* **Ineficiencia en el Entrenamiento:** El procesamiento secuencial era inherentemente lento y no permitía aprovechar plenamente la capacidad de cálculo paralelo de las computadoras modernas.

### La Solución: La Arquitectura Transformer

Propuesta en el influyente artículo de Google "Attention is All You Need", la arquitectura Transformer revolucionó el campo del Procesamiento de Lenguaje Natural al introducir un enfoque innovador:
* **Procesamiento Paralelo:** A diferencia de los modelos anteriores, el Transformer puede analizar todas las palabras de una secuencia simultáneamente, no una por una. Esto lo hace mucho más rápido y eficiente, permitiendo entrenar modelos con volúmenes de datos masivos.
* **El Mecanismo de Auto-Atención:** Es el componente clave que permite este procesamiento paralelo y la comprensión profunda del contexto global en el lenguaje.
* **Componentes Principales:** Los Transformers suelen tener un **Encoder** (codificador), que procesa la entrada y extrae su significado, y un **Decoder** (decodificador), que genera la salida deseada. Sin embargo, algunos modelos modernos (como BERT) utilizan solo la parte del Encoder, mientras que otros (como GPT) se basan principalmente en el Decoder.

---

## 3. El Mecanismo de Atención: El Corazón del Transformer

El mecanismo de atención es lo que dota a los LLMs de una capacidad sin precedentes para entender el contexto de una manera profunda y eficiente.

### ¿Qué es?
Es un sistema que permite al modelo **pesar la importancia de cada palabra** en una secuencia en relación con todas las demás palabras de esa misma secuencia. Es como si el modelo pudiera "enfocar" dinámicamente su atención en las partes más relevantes del texto para entender el significado de una palabra específica.

### ¿Por qué es Crucial?
1.  **Captura de Contexto Global:** Permite al modelo entender cómo las palabras se relacionan entre sí, sin importar su distancia física en la frase. Por ejemplo, en la frase "El **banco** financiero está cerca del río", cuando el modelo procesa la palabra "banco", el mecanismo de atención le permite darle mucho más peso a "financiero" (para entender que se refiere a una institución monetaria) y mucho menos peso a "río" (que en este caso no define el tipo de banco). Así, el modelo puede distinguir entre un "banco de un río" y un "banco financiero".
2.  **Eficiencia y Paralelización:** Al poder calcular estas relaciones de forma simultánea para todas las palabras en lugar de una a una, el mecanismo de atención es fundamental para la velocidad y eficiencia que caracterizan a los Transformers.
3.  **Resolución de Ambigüedades:** Esta capacidad de "enfocar" ayuda a resolver referencias ambiguas, como los pronombres. Por ejemplo, en "El perro persiguió al gato. **Él** corrió rápido.", la atención permite al modelo determinar que "él" se refiere al perro.

### Tipos de Atención:
* **Auto-atención (Self-Attention):** Este es el tipo principal, donde las palabras de una secuencia se relacionan entre sí para entender su contexto interno.
* **Atención Cruzada (Cross-Attention):** Se utiliza en los decodificadores para conectar la información procesada por el codificador (la entrada) con la que se está generando en la salida.

---

## 4. Procesamiento de Texto en Transformers: Un Flujo Simplificado

El flujo general de cómo un Transformer procesa el texto, desde la entrada hasta la generación de una respuesta, se puede simplificar en los siguientes pasos:
1.  **Embedding:** Las palabras o "tokens" de entrada se convierten en representaciones numéricas (vectores) que el modelo puede entender y manipular matemáticamente.
2.  **Capas de Atención:** Estas representaciones pasan por múltiples capas de auto-atención. Aquí es donde el modelo calcula y refina las relaciones de importancia entre todas las palabras de la secuencia.
3.  **Capas Feedforward:** Después de la atención, la información de cada palabra se procesa localmente en redes neuronales más simples, que refinan aún más las representaciones contextuales.
4.  **Generación (en el Decoder):** Si el modelo está generando texto (como en una conversación), el decodificador utiliza la información contextual procesada (ya sea del codificador o de su propia auto-atención) para predecir la siguiente palabra (o token) en la secuencia de salida. Este proceso se repite palabra por palabra hasta completar la respuesta.

---

## 5. Capacidades y Limitaciones en la Práctica

Como profesionales de la gestión de TI, somos testigos del vasto campo de aplicación de los LLMs y su potencial transformador en el ámbito empresarial:

### Aplicaciones Empresariales Innovadoras:
* **Chatbots y Asistentes Virtuales Avanzados:** Mejoran la atención al cliente, ofreciendo respuestas rápidas y precisas a preguntas frecuentes y gestionando consultas de manera eficiente las 24 horas del día.
* **Análisis y Resumen Inteligente de Documentos:** Automatizan la extracción de información clave de volúmenes masivos de contratos, informes legales, documentos técnicos o comunicaciones internas, agilizando procesos críticos.
* **Generación de Contenido a Escala:** Asisten en la creación de una amplia variedad de contenido, desde correos electrónicos personalizados y artículos de marketing hasta descripciones de productos y borradores de informes.
* **Traducción y Localización Mejoradas:** Facilitan la comunicación global y la adaptación de contenido a diferentes mercados con mayor fluidez y precisión que nunca.

### Riesgos y Consideraciones Críticas (Desde la Gestión de TI):
* **Riesgos Éticos y de Desinformación:** La capacidad de generar texto convincente y realista puede ser utilizada para propagar desinformación, *fake news* o contenido dañino. Esto requiere una gobernanza de la IA y un monitoreo constante.
* **Sesgos Inherentes:** Si los datos de entrenamiento contienen sesgos sociales, los LLMs pueden replicarlos y amplificarlos, lo que lleva a respuestas injustas o discriminatorias. La gestión de datos y la auditoría de modelos son esenciales.
* **Alucinaciones y Fiabilidad:** La tendencia de los LLMs a "inventar" información (alucinaciones) es un desafío importante para su fiabilidad. En aplicaciones críticas, es imperativo diseñar sistemas con mecanismos de verificación y supervisión humana.
* **Requerimientos de *Fine-tuning* y Especialización:** Para dominios muy específicos (legal, médico, ingeniería), los LLMs generales a menudo necesitan un "ajuste fino" con conjuntos de datos especializados. Esto implica experiencia técnica y recursos adicionales.
* **Dependencia de la Calidad de los Datos:** El rendimiento y la utilidad de un LLM dependen directamente de la calidad, diversidad y limpieza de los datos de entrenamiento. Una buena gestión de datos es la base del éxito de la IA.

---

## Conclusión: Hacia una Gestión Consciente de la IA

La arquitectura **Transformer** y su innovador **mecanismo de atención** son, sin duda, los pilares que han permitido el avance exponencial de los **LLMs** modernos. Estos modelos son herramientas extraordinariamente poderosas, capaces de comprender y generar lenguaje de formas que antes parecían ciencia ficción.

Sin embargo, su implementación y gestión en cualquier organización o sector requieren una atención meticulosa y una estrategia bien definida. Como líderes en gestión de TI y analítica, nuestra responsabilidad es:
* **Comprender sus fundamentos** y capacidades de manera clara y sin tecnicismos excesivos.
* **Evaluar sus aplicaciones prácticas** y el retorno de inversión potencial para nuestras organizaciones.
* **Implementar estrategias robustas para mitigar los riesgos**, como los sesgos algorítmicas, las alucinaciones y las implicaciones éticas.
* **Considerar la infraestructura tecnológica y el impacto ambiental** asociados a su despliegue y operación.
* **Participar activamente en el debate público sobre su regulación y ética**, asegurando un desarrollo y uso responsable de la IA que beneficie a la sociedad en su conjunto.

El futuro de los LLMs apunta hacia modelos aún más eficientes, capaces de integrar información de múltiples modalidades (texto, imágenes, sonido, video) y con capacidades de razonamiento cada vez más sofisticadas. Nuestra capacidad para gestionarlos de manera efectiva y ética determinará su impacto real y positivo en la estrategia y operación de las empresas.

---


## Diapositivas para Canva (Resumen)

### **Diapositiva 1: Mecanismo de Atención**  
**Título**: *¿Cómo los Transformers entienden contexto?*  
**Imagen**:  
- Frase *"El banco financiero"* con flechas gruesas entre "banco" y "financiero".  

---

### **Diapositiva 2: Fórmula Clave**  
```math
\text{Attention}(Q, K, V) = \text{softmax}\left(\frac{QK^T}{\sqrt{d_k}}\right)V
``` 
**Explicación visual**:  
- Q, K, V como cajas etiquetadas conectadas a una matriz de pesos.  

---

### **Diapositiva 3: Ejemplo Práctico**  
**Tabla**:  
| Palabra     | Peso de Atención |  
|-------------|------------------|  
| "financiero"| 0.85             |  
| "río"       | 0.10             |  

**Callout**: *"El modelo ignora 'río' al entender 'banco'"*.  

---

### **Diapositiva 4: ¿Por qué Importa?**  
**Ventajas**:  
✅ Contexto en textos largos.  
✅ Eficiencia computacional.  
**Iconos**: Cerebro (contexto), Reloj (velocidad).  

---

## Referencias

- [Large Language Models explained briefly](https://youtu.be/LPZh9BOjkQs?si=L2lAe6bGYfu9Rsk5)
- [Mathematics of LLMs, Explained in Everyday Language](https://youtu.be/1WHaFWMMXLI?si=4Wp3L2V2mazgWkDE)
- [Solving Combinatorial Problems Using Reinforcement Learning and LLMs](https://youtu.be/HmYqrhSJb6U?si=SMQF3bn8FP-MkSHV)
- [Visualizing transformers and attention | Talk for TNG Big Tech Day '24](https://youtu.be/KJtZARuO3JY?si=lrA5xwqBE545vn84)
- [But what is a neural network? | Deep learning chapter 1](https://youtu.be/aircAruvnKk?si=sp9Z0hhkJnbMGNoo)
- [Gradient descent, how neural networks learn | Deep Learning Chapter 2](https://youtu.be/IHZwWFHWa-w?si=ahYep9PICtoLgp1w)
- [Backpropagation, intuitively | Deep Learning Chapter 3](https://youtu.be/Ilg3gGewQ5U?si=oRU1RsnKtB372m3A)
- [Backpropagation calculus | Deep Learning Chapter 4](https://youtu.be/tIeHLnjs5U8?si=1Quw-Qf75209i39f)
- [Transformers, the tech behind LLMs | Deep Learning Chapter 5](https://youtu.be/wjZofJX0v4M?si=77XJr32TetcVtaOi)
- [Attention in transformers, step-by-step | Deep Learning Chapter 6](https://youtu.be/eMlx5fFNoYc?si=7lFIzg0vqatE1NS2)
- [How might LLMs store facts | Deep Learning Chapter 7](https://youtu.be/9-Jl0dxWQs8?si=eKyEA75cClQp30Ry)
- [Neural networks 3Blue1Brown](https://www.youtube.com/playlist?list=PLZHQObOWTQDNU6R1_67000Dx_ZCJB-3pi)

# 🧠 Resumen del video [Mathematics of LLMs in Everyday Language](https://www.youtube.com/watch?v=1WHaFWMMXLI) para facilitar la comprensión de los fundamentos técnicos.

---

## 🧭 ¿Qué es un LLM?

Un **Large Language Model (LLM)** es un sistema de inteligencia artificial entrenado para comprender y generar lenguaje humano. Utiliza redes neuronales profundas para procesar texto, responder preguntas, traducir idiomas, escribir código y más.

---

## 🔍 Fundamento Matemático (Resumen del video)

El video explica cómo los LLMs evolucionaron desde simples sistemas de autocompletado hasta modelos capaces de razonamiento complejo. Los puntos clave incluyen:

- **Tokens y vectores**: Las palabras se convierten en números (tokens) y se representan como vectores en espacios multidimensionales.
- **Funciones de activación**: Se aplican funciones como ReLU o tanh para transformar los vectores y permitir que la red aprenda patrones.
- **Backpropagation**: Técnica que ajusta los pesos de la red neuronal para minimizar errores, usando derivadas y gradientes.
- **Optimización**: Se utiliza el descenso de gradiente para mejorar el rendimiento del modelo en cada iteración.
- **Capas y atención**: Los modelos modernos como Transformers usan mecanismos de atención para enfocarse en partes relevantes del texto.

> 🧠 El video logra traducir estos conceptos complejos a lenguaje cotidiano, usando analogías visuales y ejemplos simples.

---

## 🧩 ¿Cómo se relaciona esto con la gestión de TI?

Desde una perspectiva de gestión tecnológica, los LLMs representan una nueva capa de infraestructura digital que:

- **Automatiza procesos**: Desde atención al cliente hasta análisis de datos.
- **Optimiza decisiones**: Mediante generación de reportes, resúmenes y recomendaciones.
- **Requiere gobernanza**: Por su capacidad de generar contenido autónomo, es vital establecer políticas de uso, seguridad y ética.

---

## 🧠 Conceptos Clave para No Especialistas

| Concepto              | Explicación sencilla                                      |
|-----------------------|-----------------------------------------------------------|
| Token                 | Fragmento de texto convertido en número                   |
| Vector                | Representación matemática de un token                     |
| Red neuronal          | Sistema que aprende patrones en datos                     |
| Backpropagation       | Método para corregir errores en el modelo                 |
| Gradiente             | Indicador de qué tan lejos está el modelo de la respuesta correcta |
| Optimización          | Proceso de mejora continua del modelo                     |
| Atención              | Mecanismo que permite al modelo enfocarse en lo relevante |

---

## 📌 Conclusión

Los LLMs no son magia, sino el resultado de aplicar matemáticas avanzadas a grandes volúmenes de texto. Comprender sus fundamentos permite a profesionales de TI y ejecutivos tomar decisiones informadas sobre su adopción, integración y regulación.

> 🎯 La clave está en traducir complejidad técnica en valor estratégico.

---

¡Por supuesto! Aquí tienes la estructura lista para copiar y pegar en Canva como presentación ejecutiva. Puedes usar una plantilla estilo "Educativo", "Moderno Profesional" o "Tecnología Didáctica".

---

### 🖼️ Presentación Editable – Fundamentos de los LLMs y su Base Matemática

---

**Slide 1: Título**  
🧠 **Entendiendo los Modelos de Lenguaje (LLMs)**  
Una introducción accesible a su funcionamiento, base matemática y relevancia en gestión TI

---

**Slide 2: ¿Qué es un LLM?**  
- Un modelo de lenguaje entrenado con grandes volúmenes de texto  
- Capaz de generar respuestas, resumir, traducir, escribir código  
- Utiliza redes neuronales profundas para interpretar el lenguaje humano

---

**Slide 3: Fundamento Matemático (Resumen del video)**  
- Las palabras se representan como **tokens y vectores**  
- Se transforman con **funciones de activación**  
- **Backpropagation** corrige errores aprendiendo del resultado  
- Se usa **descenso de gradiente** para optimizar  
- Las **capas de atención** enfocan el modelo en lo más relevante

---

**Slide 4: Conceptos Clave Simplificados**

| Término        | Explicación breve                    |
|----------------|--------------------------------------|
| Token          | Fragmento de texto convertido a número |
| Vector         | Representación matemática del token |
| Red neuronal   | Sistema que aprende patrones        |
| Gradiente      | Medida de error                     |
| Atención       | Mecanismo que da foco contextual    |

---

**Slide 5: Gestión TI y LLMs**

- Automatizan procesos repetitivos  
- Mejoran productividad en tareas cognitivas  
- Requieren gobernanza ética, normativa y estratégica  
- Representan infraestructura digital nueva y crítica

---

**Slide 6: Conclusión**

✨ **Los LLMs transforman el trabajo digital**  
- No son magia: son matemáticas aplicadas a escala  
- Su comprensión permite tomar decisiones informadas  
- El futuro está en saber usar la complejidad como ventaja

---

