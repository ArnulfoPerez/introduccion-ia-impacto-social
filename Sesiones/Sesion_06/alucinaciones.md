# 🧠 Alucinaciones en modelos de lenguaje: qué son, por qué ocurren y cómo se están abordando

## 📌 Resumen ejecutivo

Las alucinaciones en modelos de lenguaje (LLMs) **no ocurren de forma completamente aleatoria**. Según investigaciones recientes, son **más probables** cuando:

- El prompt requiere una **respuesta larga o elaborada**.
- **No existe suficiente información** en el corpus de entrenamiento.
- La información disponible **contradice la premisa del prompt**.
- El tema involucra **opiniones mayoritarias erróneas** o **datos poco difundidos**.

Estas afirmaciones están respaldadas por estudios como el de [Nerds.ai](https://www.nerds.ai/blog/alucinaciones-en-llms-que-son-por-que-ocurren-y-como-mitigarlas-en-produccion) y [Unite.AI](https://www.unite.ai/es/qu%C3%A9-son-las-alucinaciones-llm-causas-preocupaci%C3%B3n-%C3%A9tica-prevenci%C3%B3n/), que analizan cómo los LLMs generan contenido plausible pero incorrecto cuando enfrentan ambigüedad, contradicción o falta de datos.

---

## 🧠 ¿Qué son las alucinaciones en IA?

Las **alucinaciones** son respuestas generadas por un modelo de lenguaje que **parecen coherentes y confiables**, pero **no están basadas en hechos reales**. Pueden incluir:

- Datos falsos (fechas, cifras, nombres).
- Citas inventadas.
- Narrativas que suenan verosímiles pero son ficticias.

---

## 🔍 ¿Por qué ocurren?

### Causas técnicas

- **Predicción probabilística**: Los LLMs predicen la siguiente palabra, no la verdad.
- **Falta de grounding**: No tienen conexión directa con bases de datos o el mundo real.
- **Corpus incompleto o sesgado**: Si el modelo no ha visto suficiente información sobre un tema, lo “rellena”.
- **Prompts ambiguos o contradictorios**: El modelo intenta resolver la ambigüedad con su mejor conjetura.

### Factores que aumentan el riesgo

| Factor del prompt                          | Riesgo de alucinación |
|--------------------------------------------|------------------------|
| Solicita respuesta larga o compleja        | Alto                   |
| Tema con poca difusión o datos limitados   | Alto                   |
| Premisa contradictoria o errónea           | Muy alto               |
| Opinión social dominante pero incorrecta   | Alto                   |
| Pregunta sobre eventos recientes           | Alto (si el modelo no está actualizado) |

---

## 🧪 Estado del arte en mitigación

### 🔧 Técnicas actuales

- **RLHF (Reinforcement Learning with Human Feedback)**: Entrenamiento por refuerzo con retroalimentación humana. Mejora la alineación del modelo con respuestas deseadas.
- **Detección a nivel de token**: Algoritmos que identifican tokens alucinados en tiempo real.
- **Fine-tuning con datos verificados**: Ajuste del modelo con corpus curado.
- **Guardrails y validación externa**: Sistemas que filtran o corrigen respuestas antes de mostrarlas.

### 🧠 Avances recientes

- OpenAI y DeepMind han desarrollado variantes de RLHF para reducir alucinaciones en ChatGPT y Gemini.
- Investigadores como Ilya Sutskever afirman que el refuerzo posterior puede enseñar al modelo a no alucinar.
- Nuevos modelos como Claude 3 y DeepSeek R1 incorporan mecanismos de verificación interna y razonamiento paso a paso.

---

## 🧭 ¿Qué puede hacer el usuario?

- **Verificar fuentes**: No confiar ciegamente en respuestas generadas.
- **Usar prompts claros y específicos**.
- **Solicitar citas o referencias**.
- **Comparar respuestas entre modelos**.

---

## 📚 Referencias

- [Nerds.ai: Qué son las alucinaciones y cómo mitigarlas](https://www.nerds.ai/blog/alucinaciones-en-llms-que-son-por-que-ocurren-y-como-mitigarlas-en-produccion)
- [Unite.AI: Causas y prevención de alucinaciones](https://www.unite.ai/es/qu%C3%A9-son-las-alucinaciones-llm-causas-preocupaci%C3%B3n-%C3%A9tica-prevenci%C3%B3n/)
- [Jucaripo: Impacto y causas de alucinaciones en IA](https://jucaripo.com/2025/06/ia-alucinaciones-causas-impacto-consejo/)

---

## 🖼️ Diapositivas resumen

### Slide 1: ¿Qué son las alucinaciones?
- Definición
- Ejemplos comunes

### Slide 2: ¿Por qué ocurren?
- Predicción probabilística
- Corpus incompleto
- Prompts ambiguos

### Slide 3: ¿Cuándo son más probables?
- Respuestas largas
- Temas contradictorios
- Opiniones sociales erróneas

### Slide 4: ¿Cómo se mitigan?
- RLHF
- Detección token por token
- Validación externa

### Slide 5: ¿Qué puede hacer el usuario?
- Verificar
- Prompting claro
- Comparar modelos

---

