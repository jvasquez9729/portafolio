# Jhon Camilo Vásquez
**Contador Público · IA aplicada a finanzas y contabilidad**
*Public Accountant · Applied AI for finance and accounting*

Soy contador público y empecé en el trabajo de todos los días: contabilidad, impuestos, cartera, conciliaciones. Ahí aprendí que los números casi nunca fallan por la teoría; fallan en el proceso: un archivo que llega torcido, un cruce que nadie revisó, un reporte que se arma a mano cada mes.

Por eso construyo las herramientas que resuelven eso. Hoy trabajo con SQL, Python y agentes de IA para automatizar lo repetitivo, validar los datos antes de confiar en ellos y dejar dashboards que la gente sí usa. Me interesa que el resultado se pueda auditar: que se sepa de dónde sale cada cifra y cómo se comprobó.

**Lo siguiente es el aprendizaje automático.** Estoy empezando a entrenar modelos de machine learning sobre datos financieros y contables (por ejemplo, detección de anomalías y clasificación de movimientos), aplicando la misma disciplina de medición que ya uso con los agentes. Todavía no tengo un proyecto terminado en esto y prefiero decirlo así.

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

**Next up is machine learning.** I'm starting to train machine learning models on financial and accounting data (for example, anomaly detection and transaction classification), applying the same measurement discipline I already use with agents. I don't have a finished project in this yet, and I'd rather say so.

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
| **Agente analista de EEFF** · *Financial statements agent* | Analiza estados financieros sin afirmar causas que no puede probar | 16 criterios de aceptación pre-registrados |
| **Agente tributario** · *Tax agent* | Borradores de renta de persona natural (Colombia) con normativa versionada | Entrega en Excel y Word |
| **Plataforma para consultora** · *Consulting-firm platform* | Estado de resultados y flujo por proyecto, con proyecciones | Sincronización automática con la hoja contable |

**Stack:** Python · FastAPI · Next.js · PostgreSQL · Claude API · MCP · n8n · Docker

## Privacidad · Privacy

El código y los datos reales pertenecen a sus dueños y **no se publican**. Las capturas y diagramas están anonimizados o usan datos ficticios.

Real code and data belong to their owners and are **not published**. Screenshots and diagrams are anonymized or use fictional data.

## Contacto · Contact

- Sitio · Site: https://jvasquez9729.github.io/portafolio/
- GitHub: https://github.com/jvasquez9729

© 2026 Jhon Camilo Vásquez. Todos los derechos reservados · All rights reserved (ver `LICENSE`).
