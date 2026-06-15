# Guía de diseño del Brief y del panel — fundamentos con fuentes

> Investigación base para AdsOS. Decide **qué metodologías entran**, **cómo se estructura el brief** y **qué reglas de UX/UI/formularios** seguimos. Regla del proyecto: nada inventado; lo que no se sabe se marca como pendiente.

---

## 1. Metodologías: qué entra y qué se descarta (equipo pequeño y remoto)

| Metodología | Veredicto | Por qué |
|---|---|---|
| **Lean — 8 desperdicios** (DOWNTIME) | ✅ Entra (como rúbrica) | Usar como lente para eliminar re-captura, cambio de herramienta y esperas. El desperdicio digital se esconde en "pequeños retrasos, rework y tool-switching". |
| **Lean — "extra-processing" / sobre-procesar** | ✅ Entra (núcleo) | Registro en <1 min ⇒ el formulario pide **solo lo esencial**. Coincide con "Eliminar primero" (NN/G). |
| **Lean — "waiting" y "transportation"** | ✅ Entra | Justifica la herramienta: colas visibles matan la espera; sin re-teclear en correo/Excel matan los handoffs. |
| **Lean — one-piece flow / takt** | ⚠️ Parcial | El espíritu (lotes pequeños, feedback rápido) sirve; los mecanismos literales de manufactura no aplican a trabajo creativo. |
| **Lean — Pull / Kanban** | ✅ Entra (barato) | Jalar la siguiente tarea cuando hay capacidad; un tablero por estados lo da gratis. |
| **Muda/Mura/Muri formal** | ❌ Se descarta | Análisis formal de variabilidad/sobrecarga es overkill para equipo pequeño. |
| **Systems Thinking — anti-suboptimización** | ✅ Entra (guardrail) | No optimizar a una persona a costa del flujo total; mirar lead time de punta a punta. |
| **Systems Thinking — Single Source of Truth** | ✅ Entra (fundacional) | Una sola fuente autoritativa; múltiples fuentes generan info duplicada y contradictoria. Justifica un solo panel vs. hojas dispersas. |
| **Modelado de sistemas (stock & flow)** | ❌ Se descarta | Una vista compartida del flujo basta; diagramas elaborados no. |
| **WIP limits** | ✅ Entra (pero después) | Limitar trabajo concurrente mantiene flujo; fijar límites **tras observar**, no al lanzar. |
| **Human-Centered Design (ISO 9241-210 / IDEO)** | ✅ Entra | Diseñar desde las tareas reales del equipo e iterar con ellos. Cruce deseabilidad/factibilidad/viabilidad. |
| **KISS** | ✅ Entra | Menos features = menos carga cognitiva. Sirve directo al "claro, no saturado". |
| **Heurísticas de Nielsen (10)** | ✅ Entra (foco en #8, #1, #6, #4) | #8 minimalista (anti-saturación), #1 visibilidad de estado, #6 reconocer > recordar, #4 consistencia. |
| **Progressive disclosure / acordeones** | ✅ Entra | Mostrar lo importante primero; el detalle se expande. Reduce carga cognitiva en páginas densas. |
| **Leyes (Hick, Miller, Aesthetic-Usability)** | ✅ Entra | Hick: menos opciones = decisión más rápida. Miller: agrupar en bloques (chunking). Estético = se percibe más usable. |
| **AX / Agent Experience** | ✅ Entra (versión barata) | HTML semántico + controles reales + labels = el panel queda legible para IA a futuro, casi sin costo hoy. |

---

## 2. Estructura del Brief (fuente única de la verdad)

**Esenciales** (ordenadas):
1. Nombre del proyecto + resumen (1–2 líneas)
2. Antecedentes / contexto de negocio y marca
3. Objetivos (SMART, ligados a KPIs)
4. Audiencia objetivo (demografía + valores/necesidades)
5. Mensaje clave / propuesta única (una sola frase)
6. Tono y voz (con ejemplos, no solo adjetivos)
7. Entregables + especificaciones (formatos, tamaños)
8. Canales / distribución
9. Lineamientos de marca (**enlazar**, no incrustar: logos, hex, tipografías)
10. Timeline / hitos
11. Stakeholders / aprobaciones (quién aprueba)
12. Métricas de éxito

**Opcionales** (según caso):
- Presupuesto (esencial en relación agencia–cliente)
- Referencias / moodboard / inspiración
- Restricciones / fuera de alcance

**Buenas prácticas:** breve (1 página ideal, 1–3 máx.), lenguaje claro sin jerga, documento vivo, **centralizado** en un solo lugar. Para remoto: async-first, plantilla estandarizada, expectativas explícitas de quién decide y dónde se registra.

---

## 3. Reglas de UI / formularios (evidencia)

- **Una sola columna.** Estudio de eye-tracking (CXL): formulario en columna única se completó ~15.4 s más rápido que multicolumna. El ojo baja recto.
- **Labels arriba del campo.** Investigación de Penzo (UXmatters/LukeW): label + campo en una sola fijación ⇒ tiempos más rápidos.
- **Agrupar en secciones con etiqueta** (chunking, Miller): reduce carga cognitiva vs. muro de campos.
- **Menos campos.** Baymard: checkout promedio tiene 11.3 campos, la mayoría necesita ~8; 18% abandona por formularios largos. Expedia: quitar 1 campo = +$12M/año. Regla: justificar cada campo ("question protocol").
- **Combinar campos** cuando se pueda (ej. un solo "Nombre").
- **Acordeones / progressive disclosure** para secciones largas independientes; cuidar que suben el costo de interacción (no usar para lectura continua).
- **Style guide en UI:** swatches de color con valores + indicación de legibilidad; tipografía con muestras y uso; librería de componentes. Orden: auditar → documentar estilos → codificar componentes.
- **Defaults inteligentes** (estado, fecha, responsable pre-llenados) = lo que logra el registro en <1 min (NN/G EAS: Eliminar, Automatizar, Simplificar).

---

## 4. AX (Agent Experience) — preparar el panel para IA, casi gratis

- **AX** (acuñado por Matt Biilmann/Netlify, ene-2025): diseñar para agentes de IA como "usuario de primera clase". Cuatro pilares: **Access, Context, Tools, Orchestration**.
- **"Experience Orchestrator"** = Job Title del Año 2026 (SmartRecruiters): roles de orquestación +25% interanual. (Dato sólido.)
- **Lo accionable HOY (bajo costo, alto valor):**
  - HTML **semántico** (`<header>`, `<nav>`, `<main>`, jerarquía de encabezados).
  - Controles **reales** (`<button>`, `<form>`, `<a>`) con `aria-label`, `id`/`name`/`data-*` estables.
  - Datos estructurados / metadatos legibles.
  - Primitivas de **confianza/recuperación** si hay salidas de IA: explicar el porqué, deshacer, errores empáticos, "regresar a humano".
- **Marcado como hype / cautela:** `llms.txt` (efectividad disputada), "AX Designer" y "Vibe Designer" como títulos (nacientes / buzzword).

---

## 5. Cómo se traduce a AdsOS (decisiones)

1. **Brief = fuente única**, una pestaña por cliente, ordenada por las 12 secciones esenciales.
2. **Acordeón** con snapshot siempre visible arriba; el resto se expande (anti-saturación).
3. **Una columna, labels arriba, campos mínimos**, agrupados por sección.
4. **Lineamientos visuales como mini style-guide** (tipografía + swatches + ejemplos) y **enlace a Drive** en vez de incrustar archivos pesados.
5. **Pendientes explícitos** (⏳ Preguntar a Charlie / cliente) = visibilidad de estado + nada inventado.
6. **HTML semántico y controles reales** desde ya = listo para IA mañana.

---

### Fuentes principales
NN/G (heurísticas, carga cognitiva, progressive disclosure, acordeones, EAS, style guides vs design systems), Laws of UX (Hick, Miller, Aesthetic-Usability), IDEO / ISO 9241-210 (HCD), IxDF (KISS), Lean (8 desperdicios, pull/flow), Atlassian (Kanban, WIP), Donella Meadows (Systems Thinking), Document360/Strapi (SSOT), CXL (columna única), UXmatters/LukeW (labels), Baymard (campos), Smashing/Adam Silver (question protocol), Biilmann/Netlify (AX), SmartRecruiters (Orchestrator 2026). URLs completas en el historial de investigación de esta sesión.
