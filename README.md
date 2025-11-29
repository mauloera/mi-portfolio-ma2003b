# Portfolio de Análisis Multivariado en Ciencia de Datos 📊

![Status](https://img.shields.io/badge/Status-Completed-success)
![Python](https://img.shields.io/badge/Python-3.13-blue)
![Course](https://img.shields.io/badge/Course-MA2003B-orange)

Este repositorio contiene la **Evaluación Final Integradora** del curso *Aplicación de Métodos Multivariados en Ciencia de Datos* (MA2003B) del Tecnológico de Monterrey.

El portafolio consolida tres casos de negocio reales resueltos mediante técnicas estadísticas avanzadas, demostrando la capacidad de traducir datos complejos en decisiones estratégicas accionables.

---

## Equipo de Trabajo (Team 4)

| Nombre | Rol Principal |
| :--- | :--- |
| **Gerardo Javier López García** | Data Engineering & Processing |
| **Emilio Guillén Ramírez** | Business Strategy & Insights |
| **Mauricio Loera Abundis** | Modeling & Visualization |

---


## Resumen Ejecutivo de Casos

A continuación se presentan los tres proyectos estratégicos desarrollados durante el curso:

| # | Caso & Cliente | Técnica Aplicada | Problema de Negocio | Hallazgo Clave | Enlace |
|:-:| :--- | :--- | :--- | :--- | :-: |
| **01** | **TechnoServe**<br>*(Satisfacción B2B)* | **Factor Analysis**<br>(EFA) | La dispersión de métricas de encuesta impedía priorizar inversiones de mejora. | Se identificaron **5 dimensiones latentes**. La **"Excelencia Técnica"** es el predictor #1 de la lealtad ($\beta=0.19$), por encima del precio. | [Ver Caso](./case-01-factor-analysis/) |
| **02** | **LendSmart**<br>*(Riesgo Crediticio)* | **Discriminant Analysis**<br>(LDA) | Alta tasa de default (28%) en cartera de préstamos personales. | El modelo LDA alcanzó un **Recall del 100%** en la detección de defaults, señalando la *Estabilidad Laboral* y el *Uso de Crédito* como las variables de corte críticas. | [Ver Caso](./case-02-discriminant-analysis/) |
| **03** | **MegaMart**<br>*(Retail)* | **Cluster Analysis**<br>(K-Means) | Estrategias de marketing genéricas con bajo ROI y alta tasa de abandono. | Se descubrieron **5 segmentos naturales**. El grupo *"High-Value Loyalists"* genera el mayor margen pero requiere programas de retención exclusivos. | [Ver Caso](./case-03-cluster-analysis/) |

---

## Síntesis Metodológica

En este portafolio hemos aplicado tres familias de técnicas multivariadas distintas para resolver problemas de diferente naturaleza. A continuación se comparan sus aplicaciones y criterios de selección:

| Característica | Factor Analysis (Caso 1) | Discriminant Analysis (Caso 2) | Cluster Analysis (Caso 3) |
| :--- | :--- | :--- | :--- |
| **Tipo de Aprendizaje** | **No Supervisado** | **Supervisado** | **No Supervisado** |
| **¿Qué hace?** | Reduce muchas variables en pocos conceptos latentes. | Predice la pertenencia a un grupo conocido. | Descubre grupos naturales desconocidos. |
| **Variable Objetivo (Y)** | No existe. Busca correlaciones internas ($X \leftrightarrow X$). | Existe y es categórica (Ej. Default: Sí/No). | No existe. Se infiere por distancia matemática. |
| **Supuestos Clave** | Multicolinealidad entre variables es necesaria (KMO > 0.6). | Normalidad multivariada y homogeneidad de varianzas. | Los datos deben ser escalables y comparables. |
| **Valor de Negocio** | Simplificación estratégica y creación de índices (KPIs). | Automatización de decisiones y gestión de riesgo. | Personalización masiva y eficiencia de marketing. |

---

## Lecciones Aprendidas

Reflexión crítica del equipo sobre el proceso de desarrollo y análisis:

1.  **La Interpretación supera a la Matemática:**
    * *Desafío:* En el Caso 3 (Clustering), las métricas matemáticas sugerían varios números de clusters posibles.
    * *Aprendizaje:* La decisión final siempre debe ser la que tenga más sentido de negocio. Un modelo perfecto que no se puede explicar o accionar es inútil. Aprendimos a "bautizar" factores y clusters con nombres de negocio reales.

2.  **Calidad de Datos > Complejidad del Modelo:**
    * *Desafío:* En el Caso 1, la presencia de valores nulos impedía el análisis factorial.
    * *Aprendizaje:* La imputación estratégica y la limpieza previa son el 80% del éxito. "Garbage in, garbage out" es una realidad absoluta en métodos multivariados.

3.  **El Poder de la Reducción:**
    * *Aprendizaje:* Tanto en Factor Analysis como en Discriminant (vía RFE), descubrimos que menos es más. Reducir 23 métricas a 5 factores (Caso 1) o filtrar variables redundantes (Caso 2) no solo simplifica el cómputo, sino que clarifica la estrategia para la dirección.

---

## Estructura del Repositorio

```text
mi-portfolio-ma2003b/
├── pyproject.toml                 # Configuración de dependencias modernas
├── README.md                      # Documentación central (Este archivo)
├── case-01-factor-analysis/       # Proyecto de Satisfacción de Clientes
│   ├── README.md                  # Resumen Ejecutivo del Caso 1
│   ├── data/                      # Datasets y Diccionarios
│   ├── notebooks/                 # Código de análisis
│   └── reports/                   # Reportes exportados (PDF)
├── case-02-discriminant-analysis/ # Proyecto de Riesgo de Crédito
│   ├── README.md                  # Resumen Ejecutivo del Caso 2
│   ├── data/
│   ├── notebooks/
│   └── reports/
└── case-03-cluster-analysis/      # Proyecto de Segmentación de Clientes
    ├── README.md                  # Resumen Ejecutivo del Caso 3
    ├── data/
    ├── notebooks/
    └── reports/
```
---

## Instalación y Reproducibilidad

Este proyecto utiliza **Python 3.13+** y gestiona sus dependencias a través de `pyproject.toml` para garantizar un entorno reproducible y moderno.

### 1. Clonar el repositorio
```bash
git clone [https://github.com/mauloera/mi-portfolio-ma2003b.git](https://github.com/mauloera/mi-portfolio-ma2003b.git)
cd mi-portfolio-ma2003b
```
### 2. Instalar dependencias

Puede instalar todas las librerías necesarias ejecutando:
```bash
pip install .
```

Alternativamente, si prefiere instalar manualmente
```bash
pip install pandas numpy matplotlib seaborn scikit-learn factor-analyzer scipy ipykernel
```

### 3. Ejecutar los análisis
Cada caso es independiente. Navegue a la carpeta de *notebooks* correspondiente y ejecute el archivo `.ipynb`.

---
*Tecnológico de Monterrey - Noviembre 2025*
