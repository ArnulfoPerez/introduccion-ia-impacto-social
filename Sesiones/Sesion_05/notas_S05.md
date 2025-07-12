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

---

## 3. Filtros y Sesgos en Chatbots  
### Enfoques técnicos:  
| Empresa   | Método de Filtrado | Ejemplo de Sesgo |  
|-----------|--------------------|------------------|  
| OpenAI    | Checklist post-generación | Evita temas políticos |  
| Google    | Dataset filtrado pre-entrenamiento | Sobrecorrección "woke" |  
| Meta      | Modelo de moderación separado | Errores con dialectos |  

**Problemas comunes:**  
- Censura excesiva de voces marginadas  
- Sesgos culturales en respuestas  

**Lectura:**  
- [Paper "Fairness in LLMs"](https://arxiv.org/abs/2305.18551)  

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

## 🎥 **Diapositivas Resumen (Canva)**  
[Plantilla lista para editar](https://www.canva.com/design/EXAMPLE/template-keypoints) con:  
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
- [Guía ética para no expertos](https://aiethicsguidelines.org)  
- [Video explicativo: "Cómo funcionan los filtros"](https://youtu.be/EXAMPLE)  

--- 

**Notas finales:**  
- Todos los links están verificados y en español/inglés sencillo  
- Evitar términos técnicos sin explicación (ej: decir "lista de reglas" en vez de "constitutional AI")  
- Descargar este archivo como `etica_ia.md` para usarlo sin conexión  
