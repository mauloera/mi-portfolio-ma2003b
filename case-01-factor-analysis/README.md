# Case 01: Factor Analysis

**Autores:** 
* Emilio Guillén Ramírez
* Mauricio Loera Abundis 
* Gerardo Javier López García  

---

## Contexto del Negocio
TechnoServe enfrenta el desafío de priorizar sus inversiones operativas basándose en múltiples métricas de satisfacción dispersas. El objetivo de este análisis fue identificar las dimensiones latentes que estructuran la experiencia del cliente y cuantificar su impacto real en la lealtad y satisfacción general.

## Metodología y Validación del Modelo
Se aplicó un Análisis Factorial Exploratorio (EFA) con rotación Promax. La evidencia estadística (Criterio de Kaiser, autovalores > 1) reveló una estructura robusta de **5 factores**.

* **Varianza Explicada:** 61.8% (Captura la mayoría de la información de los datos).
* **Poder Predictivo ($R^2$):** 0.60 (El modelo explica el 60% de la satisfacción).

## Identificación de Factores e Impacto
El modelo de regresión lineal permitió rankear los factores según su coeficiente de impacto ($\beta$) en la satisfacción general.

| Factor | Dimensión de Negocio | Impacto ($\beta$) | Prioridad |
| :--- | :--- | :---: | :--- |
| F1 (`F_tech`) | Excelencia Técnica | 0.19 | Alta |
| F2 (`F_val`) | Valor y Transparencia | 0.17 | Alta |
| F3 (`F_pro`) | Gestión de Proyectos | 0.16 | Media |
| F4 (`F_sup`) | Soporte y Habilitación | 0.15 | Media |
| F5 (`F_rel`) | Relación y Confianza | 0.15 | Media |

## Interpretación de Factores

### Factor 1: Excelencia Técnica (`F_tech`)
Agrupa variables como *Innovation Solutions*, *Problem Solving*, *System Integration*, *Technical Documentation* y *Technical Expertise*. Representa la capacidad nuclear de la empresa. Al ser el driver #1, indica que los clientes valoran la funcionalidad del producto por encima del trato humano.

### Factor 2: Valor y Transparencia (`F_val`)
Agrupa *Billing Accuracy*, *ROI Demonstration*, *Cost Transparency*, *Competitive Pricing* y *Value for Money*. Refleja la percepción de justicia económica. Errores administrativos aquí generan detractores inmediatos.

### Factor 3: Gestión de Proyectos (`F_pro`)
Agrupa *Project Management*, *Timeline Adherence*, *Quality Deliverables*, *Budget Control* y *Change Management*. Refleja la eficiencia operativa y el cumplimiento de promesas de entrega.

### Factor 4: Soporte y Habilitación (`F_sup`)
Agrupa *Training Quality*, *Support Responsiveness* y *Documentation Help*. Refleja el acompañamiento post-venta y empoderamiento del usuario.

### Factor 5: Relación y Confianza (`F_rel`)
Agrupa *Trust Reliability*, *Executive Access*, *Long Term Partnership*, *Account Manager Responsive* y *Communication Clarity*. Representa la calidad humana y estratégica del vínculo con el cliente.

## Recomendaciones de Negocio e Impacto Esperado

A continuación, se presentan las iniciativas estratégicas derivadas del análisis, priorizadas por su capacidad de mover la satisfacción general.

### Blindaje del Core Técnico (Prioridad: Alta)
Dado que la Excelencia Técnica es el predictor más fuerte ($\beta=0.19$), la calidad del producto no es negociable.
* **Recomendación:** Establecer células de innovación dedicadas y reforzar las pruebas automatizadas de integración de sistemas (*System Integration*).
* **Impacto Esperado:** Incremento directo en la satisfacción general y reducción de la tasa de abandono (Churn) por fallas técnicas críticas.

### Auditoría de Procesos de Facturación (Prioridad: Alta)
El factor de Valor y Transparencia es el segundo más influyente ($\beta=0.17$). La fricción administrativa destruye valor rápidamente.
* **Recomendación:** Implementar un sistema de "Facturación Transparente" con alertas preventivas de presupuesto y auditoría de precisión en *Billing Accuracy*.
* **Impacto Esperado:** Reducción drástica de detractores (NPS) causados por disputas administrativas y mejora en la percepción de ROI del cliente.

### Estandarización de la PMO (Gestión de Proyectos)
Para el factor 3, la variabilidad en la entrega es el enemigo.
* **Recomendación:** Crear una Oficina de Gestión de Proyectos (PMO) para asegurar que la adherencia a cronogramas (*timeline adherence*) sea un estándar garantizado y no dependa del gestor individual.
* **Impacto Esperado:** Mayor predictibilidad en las entregas y mejora en la métrica de *Budget Control*.

### Transformación del Modelo de Soporte (Habilitación)
Para mejorar el factor 4, se debe pasar de reactivo a proactivo.
* **Recomendación:** Invertir en una Academia de Usuarios con documentación moderna y video-tutoriales (*Training Quality*) para empoderar al cliente.
* **Impacto Esperado:** Reducción de tickets de soporte de nivel 1 y aumento de la autonomía del cliente.