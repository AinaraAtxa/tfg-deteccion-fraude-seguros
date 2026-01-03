# Detección de fraude en siniestros de automóvil mediante aprendizaje automático

Trabajo Final de Grado – Grado en Ciencia de Datos Aplicada  
Universitat Oberta de Catalunya (UOC)

Autora: Ainara Acha Sánchez  
Tutor: Antonio Gutiérrez Blanco  
Fecha: Enero 2026

---

## Descripción del proyecto

Este repositorio contiene el código y la documentación asociada al Trabajo Final de Grado  
**“Detección del fraude en siniestros de automóvil mediante aprendizaje automático”**.

El objetivo del proyecto es desarrollar un sistema predictivo capaz de estimar la probabilidad
de fraude en partes de siniestro de automóvil, combinando:

- Modelos de *machine learning* (Random Forest)
- Técnicas de explicabilidad (SHAP y LIME)
- Un agente basado en un modelo de lenguaje local (LLM) para interpretar descripciones
  en lenguaje natural y generar explicaciones comprensibles

El sistema está orientado a tareas de **cribado y priorización** de siniestros sospechosos.

---

## Estructura del repositorio

├── notebooks/
├── data/
├── models/
├── memory/
├── requirements.txt
└── README.md


---

## Dataset

Se utiliza el dataset **Vehicle Insurance Claim** disponible en Kaggle (Oracle).

Por motivos de licencia, el dataset no se incluye directamente en el repositorio.
Puede descargarse desde:

https://www.kaggle.com/datasets/shivamb/vehicle-insurance-claim-dataset

Una vez descargado, debe colocarse en la carpeta `data/`.

---

## Modelo LLM

El agente de lenguaje natural utiliza un modelo **local** basado en:

- **Mistral-7B-Instruct (GGUF)**
- Ejecutado mediante `llama-cpp-python`

El archivo del modelo no se incluye en el repositorio debido a su tamaño.

Puede descargarse, por ejemplo, desde Hugging Face:

https://huggingface.co/TheBloke/Mistral-7B-Instruct-v0.2-GGUF

Colocar el archivo `.gguf` en la carpeta `models/`.

---

## Requisitos y entorno

- Python 3.10+
- Jupyter Notebook

Instalación de dependencias:

```bash
pip install -r requirements.txt
```

## Principales librerías utilizadas:
scikit-learn
pandas
numpy
imbalanced-learn
shap
lime
llama-cpp-python

## Ejecución

Descargar el dataset y el modelo LLM

Instalar las dependencias

Ejecutar el notebook notebooks/deteccion_fraude_seguros.ipynb

## Resultados principales
Recall fraude ≈ 50 %
ROC-AUC ≈ 0.84
Alta capacidad de priorización (Lift > 3 en el primer decil)

El modelo resulta adecuado como sistema de apoyo a la toma de decisiones,
no como sustituto de la revisión humana.

## Licencia

Este proyecto se distribuye bajo licencia Creative Commons
Reconocimiento-NoComercial-SinObraDerivada 3.0 España.

