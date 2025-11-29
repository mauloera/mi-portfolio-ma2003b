# Portfolio de Análisis Multivariado en Ciencia de Datos

![Status](https://img.shields.io/badge/Status-Completed-success)
![Python](https://img.shields.io/badge/Python-3.13-blue)
![Course](https://img.shields.io/badge/Course-MA2003B-orange)

Este repositorio contiene la **Evaluación Final Integradora** del curso *Aplicación de Métodos Multivariados en Ciencia de Datos* (MA2003B) del Tecnológico de Monterrey.

El portafolio consolida tres casos de negocio reales resueltos mediante técnicas estadísticas avanzadas, demostrando la capacidad de traducir datos complejos en decisiones estratégicas accionables.

---

## Equipo de Trabajo (Team 4)

| Nombre | Matrícula | Rol Principal |
| :--- | :--- | :--- |
| **Mauricio Loera Abundis** | A01659048 | Data Engineering & Processing |
| **Emilio Guillén Ramírez** | A01029858 | Business Strategy & Insights |
| **Gerardo Javier López García** | A01660262 | Modeling & Visualization |

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
| **Tipo de Aprendizaje** | No Supervisado | Supervisado | No Supervisado |
| **¿Qué hace?** | Reduce muchas variables en pocos conceptos latentes. | Predice la pertenencia a un grupo conocido. | Descubre grupos naturales desconocidos. |
| **Variable Objetivo (Y)** | No existe. Busca correlaciones internas ($X \leftrightarrow X$). | Existe y es categórica (Ej. Default: Sí/No). | No existe. Se infiere por distancia matemática. |
| **Supuestos Clave** | Multicolinealidad entre variables es necesaria (KMO > 0.6). | Normalidad multivariada y homogeneidad de varianzas. | Los datos deben ser escalables y comparables. |
| **Valor de Negocio** | Simplificación estratégica y creación de índices (KPIs). | Automatización de decisiones y gestión de riesgo. | Personalización masiva y eficiencia de marketing. |

---

## Lecciones Aprendidas

En el análisis de Clustering, aunque las fórmulas sugerían varias opciones de segmentación, la decisión final se basó en lo que realmente servía al negocio. Aprendimos que un modelo matemático puede ser perfecto, pero si no se puede explicar o utilizar, no tiene valor. Por eso nos enfocamos en ponerle nombres claros y útiles a cada grupo.

Aprendimos a no aferrarnos a nuestra primera idea. En el caso 1, al principio queríamos usar solo 3 factores porque sonaba más simple, pero los datos nos decían que había 5. Entendimos que el trabajo del analista es escuchar lo que dicen los números, no manipularlos para que digan lo que nosotros queremos.

Nos dimos cuenta de que lo más difícil no es programar, sino explicar los resultados para que sean entendibles para un público objetivo. Un $R^2$ de 0.60 no le dice nada a un gerente, pero decirle "esto explica el 60% de la satisfacción" es mucho más entendible para personas que no están familiarizadas. Aprendimos que nuestro trabajo real es traducir matemáticas complejas en instrucciones claras que cualquiera pueda entender.

Confirmamos que simplificar la información ayuda a tomar mejores decisiones. Tanto en el Análisis Factorial como en el Discriminante, vimos que reducir 23 métricas a solo 5 factores o eliminar variables repetidas no solo hace que el código corra más rápido, sino que facilita enormemente entender qué acciones tomar sin perderse en el ruido de los datos.

---

## Estructura del Repositorio

```text
mi-portfolio-ma2003b/
├── .gitignore                     # Archivos ignorados por git
├── .python-version                # Versión específica de Python para el entorno
├── LICENSE                        # Licencia del proyecto
├── README.md                      # Documentación central
├── pyproject.toml                 # Configuración de dependencias modernas
├── uv.lock                        # Bloqueo de versiones
├── case-01-factor-analysis/       # Proyecto de Satisfacción
│   ├── README.md                  # Resumen Ejecutivo del Caso 1
│   ├── data/                      # Datasets y Diccionarios
│   ├── notebooks/                 # Código de análisis
│   └── reports/                   # Reportes exportados
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

## Declaración de Uso de IA

De conformidad con las políticas de integridad académica del curso, declaramos que este portafolio utilizó herramientas de Inteligencia Artificial Generativa (ChatGPT y Gemini) como apoyo.

* **Propósito del uso:** Asistencia en la estructuración de scripts, depuración de errores (debugging), mejora de estilo en redacción y generación de esqueletos de documentación.
* **Validación humana:** Todo el código, análisis y conclusiones presentadas fueron revisados, validados y editados por los miembros del equipo para asegurar su precisión y alineación con el contexto del negocio. Asumimos plena responsabilidad por el contenido final.

---
*Tecnológico de Monterrey - Noviembre 2025*
