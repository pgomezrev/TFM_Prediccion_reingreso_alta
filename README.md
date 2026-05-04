# Predicción de reingreso hospitalario a 30 días

**Trabajo Fin de Máster – Ciencia de Datos**

## Descripción del proyecto

Este proyecto tiene como objetivo el desarrollo de un modelo predictivo capaz de estimar la probabilidad de reingreso hospitalario en los 30 días posteriores al alta, utilizando técnicas de aprendizaje automático aplicadas a datos clínicos y administrativos.

El problema se formula como una tarea de **clasificación binaria**, donde se predice si un paciente será readmitido o no en dicho intervalo temporal. Este tipo de análisis tiene un alto interés en el ámbito sanitario, ya que permite identificar pacientes de riesgo y optimizar la gestión de recursos hospitalarios.

---

## Objetivos

* Analizar la estructura y calidad de un dataset clínico real
* Realizar un pipeline completo de ciencia de datos (EDA → preprocessing → modelado)
* Desarrollar modelos predictivos basados en machine learning
* Evaluar el rendimiento de los modelos mediante métricas adecuadas
* Analizar la interpretabilidad de los resultados

---

## Dataset

Se utiliza el dataset público:

**Diabetes 130-US hospitals (1999–2008)**
Disponible en:
https://archive.ics.uci.edu/dataset/296/diabetes+130-us+hospitals+for+years+1999-2008

Características principales:

* Más de 100.000 episodios hospitalarios
* Variables demográficas, clínicas y administrativas
* Información longitudinal de pacientes (anonimizada)
* Variable objetivo: readmisión hospitalaria

---

## 🧱 Estructura del proyecto

```bash
.
├── data/
│   ├── raw/                # Dataset original
│   ├── processed/          # Datos preprocesados
│
├── notebooks/
│   ├── 01_EDA.ipynb        # Análisis exploratorio de datos
│   ├── 02_preprocessing.ipynb  # Limpieza, feature engineering y preparación
│   ├── 03_modeling.ipynb   # Modelado y evaluación
│
├── environment.yml         # Entorno reproducible (conda)
├── README.md               # Documentación del proyecto
```

---

## Pipeline del proyecto

El desarrollo sigue un enfoque estructurado en varias fases:

### 1. Análisis exploratorio (EDA)

* Calidad de datos
* Valores missing
* Distribución de variables
* Análisis de la variable objetivo
* Identificación de variables problemáticas

### 2. Preprocesamiento

* Limpieza de datos (`?` → NaN)
* Tratamiento de valores ausentes
* Selección de variables
* Feature engineering
* Reducción de cardinalidad
* Codificación de variables categóricas
* División train/test

### 3. Modelado (fase posterior)

* Regresión logística (baseline)
* Random Forest
* XGBoost
* Evaluación con AUC-ROC, recall, precision, F1-score
* Interpretabilidad (SHAP)

---

## Consideraciones metodológicas

* El problema presenta **desbalanceo de clases (~11% positivos)**
* Se prioriza el **recall** debido al coste clínico de falsos negativos
* Se evita el uso de técnicas de oversampling en preprocessing para preservar la integridad de los datos
* Se utilizan técnicas de interpretabilidad para garantizar la comprensión del modelo

---

## Cómo ejecutar el proyecto

### 1. Clonar el repositorio

```bash
git clone https://github.com/tu_usuario/tu_repositorio.git
cd tu_repositorio
```

### 2. Crear entorno conda

```bash
conda env create -f environment.yml
conda activate nombre_del_entorno
```

### 3. Ejecutar notebooks

```bash
jupyter notebook
```

Seguir el orden:

1. `01_EDA.ipynb`
2. `02_preprocessing.ipynb`
3. `03_modeling.ipynb`

---

## Resultados esperados

El objetivo no es únicamente maximizar el rendimiento predictivo, sino:

* Obtener un modelo **interpretativo**
* Identificar **factores relevantes de riesgo**
* Evaluar la **viabilidad real** del enfoque en datos administrativos

---

## Contexto académico

Este proyecto se enmarca dentro del:

* Máster en Ciencia de Datos
* Área: Machine Learning aplicado a datos clínicos

---

## Autor

Pedro Gómez Revilla

---

## Licencia

Este proyecto se desarrolla con fines académicos. El dataset utilizado es público y está sujeto a sus propias condiciones de uso.

---

## Disclaimer

Este proyecto tiene fines exclusivamente académicos.
No debe utilizarse para la toma de decisiones clínicas reales.
