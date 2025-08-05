## 📊 Análisis del Proyecto Final - Heart Disease Prediction

### 📌 Descripción del Dataset

Se utilizó el dataset **Heart Failure Prediction** de Kaggle, con un total de **918 registros** y 12 columnas que representan tanto variables clínicas (edad, presión arterial, colesterol) como categóricas (sexo, tipo de dolor torácico, resultados de electrocardiograma, etc.).

No se encontraron valores nulos. Las variables categóricas fueron transformadas mediante codificación *One-Hot Encoding* para su correcto procesamiento por el modelo.

---

### 🔍 Resultados del Análisis Exploratorio

- La variable `HeartDisease` está relativamente balanceada: alrededor del **55%** de los pacientes presentan la enfermedad.
- Se evidencian patrones importantes en variables como `Oldpeak`, `ChestPainType`, y `ExerciseAngina` relacionados con la variable objetivo.
- La edad promedio de los pacientes es de aproximadamente **53 años**.

---

### 🤖 Modelo y Evaluación

Se construyó un pipeline en Python usando programación orientada a objetos con un modelo de clasificación **Random Forest**. Este pipeline incluyó:

- Preprocesamiento de datos (limpieza + codificación)
- División del dataset en entrenamiento y prueba (80/20)
- Entrenamiento del modelo y evaluación de métricas

---

### 📈 Métricas de Evaluación (generadas por `classification_report`)

El modelo logró una **precisión (accuracy)** aceptable en la predicción general. Sin embargo, más allá del accuracy, se destacan las siguientes métricas clave para la clase **1 = enfermo**:

- **Recall**: Mide cuántos enfermos fueron detectados correctamente.
- **Precision**: Evalúa cuántos de los diagnosticados como enfermos realmente lo están.
- **F1-score**: Balance entre precisión y recall.

---

### 🩺 Evaluación Clínica del Modelo

Con base en los valores obtenidos para la clase positiva:

- Si el **recall ≥ 0.85**, el modelo es excelente para detectar pacientes con riesgo.
- Si el **recall está entre 0.7 y 0.85**, el modelo es funcional pero podría necesitar mejoras.
- Si el **recall < 0.7**, es riesgoso usarlo en un entorno clínico sin ajustes o validación adicional.

---

### ✅ Conclusión

El pipeline desarrollado demuestra un uso efectivo de paradigmas de programación y técnicas de aprendizaje automático para abordar un problema real de salud pública. Se recomienda continuar con el ajuste de hiperparámetros y aplicar validación cruzada para mejorar el rendimiento clínico del modelo.

