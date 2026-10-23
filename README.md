# Jhon Camilo Vásquez
**Contador Público · IA aplicada a finanzas y contabilidad**
*Public Accountant · Applied AI for finance and accounting*

Soy contador público y empecé en el trabajo de todos los días: contabilidad, impuestos, cartera, conciliaciones. Ahí aprendí que los números casi nunca fallan por la teoría; fallan en el proceso: un archivo que llega torcido, un cruce que nadie revisó, un reporte que se arma a mano cada mes.

Por eso construyo las herramientas que resuelven eso. Hoy trabajo con SQL, Python y agentes de IA para automatizar lo repetitivo, validar los datos antes de confiar en ellos y dejar dashboards que la gente sí usa. Me interesa que el resultado se pueda auditar: que se sepa de dónde sale cada cifra y cómo se comprobó.

**Mi siguiente frente es el aprendizaje automático.** Estoy desarrollando modelos de machine learning para datos financieros y contables, con la misma disciplina de medición que ya aplico a los agentes: criterios fijados de antemano, datos de verdad conocida y evaluación honesta. Los modelos en los que trabajo, y para qué sirve cada uno (estado: *planeado*, *en curso* o *entrenado con resultados*; hoy todos están en *planeado*, empezando por la detección de anomalías):

- **Regresión lineal y regularizada (Ridge, Lasso):** explicar y proyectar rubros (ingresos, costos, recaudo) a partir de sus drivers, y medir cuánto pesa cada uno en el margen.
- **Regresión logística:** estimar la probabilidad de que una factura o una entidad pague tarde o caiga en mora, para priorizar el cobro.
- **Árboles y *gradient boosting* (Random Forest, XGBoost):** predecir recaudo y mora con datos tabulares, y clasificar movimientos contables en su cuenta del plan de cuentas.
- **Detección de anomalías (Isolation Forest, puntajes robustos):** encontrar asientos, facturas o conciliaciones atípicos: duplicados, montos fuera de patrón, pares +/− que no deberían estar.
- **Series de tiempo (ETS, ARIMA):** proyectar flujo de caja y ventas con su estacionalidad.
- **Agrupamiento (K-means):** segmentar clientes o EPS por comportamiento de pago.
- **Clasificación de texto (TF-IDF + modelo lineal):** categorizar descripciones de movimientos y glosas.

## Cómo trabajo

No construyo nada sin pasar por este recorrido:

1. **Plan escrito** con criterios de aceptación fijados *antes* de probar, para que nadie (yo incluido) pueda ajustar la vara después de ver los resultados.
2. **Datos de verdad conocida:** un conjunto etiquetado, con casos difíciles y ambiguos a propósito.
3. **Pruebas repetidas** (más de 100 corridas) midiendo exactitud, estabilidad entre repeticiones, calibración y costo.
4. **Análisis de cada error:** se clasifica si falló el prompt, el criterio, el dato o si el caso es genuinamente ambiguo, y se itera.
5. **Informe de calidad.** Si no cumple los criterios, no se construye: se itera o se aborta con informe.
6. **Revisión antes de producción:** los cambios importantes pasan por tres revisores independientes (seguridad, rendimiento y mantenibilidad) y un veredicto combinado; si falta un informe, se bloquea.

En la práctica: el cobro de cartera coincide al peso con el cálculo manual en 62 de 62 entidades, y el agente analista de estados financieros se mide contra 16 criterios de aceptación pre-registrados.

---

I'm a public accountant, and I started in the day-to-day work: accounting, taxes, receivables, reconciliations. That's where I learned that numbers rarely fail because of theory; they fail in the process: a file that arrives wrong, a match nobody checked, a report assembled by hand every month.

So I build the tools that fix that. Today I work with SQL, Python and AI agents to automate the repetitive parts, validate data before trusting it, and ship dashboards people actually use. I care about results that can be audited: knowing where every figure comes from and how it was checked.

**My next front is machine learning.** I'm developing machine learning models for financial and accounting data, with the same measurement discipline I already apply to agents: criteria set in advance, known-truth data and honest evaluation. The models I'm working on, and what each is for (status: *planned*, *in progress* or *trained with results*; today all are *planned*, starting with anomaly detection):

- **Linear and regularized regression (Ridge, Lasso):** explain and forecast line items (revenue, costs, collections) from their drivers, and measure how much each one weighs on margin.
- **Logistic regression:** estimate the probability that an invoice or an entity pays late or defaults, to prioritize collection.
- **Trees and gradient boosting (Random Forest, XGBoost):** predict collections and delinquency from tabular data, and classify accounting entries into their chart-of-accounts code.
- **Anomaly detection (Isolation Forest, robust scores):** find unusual entries, invoices or reconciliations: duplicates, out-of-pattern amounts, +/− pairs that shouldn't be there.
- **Time series (ETS, ARIMA):** forecast cash flow and sales with seasonality.
- **Clustering (K-means):** segment customers or insurers by payment behavior.
- **Text classification (TF-IDF + linear model):** categorize transaction descriptions and audit notes.

## How I work

Nothing gets built without going through this path:

1. **Written plan** with acceptance criteria set *before* testing, so nobody (me included) can move the bar after seeing results.
2. **Known-truth data:** a labeled set with deliberately hard and ambiguous cases.
3. **Repeated runs** (100+) measuring accuracy, stability across repetitions, calibration and cost.
4. **Error analysis:** every failure is classified as prompt, criterion, data, or a genuinely ambiguous case, then I iterate.
5. **QA report.** If it doesn't meet the criteria, it isn't built: I iterate or abort with a report.
6. **Review before production:** important changes go through three independent reviewers (security, performance, maintainability) and a combined verdict; if a report is missing, it's blocked.

In practice: receivables collection matches the manual calculation to the peso in 62 of 62 entities, and the financial statements analyst agent is measured against 16 pre-registered acceptance criteria.

## Casos de estudio · Case studies

| | Qué resuelve · What it solves | Evidencia · Evidence |
|---|---|---|
| **ContIA** | SaaS multi-tenant de reportes financieros y KPIs para pymes | 9 KPIs en producción (DuPont y eficiencia); aislamiento por empresa probado con pruebas de ataque |
| **Cobro de cartera (salud)** · *Healthcare receivables* | Cobro a decenas de EPS desde un reporte de 116.524 filas | 62/62 entidades iguales al peso frente al cálculo manual |
| **Agentes de análisis financiero** · *Financial analysis agents* | Extraen, validan y analizan estados financieros; otros agentes auditan el resultado | 16 criterios de aceptación pre-registrados en el agente analista |
| **Agente tributario** · *Tax agent* | Borradores de renta de persona natural (Colombia) con normativa versionada | Entrega en Excel y Word |
| **Plataforma para consultora** · *Consulting-firm platform* | Estado de resultados y flujo por proyecto, con proyecciones | Sincronización automática con la hoja contable |

**Stack:** Python · FastAPI · Next.js · PostgreSQL · Claude API · MCP · n8n · Docker

## Agentes que he construido · Agents I've built

No es un solo agente: es un equipo, cada uno con un rol acotado y memoria propia.

**Análisis financiero**
- **Analista de estados financieros:** lee imágenes, PDF y Excel, verifica que el balance cuadre, calcula márgenes y razones, arma el puente de márgenes y detecta anomalías. Nunca afirma una causa que no pueda probar: dice qué se movió, cuánto y qué documento lo resolvería. Entrega en Excel y Word.
- **Pipeline de tres capas para documentos financieros:** extracción del contenido, razonamiento con IA para identificar las cifras y *compuertas* en Python que validan los números antes de aceptarlos.
- **Agente de análisis sobre plan de cuentas (PUC):** extrae y analiza estados financieros de PDF para empresas colombianas.
- **Controller financiero (FP&A):** presupuestos, proyecciones, análisis de variaciones y flujo de caja.

**Tributario**
- **Agente de renta de persona natural (Colombia):** calcula y prepara borradores con normativa versionada y vigilancia web de cambios.

**Auditoría y control**
- **Tres revisores independientes** (seguridad, rendimiento y mantenibilidad) que auditan cada cambio importante, y un **orquestador** que emite un veredicto combinado: si falta un informe, bloquea.
- **Revisor de seguridad fintech:** aislamiento multi-tenant, cifrado, manejo de secretos y cumplimiento de Habeas Data (Ley 1581 de 2012).

*Multiple agents, each with a narrow role and its own memory.* **Financial analysis:** a statements analyst that never asserts a cause it can't prove; a three-layer pipeline (extraction, AI reasoning, Python validation gates); a chart-of-accounts analyst for Colombian companies; and an FP&A controller. **Tax:** a personal income tax agent with versioned regulations and web monitoring. **Audit and control:** three independent reviewers (security, performance, maintainability) plus an orchestrator that issues a fail-closed verdict, and a fintech security reviewer covering multi-tenancy, encryption, secrets and Colombian data-protection law.

## Privacidad · Privacy

El código y los datos reales pertenecen a sus dueños y **no se publican**. Las capturas y diagramas están anonimizados o usan datos ficticios.

Real code and data belong to their owners and are **not published**. Screenshots and diagrams are anonymized or use fictional data.

## Contacto · Contact

- Sitio · Site: https://jvasquez9729.github.io/portafolio/
- GitHub: https://github.com/jvasquez9729

© 2026 Jhon Camilo Vásquez. Todos los derechos reservados · All rights reserved (ver `LICENSE`).
