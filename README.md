#  Sistema de Diagnóstico Asistido por IA

> **Resumen corto:** Desarrollo de un sistema basado en inteligencia artificial para la detección temprana de cáncer de tiroides mediante imágenes ecográficas, evaluando modelos de Machine Learning y Deep Learning.

[![Estado](https://img.shields.io/badge/status-Activo-brightgreen)]() [![Licencia](https://img.shields.io/badge/license-MIT-blue)]() [![Python](https://img.shields.io/badge/Python-3.10%2B-informational)]() [![Made with Jupyter](https://img.shields.io/badge/Made%20with-Jupyter-orange)]()

---

##  Tabla de Contenidos

* [Descripción](#-descripción)
* [Estructura del repositorio](#-estructura-del-repositorio)
* [Requisitos](#-requisitos)
* [Instalación](#-instalación)
* [Ejecución](#-ejecución)
* [Datos](#-datos)
* [Resultados y Métricas](#-resultados-y-métricas)
* [Curvas de Aprendizaje](#-curvas-de-aprendizaje)
* [Diagnóstico y Análisis](#-diagnóstico-y-análisis)
* [Estrategias de Mejora](#-estrategias-de-mejora)
* [Visualizaciones](#-visualizaciones)
* [Estructura del Código / Módulos](#-estructura-del-código--módulos)
* [Acceso a Documentación](#-acceso-a-documentación)
* [Conclusiones](#-conclusiones)
* [Referencias](#-referencias)
* [Licencia](#-licencia)

---

##  Descripción

Este proyecto presenta un **sistema de diagnóstico asistido por inteligencia artificial** aplicado a imágenes ecográficas de tiroides. Se evaluaron dos enfoques de clasificación:

* Una **Red Neuronal Convolucional (CNN)**.
* Un **Random Forest**.

El propósito es identificar patrones en ecografías que apoyen la **detección temprana de cáncer de tiroides** y proponer mejoras metodológicas para su uso clínico.

---

##  Estructura del repositorio

```text
.
├─ README.md
├─ Integrador30.ipynb                   # Notebook principal del proyecto
├─ CODIGO MODULAR.docx / .pdf           # Documentación modular
├─ REPORTE TECNICO.docx / .pdf          # Reporte técnico detallado
├─ VISUALIZACIONES PROFESIONALES BC.pptx # Presentación de resultados
├─ data/
│  ├─ raw/                              # Datos originales (637 imágenes)
│  ├─ processed/                        # Datos procesados
├─ reports/
│  ├─ figures/                          # Gráficas exportadas
│  └─ word_pdf/                         # Documentos generados
└─ src/                                 # Código modular (data, features, models, viz)
```

---

##  Requisitos

* Python 3.10+
* Jupyter Notebook / JupyterLab
* Librerías principales:

  * `tensorflow/keras`
  * `scikit-learn`
  * `imblearn` (SMOTE)
  * `matplotlib`, `seaborn`
  * `pandas`, `numpy`

```bash
pip install -r requirements.txt
```

---

##  Instalación

1. Clonar el repositorio.
2. Crear un entorno virtual.
3. Instalar dependencias.

---

##  Ejecución

Ejecutar el notebook principal:

```bash
jupyter notebook Integrador30.ipynb
```

---

##  Datos

* **Total:** 637 imágenes ecográficas.
* **Clases:** 377 malignas, 260 benignas.
* **Preprocesamiento:** redimensionamiento (299x299), normalización, balanceo con **SMOTE** y `class weights`.

---

##  Resultados y Métricas

* **Random Forest:** 99.22% precisión.
* **CNN:** 59.38% exactitud.
* **F1-score:** mejorado mediante SMOTE.

> El Random Forest superó ampliamente a la CNN, demostrando mejor generalización en este dataset.

---

##  Curvas de Aprendizaje

* Se generaron curvas de entrenamiento y validación.
* Evidencian **overfitting** en la CNN y estabilidad en Random Forest.

---

##  Diagnóstico y Análisis

* **Hallazgos:**

  * Random Forest > CNN en precisión y consistencia.
  * La CNN presentó **overfitting** significativo.
  * SMOTE redujo sesgo de clase.
* **Errores frecuentes:** baja capacidad de generalización de la CNN.

---

##  Estrategias de Mejora

* Incrementar dataset y aplicar **data augmentation**.
* Explorar arquitecturas CNN avanzadas (**ResNet, EfficientNet**).
* Regularización: dropout, L2, early stopping.
* Ajustar hiperparámetros y aplicar validación estratificada.
* Ensambles (RF + CNN).
* Validación externa con especialistas clínicos.

---

##  Visualizaciones

Se incluyen:

* Tracking de métricas (loss, accuracy, F1-score).
* Curvas de aprendizaje.
* Matrices de confusión.
* Comparativas con y sin SMOTE.

Todas disponibles en `reports/figures/` y `VISUALIZACIONES PROFESIONALES BC.pptx`.

---

##  Estructura del Código / Módulos

```text
src/
├─ data/              # Preprocesamiento y carga de datos
├─ features/          # Extracción de características
├─ models/            # Entrenamiento, evaluación y predicción
└─ viz/               # Visualizaciones y gráficos
```

---

##  Acceso a Documentación

Este repositorio incluye documentos clave con explicaciones y resultados:

* 📄 [Reporte Técnico – DOCX](REPORTE%20TECNICO%20.docx)
* 📄 [Reporte Técnico – PDF](REPORTE%20TECNICO%20.pdf)
* 📄 [Código Modular – DOCX](CODIGO%20MODULAR.docx)
* 📄 [Código Modular – PDF](CODIGO%20MODULAR.pdf)
* 📊 [Visualizaciones – PPTX](VISUALIZACIONES%20PROFESIONALES%20BC.pptx)

> Puedes acceder a ellos directamente desde la carpeta principal del proyecto.

---

##  Conclusiones

El sistema demostró que **Random Forest** es más confiable que una CNN básica en el diagnóstico asistido con imágenes ecográficas tiroideas. No obstante, se requiere:

* Mayor volumen y diversidad de datos.
* Arquitecturas profundas de CNN.
* Validación con expertos médicos.

El proyecto valida la **viabilidad del uso de IA como apoyo al diagnóstico clínico temprano** de cáncer de tiroides.

---

##  Referencias

1. Goodfellow, I., Bengio, Y., & Courville, A. *Deep Learning*. MIT Press, 2016.
2. Chollet, F. *Deep Learning with Python*, 2nd ed. Manning, 2021.
3. Rokach, L., & Maimon, O. *Data Mining with Decision Trees: Theory and Applications*. World Scientific, 2014.
4. Chawla, N. V., et al. “SMOTE: Synthetic Minority Over-sampling Technique.” *Journal of Artificial Intelligence Research*, 2002.

---

## Autores

Byron Piedra
Christian Garcia 
