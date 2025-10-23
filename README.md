# Modelos de Sincronización: Kuramoto y Winfree

Este repositorio explora y analiza dos modelos fundamentales de sincronización en sistemas complejos:  
**el modelo de Kuramoto** y **el modelo de Winfree**.  

Ambos son paradigmas en el estudio del acoplamiento de osciladores y permiten comprender fenómenos como la sincronización neuronal, la coherencia en redes eléctricas y los ritmos biológicos.

---

## 1) Interpretación de las figuras (qué mirar)

### 🔹 **r(t): parámetro de sincronía**

\( r ∈ [0,1] \)

- Valores cercanos a **1 → alta sincronía** (fases agrupadas).  
- Valores cercanos a **0 → fases distribuidas aleatoriamente**.  

Observa la **velocidad de crecimiento de ( r(t) )** y su **valor final**, ya que indican cuán rápido y cuánto sincroniza el conjunto.

---

### 🔹 **Raster (fases vs tiempo)**

- Líneas con pendiente constante y **agrupamientos verticales** indican osciladores que han quedado en fase y comparten frecuencia.  
- Si las columnas se alinean verticalmente o las fases se superponen → hay **bloqueo de fase**.

---

### 🔹 **Diagramas polares finales**

- Muestran directamente si las fases se **agrupan (clúster visible)** o permanecen **distribuidas aleatoriamente**.

---

### 🔹 **Histogramas de frecuencias estimadas**

- Indican si las frecuencias convergen a un **valor común (entrainment)** o quedan **distribuidas**.  

> En un ejemplo, **ambos modelos alcanzan sincronía** ( r → 1 \).  
> Dependiendo de los parámetros **K**, **N**, y la dispersión de (ω), pueden observarse transiciones **sincrónico ↔ incoherente**.

---

## 2) Comparación funcional Kuramoto vs Winfree

###  **Mecánica de acoplamiento**

| Modelo | Descripción |
|:--------|:-------------|
| **Kuramoto** | Acoplamiento emparejado y sinusoidal entre pares. Modelo simple y analíticamente tratable. Define un parámetro de orden natural \( r(t) \). |
| **Winfree** | Acoplamiento global mediado por señales/pulsos **P(θ)** y la sensibilidad de cada oscilador **Q(θ)**. Modela interacción por impulsos y respuesta de fase (PRC). |

---

###  **Diferencias prácticas observables**

- **Umbral de sincronización:**  
  Ambos muestran transiciones, pero **Winfree** puede sincronizar más fácilmente dependiendo de las funciones \( P/Q \), ya que el acoplamiento entra multiplicativamente por la PRC. La dinámica puede ser más abrupta o no lineal.

- **Fases y agrupamiento:**  
  - **Kuramoto:** sincronía por acoplamiento *pairwise* (seno de diferencias de fase).  
  - **Winfree:** sincronía dependiente de la **curva de respuesta Q(θ)**, pudiendo favorecer ciertos osciladores.

- **Robustez a heterogeneidad:**  
  **Winfree** puede adaptarse mejor si \( P/Q \) están ajustadas a la naturaleza del sistema (por ejemplo, pulsos fuertes que arrastran osciladores diversos).

---

###  **Gráficos**

| Tipo de gráfico | Qué representa | Qué esperar |
|:-----------------|:----------------|:-------------|
| **r(t)** | Nivel global de sincronía | Curva ascendente hacia 1 si sincroniza |
| **Raster** | Evolución de fases individuales | Alineamientos verticales = sincronía |
| **Diagrama polar** | Distribución final de fases | Clúster compacto si hay coherencia |
| **Histograma de frecuencias** | Frecuencias finales | Pico único si hay entrainment |

---

###  **Resumen funcional**

| Modelo | Características principales |
|:--------|:------------------------------|
| **Kuramoto** | Modelo *pairwise*, acoplamiento sinusoidal, base teórica para transiciones de sincronía. |
| **Winfree** | Modelo *pulso + PRC*, más realista para sistemas con interacción impulsiva (neuronas, luciérnagas, células cardíacas). |

---

##  3) Aplicación: sincronización en redes eléctricas (generadores síncronos)

### **Contexto**

En sistemas de potencia, la frecuencia (50/60 Hz) debe mantenerse **uniforme** en toda la red.  
Cada generador tiene una **fase** y **frecuencia natural** que ajusta con controladores, y las **líneas eléctricas** acoplan sus fases.

---

### **Por qué la sincronización importa**

Si los generadores se desincronizan, aparecen corrientes incontroladas, fluctuaciones de frecuencia y riesgo de apagones en cascada. El comportamiento colectivo de múltiples generadores y cargas se puede estudiar con modelos simplificados de osciladores acoplados (Kuramoto modificado y variantes de Winfree) para entender estabilidad, umbrales de fallo, y estrategias de control.

---

### **Cómo se aplica**

- **Modelado rápido:**  
  Usar modelos tipo Kuramoto para estudiar estabilidad y detectar condiciones donde la red perdería sincronía.

- **Diseño de control:**  
  Estimar cuánto acoplamiento (líneas o potencia) o qué acción de control se requiere para restaurar sincronía.

- **Análisis de perturbaciones:**  
  Simular pérdidas de generadores o fluctuaciones de carga y verificar si el sistema vuelve al estado sincronizado.

---

### **Por qué Kuramoto y Winfree son válidos**

Aunque las redes eléctricas reales más complejas incluyen **(inercia, controladores y retardos)**, modelos de osciladores acoplados capturan el mecanismo esencial de acoplamiento de fase y permiten análisis teórico y numérico eficiente, lo que permite:

- Análisis teórico eficiente.  
- Simulación numérica rápida.  
- Interpretación clara de la **estabilidad colectiva**.

---

### **Otras aplicaciones**

- 🧠 **Neurociencia:** sincronía neuronal y patologías como Parkinson.  
- ⏰ **Ritmos biológicos:** circadianos, cardíacos y hormonales.  
- 🔦 **Sistemas naturales:** sincronía en luciérnagas, bacterias y células.  
- 🤖 **Tecnología:** sincronización de relojes distribuidos, redes de sensores y robótica colaborativa.

---
