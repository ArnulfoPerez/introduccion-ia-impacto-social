---
---
# Fundamentos Conceptuales del Machine Learning:  


---

## I. Regresión: El Corazón Matemático del Aprendizaje  

### ¿Qué es Regresión?  
En esencia, **encontrar la mejor curva** que explique una nube de puntos. Formalmente:  

```math  
\min_{θ} \sum_{i=1}^n (y_i - f(x_i; θ))^2
```
donde 
```math
f(x;θ)
```
es nuestro modelo y θ sus parámetros.

#### Ejemplo intuitivo:

Ajustar una recta (regresión lineal) a datos de precio de casas vs. metros cuadrados.

### Conexión con Redes Neuronales
Una red neuronal es una función paramétrica ultra-flexible:

- Capas ocultas = transformaciones no lineales
- Parámetros θ = pesos sinápticos
- Entrenar = ajustar θ para minimizar error (como en regresión, pero con gradiente descendente).

## II. 🧠 Overfitting

### ❓ ¿Qué es?

El **overfitting** ocurre cuando un modelo aprende demasiado bien los datos de entrenamiento, incluyendo el **ruido y las excepciones**, en lugar de captar los **patrones generales**.

Esto significa que cuando el modelo tiene muchos parámetros (θ) y poca señal útil en los datos, existe gran riesgo de que aprenda ruido.

---

## 🛡️ Estrategias Antídoto

### 1. 📊 Gestión Inteligente de Datos

| Conjunto      | Propósito                         | % Típico    |
|---------------|-----------------------------------|-------------|
| Entrenamiento | Ajustar parámetros (θ)            | 60–70%      |
| Validación    | Tunar hiperparámetros             | 15–20%      |
| Prueba        | Evaluación final (¡solo una vez!) | 15–20%      |

🔁 **Protocolo clave**:  
**K-fold Cross-Validation**  
→ Dividir datos en K bloques, usar K–1 para entrenar, 1 para validar, rotar el proceso.

---

### 2. 🧮 Regularización

- **L1 / L2**: Penalizan parámetros grandes para evitar sobreajuste.
```math
  $$L_{\text{total}} = L_{\text{error}} + \lambda \|θ\|^2$$
```

Penaliza parámetros demasiado grandes

λ controla la fuerza de la regularización

### Dropout:

- Apaga neuronas aleatoriamente durante entrenamiento
- Previene dependencias excesivas entre neuronas
- **Dropout**: Apagar neuronas aleatoriamente durante el entrenamiento para obligar al modelo a generalizar.

---

## Referencias

- [Análisis de la regresión](https://es.wikipedia.org/wiki/An%C3%A1lisis_de_la_regresi%C3%B3n)
