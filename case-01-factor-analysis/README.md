# Case 01: Customer Satisfaction Drivers Analysis

## 1. Contexto del Negocio
**Cliente:** TechnoServe Solutions (Empresa B2B de Tecnología)

**Problema de Negocio:**
La empresa recopila trimestralmente una encuesta de satisfacción con 23 variables métricas. La dirección enfrenta dificultades para priorizar acciones estratégicas debido a la dispersión de estos indicadores.

**Objetivo:**
Identificar las dimensiones latentes (factores) que estructuran la experiencia del cliente y determinar cuáles tienen mayor impacto en la satisfacción general y la lealtad.

---

## 2. Metodología
Se aplicó **Análisis Factorial** para reducir la dimensionalidad de los datos.

* **Método de Extracción:** Ejes Principales (MinRes).
* **Rotación:** **Promax (Oblicua)**. Se seleccionó una rotación oblicua asumiendo que las dimensiones de satisfacción (ej. técnica y relacional) están correlacionadas entre sí, lo cual se confirmó en el análisis ($r \approx 0.4 - 0.6$).
* **Criterio de Retención:** **Criterio de Kaiser**. El análisis de *Eigenvalues* mostró claramente 5 factores con valor > 1.0, lo que llevó a seleccionar una estructura de **5 dimensiones** (explicando el **61.8% de la varianza**), superior a modelos más simples de 3 factores.

---

## 3. Datos
* **Muestra:** 3,400 respuestas de clientes corporativos.
* **Variables:** 23 métricas de percepción (escala 1-5) + métricas de resultado (Satisfacción, NPS, Renovación).
* **Integridad:** Se realizó imputación de valores nulos utilizando la media para mantener la consistencia de la matriz factorial.

---

## 4. Hallazgos Principales
El análisis reveló 5 pilares estratégicos que componen la experiencia del cliente:

### Estructura Factorial (5 Dimensiones)
1.  **Excelencia Técnica (Factor 1 `F_tech`):**
    * Agrupa: `innovation_solutions`, `problem_solving`, `system_integration`, `technical_documentation`, `technical_expertise`.
    * *Significado:* La capacidad de la empresa para entregar soluciones funcionales y avanzadas.
2.  **Gestión de Proyectos (Factor 2 `F_pro`):**
    * Agrupa: `project_management`, `timeline_adherence`, `quality_deliverables`, `budget_control`, `change_-management`.
    * *Significado:* La eficiencia operativa y el cumplimiento de promesas de entrega.
3.  **Relación y Confianza (Factor 3 `F_rel`):**
    * Agrupa: `trust_reliability`, `executive_access`,`long_term_partnership`, `account_manager_responsive`, `communication_clarity`.
    * *Significado:* La calidad humana y estratégica del vínculo con el cliente.
4.  **Valor y Transparencia (Factor 4 `F_val`):**
    * Agrupa: `billing_accuracy`, `roi_demonstration`, `cost_transparency`, `competitive_pricing`, `value_for_money`.
    * *Significado:* La percepción de justicia económica y claridad administrativa.
5.  **Soporte y Habilitación (Factor 5 `F_sup`):**
    * Agrupa: `training_quality`, `support_responsiveness`, `documentation_help`.
    * *Significado:* El acompañamiento post-venta y empoderamiento del usuario.

### Impacto en el Negocio (Modelo Predictivo)
Un modelo de regresión lineal ($R^2 = 0.60$) determinó el peso de cada factor en la satisfacción general:

| Factor | Impacto ($\beta$) | Prioridad |
| :--- | :---: | :--- |
| **Excelencia Técnica** | **0.19** | Alta |
| **Valor y Transparencia** | **0.17** | Alta |
| **Gestión de Proyectos** | 0.16 | Media |
| **Soporte y Habilitación** | 0.15 | Media |
| **Relación y Confianza** | 0.15 | Media |

> *Insight:* Aunque todas las dimensiones importan, la **solidez técnica** y la **percepción de valor** son los diferenciadores más críticos.

---

## 5. Recomendaciones de Negocio

1.  **Inversión Prioritaria en QA e Innovación (Técnica):**
    * Al ser el driver #1, se debe asegurar que el producto funcione impecablemente. Asignar recursos a *System Integration* e *Innovation*.

2.  **Revisión de Procesos de Facturación (Valor):**
    * El factor "Valor y Transparencia" es el segundo más importante. Errores en `billing_accuracy` o falta de `cost_transparency` dañan desproporcionadamente la satisfacción. Se recomienda auditar el proceso de facturación.

3.  **Estandarización de la Gestión de Proyectos:**
    * Dado el peso de la adherencia a cronogramas (`timeline_adherence`), se sugiere implementar una PMO (Oficina de Gestión de Proyectos) para estandarizar entregas.

---

## Instrucciones de Reproducción
1.  Instalar dependencias:
2.  Ejecutar el notebook: `notebooks/factor_analysis.ipynb`