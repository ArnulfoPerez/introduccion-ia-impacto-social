# La Conferencia de Dartmouth (1956)

El verano de 1956 en el Dartmouth College, **John McCarthy** (MIT) acuñó el término "inteligencia artificial" y reunió a los pioneros:

- **Los padres fundadores**:
  - **Marvin Minsky** (MIT): Teoría de marcos y sistemas simbólicos
  - **Claude Shannon** (Bell Labs): Teoría de la información aplicada a IA
  - **Allen Newell & Herbert Simon** (CMU): Lógica y resolución de problemas
  - **Nathaniel Rochester** (IBM): Primeras implementaciones prácticas

**Contexto clave**: 
- Guerra Fría en auge → Fondos militares para computación
- Optimismo posguerra: "Las máquinas pensarán en 10 años" (Minsky, 1967)
- **"Computing Machinery and Intelligence"** de Turing (1950) como inspiración

## El Perceptrón y sus Promesas (1958)

**Frank Rosenblatt** (Cornell) desarrolló el **Mark I Perceptron**, financiado por la Marina de EE.UU.:

- **Innovación**: Primera red neuronal capaz de aprender patrones simples
- **Texto clave**: *"Principles of Neurodynamics"* (1962)
- **Limitación**: Solo resolvía problemas linealmente separables

**Reacción del MIT**: 
- Minsky y Papert publican **"Perceptrons"** (1969) demostrando sus límites matemáticos
- Crítica mordaz: "No pueden aprender XOR" → Congela investigación en redes por 15 años

## El Invierno de la IA (1974-1980)

**Causas del colapso**:
1. **Expectativas irreales**: Proyectos como el *General Problem Solver* no escalaron
2. **Límites computacionales**: Memoria de 64KB en 1970 vs los TB actuales
3. **Recorte de fondos**: Informe Lighthill (UK, 1973) declaró la IA "un fracaso"

**Ironía histórica**: 
- Las críticas de Minsky al perceptrón eran correctas técnicamente, pero su pesimismo retrasó el desarrollo de redes profundas
- No anticipó que backpropagation + GPU resolverían esos límites décadas después

## Lecciones para el Presente

1. **Ciclos de hype**: Hoy con LLMs vivimos un nuevo verano, pero debemos aprender de la historia
2. **Importancia de fundamentos teóricos**: Como demostraron los trabajos de **Judea Pearl** (causalidad) y **Yann LeCun** (convoluciones)
3. **Ética desde el origen**: Los pioneros ignoraron el impacto social → hoy enfrentamos sesgos algorítmicos

---

# Diapositivas Resumen

## 1. Padres Fundadores y sus Obras
| Nombre | Contribución | Texto Clásico |
|--------|--------------|---------------|
| Alan Turing | Prueba de Turing | "Computing Machinery and Intelligence" (1950) |
| John McCarthy | LISP, IA simbólica | "Programs with Common Sense" (1958) |
| Marvin Minsky | Marcos cognitivos | "The Society of Mind" (1985) |
| Frank Rosenblatt | Perceptrón | "Principles of Neurodynamics" (1962) |

## 2. La Montaña Rusa de la IA
```mermaid
graph LR
  1956[Dartmouth] --> 1960s[Optimismo]
  1960s --> 1974[Invierno]
  1974 --> 1980s[Expert Systems]
  1980s --> 1990s[2do Invierno]
  1990s --> 2012[Deep Learning]
