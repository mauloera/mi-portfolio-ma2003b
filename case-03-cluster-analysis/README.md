# Case 02: Discriminant Analysis

**Autores:** 
* Mauricio Loera Abundis
* Gerardo Javier López García
* Emilio Guillen Ramírez  

---

## 1. Contexto del Negocio

MegaMart se enfrenta a diversas complicaciones derivadas de una estrategia de mercadotecnia insuficiente y genérica que no diversifica en todos los tipos de clientes que atienden. A pesar de contar con una gran cantidad de datos transaccionales, la falta de una segmentación estructurada ha generado cuatro desafíos principales:

* **Marketing Genérico:** Las campañas no segmentadas resultan en bajas tasas de interacción y relevancia para el cliente.
* **Desperdicio de Recursos:** El presupuesto de marketing se distribuye uniformemente, asignando recursos costosos a clientes de bajo valor o riesgo, mientras se sub-invierte en los de alto valor.
* **Oportunidades Perdidas:** La incapacidad para identificar necesidades específicas impide la personalización, limitando el *up-selling* y *cross-selling*.
* **Riesgo de Abandono:** Falta de mecanismos para detectar proactivamente a los clientes en riesgo antes de que dejen de comprar.

El objetivo de este análisis es utilizar los datos de comportamiento de 3,000 clientes activos para descubrir segmentos naturales que compartan patrones de compra y navegación similares. A través de técnicas de agrupamiento no supervisado (Clustering), se lograron identificar grupos distintos que permitirán a MegaMart pasar de un marketing genérico a estrategias dirigidas y de alto impacto.

---

## 2. Perfiles de Segmentos Identificados

En el análisis técnico se identificaron **5 segmentos** distintos de clientes, validados mediante el método del codo (*Elbow Method*), el análisis de silueta (*Silhouette Score*) y su relevancia para decisiones de negocio.

### High-Value Loyalists (Cluster 0)
* **Perfil:** La élite de la base de clientes.
* **Comportamiento:** Muy alta frecuencia de transacciones mensuales, carritos grandes (~22 productos), gasto total más elevado ($6,540).
* **Interacción:** Fuertes tasas de apertura de correos, sesiones largas y alta exploración de productos.
* **Relación:** Baja recencia y alta antigüedad.
* **Valor:** Clientes estratégicos, altamente rentables y prioritarios para retención.

### New Low-Engagement Shoppers (Cluster 1)
* **Perfil:** Clientes nuevos o en fase temprana de adopción.
* **Comportamiento:** Pocas transacciones, carritos pequeños y gasto bajo.
* **Interacción:** Sesiones cortas, pocas vistas y engagement muy bajo en emails.
* **Relación:** Tenure corto y recencia moderada.
* **Valor:** Segmento que requiere estrategias de onboarding y educación del cliente.

### Big-Basket High-Spend Shoppers with Higher Returns (Cluster 2)
* **Perfil:** Compradores de alto valor por visita.
* **Comportamiento:** Carritos muy grandes y gasto total alto, aunque con frecuencia media.
* **Interacción:** Sesiones más directas, con menos vistas de producto (compras planificadas).
* **Relación:** Tenure largo, recencia promedio, pero tasas de devolución elevadas.
* **Valor:** Segmento rentable, pero con costos asociados a devoluciones.

### Engaged Mid-Spend Loyalists (Cluster 3)
* **Perfil:** Clientes leales con fuerte compromiso digital.
* **Comportamiento:** Frecuencia por encima del promedio, carritos medianos y gasto moderado.
* **Interacción:** Email open rate alto, vistas frecuentes y sesiones constantes.
* **Relación:** Alta antigüedad y bajos niveles de devolución.
* **Valor:** Segmento estable con alto potencial para estrategias de crecimiento.

### Low-Spend Browsers at Risk (Cluster 4)
* **Perfil:** Clientes que navegan mucho pero compran poco.
* **Comportamiento:** Muy pocas transacciones, carritos pequeños y gasto mínimo.
* **Interacción:** Sesiones largas, muchas vistas, pero baja conversión.
* **Relación:** Recencia alta y devoluciones elevadas.
* **Valor:** Segmento de alto riesgo que requiere activación inmediata.

---

## 3. Recomendaciones Estratégicas de Mercadotecnia

### Estrategia para High-Value Loyalists (Retención y Exclusividad)
* Crear un programa VIP con beneficios especiales.
* Ofrecer venta cruzada premium basada en su historial.
* Incentivar referencias mediante recompensas.

### Estrategia para Engaged Mid-Spend Loyalists (Desarrollo y Crecimiento)
* Implementar descuentos escalonados para aumentar el ticket.
* Desarrollar retos de frecuencia mensual.
* Personalización avanzada de correos.

### Estrategia para Big-Basket High-Spend Shoppers (Optimización y Reducción de Devoluciones)
* Refinar recomendaciones de tallas y productos.
* Mejorar el soporte post-compra.
* Analizar causas de devoluciones y ajustar surtido.

### Estrategia para Low-Spend Browsers at Risk (Activación y Conversión)
* Cupones de tiempo limitado.
* Remarketing de productos vistos.
* Resaltar políticas de devolución sencilla.

### Estrategia para New Low-Engagement Shoppers (Onboarding y Educación)
* Campañas de bienvenida con descuentos iniciales.
* Guías de compra y recomendaciones personalizadas.
* Automatizar *flows* de primera y segunda compra.

---

## 4. Impacto Esperado

La adopción de esta segmentación permitirá:
* Optimizar el ROI al dirigir recursos a segmentos de mayor valor.
* Incrementar ingresos mediante estrategias diferenciadas.
* Acelerar la rotación de inventario mediante activación del segmento de bajo gasto.
* Disminuir el abandono gracias a la detección temprana de clientes en riesgo.

---

## 5. Recomendaciones y Siguientes Pasos

* Integrar las etiquetas de la segmentación (0, 1, 2, 3, 4) en la base de datos de clientes de MegaMart para que sean visibles para los equipos de marketing y ventas.
* Lanzar campañas piloto individualizadas por segmento para evaluar las estrategias.
* Establecer un tablero de control para rastrear mensualmente cuántos clientes se mueven entre segmentos.
* Dado que el comportamiento de los clientes cambia, se recomienda volver a ejecutar el algoritmo de clustering cada 6 meses para mantener la relevancia de los segmentos.