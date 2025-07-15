# Material de Referencia: Dilemas Éticos y Gobernanza en IA    

---

## 🌐 **Temas Cubiertos**  
1. Manipulación de narrativas mediante IA y redes sociales  
2. Alineación empresa-gobierno en vigilancia masiva (caso Palantir)  
3. Filtros de contenido y sesgos en LLMs/Chatbots  
4. Mecanismos contra alucinaciones en IA  

---

## 1. Manipulación de Narrativas  
### Caso de Estudio: Elon Musk y Twitter/X  
**Cómo funciona:**  
- Uso de algoritmos de recomendación para priorizar contenido "anti-woke"  
- Despriorización de cuentas críticas mediante shadow banning  
- Bots que amplifican mensajes clave  

**Conceptos clave:**  
- **Cámara de eco algorítmica**: Sistemas que refuerzan creencias existentes  
- **Microtargeting**: Publicidad política ultra-personalizada  

**Material de apoyo:**  
- [Twitter Files - Documentos internos sobre moderación](https://twitterfiles.com)   
- [Platform Manipulation in 2023](https://www.rand.org/content/dam/rand/pubs/perspectives/PEA2600/PEA2679-1/RAND_PEA2679-1.pdf)
- [Cómo Elon Musk destruyó Twitter y cómo salvarlo](https://www.washingtonpost.com/es/post-opinion/2023/01/02/elon-musk-twitter-encuesta-periodistas/)
- [The Hill & Valley Forum](https://www.youtube.com/@HillValleyForum)
- [Forging the Technological Republic](https://www.youtube.com/live/uQCazCId_9o?si=FzwXM4817BtZIo0f&t=4790)

---

## 2. Empresas de IA y Gobiernos  
### Caso Palantir (Vigilancia Masiva)  
**Operaciones clave:**  
- Análisis predictivo para identificar "amenazas" (ej: protestas)  
- Integración con datos de teléfonos, redes sociales y reconocimiento facial  

**Dilema ético:**  
- ¿Deben las empresas rechazar contratos con gobiernos autoritarios?  

**Recursos:**  
- [Informe Amnesty sobre Palantir](https://doc.es.amnesty.org/ms-opac/doc?q=norm%3Asiai+AND+media%3Atrue+AND+msstored_doctype%3ADocumentaci%C3%B3n&start=3371&rows=1&sort=fecha%20asc&fq=norm&fv=*&fo=and) 
- [Contratos con ICE (EE.UU.)](https://www.lanacion.com.ar/estados-unidos/migraciones/immigrationos-asi-funciona-el-nuevo-software-para-rastrear-migrantes-para-ice-nid10052025/)
- [Palantir CEO Alex Karp and Jacob Helberg | Hill & Valley Forum 2024](https://www.youtube.com/watch?app=desktop&v=MqXQFfCIOiA)
- [There have been 500 days genocide and Palantir is responsible for killig innocent civilians in Gaza](https://youtu.be/RPQFWWXrEJc?si=w7v6Ew7ybdL80rIo)
- [Viral Palantir protester warns all complicit in Gaza horrors](https://www.aa.com.tr/en/middle-east/interview-expose-them-viral-palantir-protester-warns-all-complicit-in-gaza-horrors/3565328)
- [Palantir allegedly enables Israel's AI targeting in Gaza, raising concerns over war crimes](https://www.business-humanrights.org/es/%C3%BAltimas-noticias/palantir-allegedly-enables-israels-ai-targeting-amid-israels-war-in-gaza-raising-concerns-over-war-crimes/)
- [Palantir allegedly supplying Israel with AI tools amid Israel's war in Gaza](https://www.business-humanrights.org/es/%C3%BAltimas-noticias/palantir-allegedly-supplying-israel-with-ai-tools-amid-israels-war-in-gaza/)
- [Palantir CEO Alex Karp on college protests and the future of war](https://youtu.be/E1schQrqJFU?si=HuvE9Whhmovbmvnu)
- [ICE firma contrato de $30M con Palantir para tecnología de datos](https://www.visaverge.com/es/noticias/ice-firma-contrato-de-30m-con-palantir-para-tecnologia-de-datos/)
- [InmigrationOS, la tecnología de vigilancia que Trump ha encargado a Palantir para monitorizar inmigrantes: “Pretende un control absoluto”](https://elpais.com/tecnologia/2025-04-25/inmigrationos-la-tecnologia-de-vigilancia-que-trump-ha-encargado-a-palantir-para-monitorizar-inmigrantes-pretende-un-control-absoluto.html)
- [El ICE y Palantir desarrollarán una nueva tecnología de IA para identificar a inmigrantes en EE UU](https://es.wired.com/articulos/ice-y-palantir-desarrollaran-nueva-tecnologia-para-identificar-a-inmigrantes-en-ee-uu)
- [Palantir se vuelve hostil contra periodistas por la cobertura sobre su relación con el gobierno de Trump](https://es.wired.com/articulos/palantir-se-vuelve-hostil-contra-periodistas-por-la-cobertura-sobre-su-relacion-con-el-gobierno-de-trump)
- [The Hill & Valley Forum 2025: Rebuilding America](https://www.youtube.com/live/uQCazCId_9o?si=mhW_Oq4AJ6dIRXcZ)
- [Palantir CEO Alex Karp & Rep. Ritchie Torres on Innovation & The West](https://youtu.be/DEZCBkn20Og?si=fSQ06YQ06FHrHY1z)
- [What is a long context window?](https://blog.google/technology/ai/long-context-window-ai-models/#:~:text=Previously%2C%20Gemini%20could%20process%20up,can%20take%20in%20and%20process.)

---

## 3. Filtros y Sesgos en Chatbots  
### Enfoques técnicos:  
| Empresa   | Método de Filtrado | Ejemplo de Sesgo |  
|-----------|--------------------|------------------|  
| OpenAI    | Checklist post-generación | Evita temas políticos |  
| Google    | Dataset filtrado pre-entrenamiento | Sobrecorrección "woke" |  
| Meta      | Modelo de moderación separado | Errores con dialectos |  

Los filtros de *political correctness* son mecanismos que limitan o moderan las respuestas de los modelos de lenguaje para evitar contenido ofensivo, discriminatorio o políticamente sensible. Estos filtros se implementan por razones éticas, legales y comerciales.

---

### 1. [Hablemos de Chatbots](https://www.youtube.com/watch?v=aQf9kzb_3ng)

- Los chatbots no son conscientes, pero pueden generar contenido sensible si no se filtra.
- Las empresas como OpenAI y Microsoft implementan APIs y capas de moderación para evitar que respondan sobre violencia, política extrema o contenido sexual.
- Estas limitaciones pueden afectar la autenticidad y utilidad del chatbot en ciertos contextos.

---

### 2. [¿Cómo funcionan los chatbots?](https://www.youtube.com/watch?v=Fw9tWZOraUo)

- Los modelos aprenden de datos públicos y luego se ajustan con reglas para evitar sesgos.
- Los filtros pueden limitar la expresión libre, pero también protegen contra desinformación y discurso de odio.
- Los moderadores humanos complementan el sistema para bloquear respuestas ofensivas.

---

### 3. [El renacer de los chatbots en la era de la IA Generativa](https://www.youtube.com/watch?v=z1SBcWzcpY0)

- Existe una tensión entre creatividad y seguridad, y los filtros pueden bloquear respuestas útiles en arte o filosofía.
- Los modelos modernos detectan intención y contexto, no solo palabras prohibidas.
- Se debate si los filtros reflejan valores universales o intereses corporativos.

---


**Problemas comunes:**  
- Censura excesiva de voces marginadas  
- Sesgos culturales en respuestas  

**Lectura:**  
- [Fairness in Large Language Models: A Taxonomic Survey](https://arxiv.org/abs/2404.01349)
- [Corredores de datos, empresas de análisis de datos, “registros musulmanes” y derechos humanos](https://medium.com/amnesty-insights/corredores-de-datos-empresas-de-an%C3%A1lisis-de-datos-registros-musulmanes-y-derechos-humanos-d0be38295a29)

---

## 4. Alucinaciones en IA  
### ¿Por qué ocurren?  
- Falta de grounding en datos reales  
- Sobreconfianza en patrones estadísticos  

**Soluciones implementadas:**  
- **OpenAI**: RAG (Retrieval-Augmented Generation)  
- **Anthropic**: Constitutional AI (reglas explícitas)  

**Ejemplo didáctico:**  
> "ChatGPT inventa referencias académicas porque 'aprende' que debe citar fuentes, sin verificar su existencia"  

---

# 🧠 ¿Qué son los filtros de corrección política en IA?

Los filtros de corrección política en IA son herramientas necesarias para evitar daños, pero generan debates sobre censura, libertad de expresión y sesgo institucional. Su implementación varía según la empresa, el país y el tipo de aplicación.

---


## 🎥 **Diapositivas Resumen (Canva)**  

1. Portada con título  
2. Infografía "Flujo de manipulación en redes"  
3. Tabla comparativa de filtros por empresa  
4. Diagrama simple "Cómo se generan alucinaciones"  
5. Casos prácticos para debate  

---

## 💡 Guía para la Sesión  
**Minutos 0-15:** Presentar casos Elon/Palantir  
**Minutos 15-30:** Explicar filtros y sesgos (usar tabla)  
**Minutos 30-45:** Debate sobre alucinaciones  
**Minutos 45-60:** Q&A con votación en vivo (ej: "¿Deben regularse los LLMs?")  

**Material adicional:**  
- [Guía ética de la UNESCO](https://www.unesco.org/en/artificial-intelligence/recommendation-ethics) 

--- 

# [El Fin de la Ley de Moore para la IA: ¿Por Qué los Ejecutivos de IA Están Aterrados?](https://www.youtube.com/watch?v=VhLeHvouPWs)

El video, presentado por Spencer de STARTUP HAKK, aborda un cambio crucial en el panorama de la inteligencia artificial: el fin de la suposición de que los costos de la IA disminuirán perpetuamente, una idea a menudo comparada con la Ley de Moore. Este cambio se evidencia con el reciente aumento de precios de Google para su modelo Gemini Flash.

## Puntos Clave del Video:

### 1. Aumento de Precios de Google y el Fin de la Tendencia
* **Precedente:** Google duplicó el precio de entrada de tokens de su modelo Gemini 2.5 Flash (de $0.15 a $0.30 por millón de tokens) y cuadruplicó el precio de salida (de $0.60 a $2.50 por millón de tokens). Esta es la primera vez que un proveedor importante de IA aumenta los precios de un modelo establecido, marcando un punto de inflexión.

### 2. La Realidad de los Costos Cuadráticos de la IA
* **Escalado no lineal:** El presentador explica que los costos de procesamiento de la IA no escalan linealmente, sino **cuadráticamente** con la longitud de la secuencia. Esto significa que si la longitud de entrada de un modelo se duplica, el costo de procesamiento se cuadruplica. Los proveedores de API han estado cobrando una tarifa plana por token, mientras que sus costos operativos reales aumentaban exponencialmente.

### 3. El Fin de los Subsidios
* **Quema de efectivo:** Las grandes empresas de IA han estado subsidiando los precios de sus servicios, quemando efectivo con la esperanza de alcanzar futuras economías de escala.
* **Límites físicos:** Este modelo de subsidio está llegando a su límite debido a limitaciones físicas y de hardware, como los altos costos de energía de los centros de datos y las limitaciones en el ancho de banda de la memoria de los chips de IA.

### 4. Cambio Estratégico Hacia el Procesamiento por Lotes
* **Límite de inferencia en tiempo real:** Dado que la inferencia de IA en tiempo real ha alcanzado un límite de costos, el procesamiento por lotes (procesar tareas en grupos en lugar de una por una) se vuelve mucho más atractivo.
* **Ahorros significativos:** Se pueden lograr ahorros de costos de hasta el 90% al procesar tareas en lotes en servidores locales en lugar de depender de APIs en tiempo real de terceros.

### 5. La Importancia de los Modelos de Código Abierto y el Control de Datos
* **Alternativa rentable:** Se recomienda el uso de modelos de código abierto (como los disponibles en plataformas como Olama), ya que ofrecen un rendimiento equivalente o superior a una fracción del costo, eliminando la dependencia de un único proveedor.
* **Soberanía de datos:** Mantener los datos y los modelos en servidores propios permite a las empresas retener el control total de su información, un aspecto crucial para la seguridad y la privacidad.

### 6. Límites Fundamentales de los LLMs
* **Restricciones físicas y de datos:** El video destaca que los modelos de lenguaje grandes (LLM) están alcanzando límites fundamentales debido a restricciones físicas en el ancho de banda de la memoria y a la escasez de datos de entrenamiento de alta calidad.
* **"Colapso del modelo":** Entrenar con datos sintéticos o repetidos puede llevar al "colapso del modelo", donde el rendimiento del LLM se degrada significativamente.

### 7. Implicaciones Críticas para las Empresas
* **Gestión de costos:** Las empresas ya no pueden asumir que los costos de la IA disminuirán. Los gerentes de producto y líderes de TI deben integrar la gestión de costos como una característica principal en sus estrategias de IA.
* **Inversión en infraestructura:** Las empresas deben considerar invertir en arquitecturas de procesamiento por lotes y en infraestructura para modelos de código abierto para optimizar costos y mantener el control.

Spencer, a través de Starter Pack, ofrece servicios de desarrollo de software y consultoría para ayudar a las empresas a navegar por estos cambios, enfocándose en la conexión de sistemas y la creación de agentes de IA personalizados.
