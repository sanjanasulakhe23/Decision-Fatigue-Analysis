## 🧠 Concept & Approach

Decision fatigue is not directly measurable in real-world datasets.  
To analyze it, this project models decision fatigue using **proxy lifestyle variables** that influence cognitive exhaustion.

The analysis is based on three core factors:
- Mental pressure (stress)
- Cognitive recovery (sleep quality)
- Physical recovery (physical activity)

---

## 📐 Metric Design

### Decision Fatigue Index
A weighted index was created to represent overall decision fatigue risk.

The index increases when:
- Stress levels are high
- Sleep quality is poor
- Physical activity is low

This reflects real-world behavior where sustained stress combined with insufficient recovery leads to cognitive exhaustion.

---

## ⚖️ Why Weights Were Used

Each factor does not contribute equally to decision fatigue, so weights were assigned based on relative influence:

- **Stress (0.5):** Primary driver of mental exhaustion and impaired decision-making.
- **Sleep Quality Deficit (0.3):** Poor sleep limits cognitive recovery and amplifies fatigue.
- **Physical Activity (0.2):** Supports recovery and reduces fatigue, therefore treated as a mitigating factor.

Weights reflect **logical causality and behavioral reasoning**, not arbitrary scaling.

---

## ➖ Why Subtraction and Transformation Were Applied

- **Physical activity is subtracted** because it reduces fatigue rather than increasing it.
- **Sleep quality is transformed (`10 − quality_of_sleep`)** to represent sleep deficit, ensuring all components move in the same direction.
- These transformations make the index interpretable, where higher values consistently indicate higher fatigue.

---

## 🧮 Cognitive Load Metric

A separate **Cognitive Load** metric was created to measure mental pressure relative to recovery capacity.

This captures scenarios where individuals with similar stress levels experience different fatigue depending on sleep duration.

---

## 🏁 Summary

This approach demonstrates how decision fatigue can be modeled using lifestyle and stress proxies.  
The resulting metrics provide an interpretable framework for identifying cognitive overload and fatigue risk using real-world data.
