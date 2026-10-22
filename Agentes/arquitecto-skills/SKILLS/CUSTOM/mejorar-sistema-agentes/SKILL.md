---
name: mejorar-sistema-agentes
description: Superskill para actualizar contratos de la plantilla de agentes, diseñar habilidades especializadas y verificar coherencia entre prompts, índices y reglas compartidas.
---

# Mejorar sistema de agentes

Yo leo SYSTEM/PROTOCOL.md, SYSTEM/IA_TEMPLATE/, las skills de orquestación y creación, y las reglas compartidas antes de editar. No ejecuto bootstrap.

Yo identifico los contratos que cambian y sus consumidores: alta de agentes, ubicación de skills, índice y permisos de trabajo frente al aislamiento de memorias. Evito modificar contratos ajenos al encargo.

Yo creo cada superskill buscando ampliamente skills del tema en internet, leyendo las relevantes e investigando en profundidad para complementarlas; sintetizo en una sola skill si es cohesivo o en una skill índice que deriva a otras relevantes propias. Registro fuentes, aportes y límites. La habilidad resultante incluye decisiones del dominio y validación observable. Uso referencias solo cuando aportan variantes o evidencia. Busco habilidades existentes y fuentes primarias antes de añadir conocimiento técnico; registro enlaces realmente consultados y límites de investigación.

Yo mantengo AGENTS.md, CLAUDE.md y GEMINI.md sincronizados cuando cambia una regla permanente. Conservo placeholders en la plantilla y personalizo únicamente los clones. No borro habilidades ajenas a la tarea.

Yo verifico frontmatter de skills, enlaces locales, marcadores sin rellenar en agentes configurados y coherencia entre instrucciones y permisos. Reviso git diff --check y comunico resultados reales a la orquestadora.

## Síntesis y fuentes de esta habilidad

Yo consolidé las skills locales crear-superskills y orquestar-agentes para distinguir autoría, configuración y aislamiento de memorias; crear-prompts aporta contratos de tarea y criterios observables. Leí skill-creator de sistema como referencia de alcance, carga progresiva y validación, sin copiar sus ubicaciones globales.

Yo busqué skills con `npx --yes skills find 'agent skills'` y `'prompt engineering'`; leí [prompt-engineering-patterns](https://raw.githubusercontent.com/wshobson/agents/main/plugins/llm-application-dev/skills/prompt-engineering-patterns/SKILL.md), [prompt-engineering](https://raw.githubusercontent.com/giuseppe-trisciuoglio/developer-kit/main/plugins/developer-kit-ai/skills/prompt-engineering/SKILL.md) y [ai-prompt-engineering-safety-review](https://raw.githubusercontent.com/github/awesome-copilot/main/skills/ai-prompt-engineering-safety-review/SKILL.md). Integro contratos claros, pruebas con casos y límites de acceso; descarto umbrales universales y reportes extensos que no apoyan el mantenimiento solicitado.

Yo complementé con [Agent Skills: formato](https://agentskills.io/specification) y [evaluación](https://agentskills.io/skill-creation/evaluating-skills), [Google: diseño de prompts](https://ai.google.dev/gemini-api/docs/prompting-strategies) y [Anthropic: éxito antes de optimizar](https://platform.claude.com/docs/en/build-with-claude/prompt-engineering/overview), consultadas el 2026-10-22. Unifico aquí porque mantener contratos de este sistema es cohesivo; las fuentes generales no sustituyen sus reglas locales. No investigué todos los frameworks de agentes ni ejecuté los SDK de las fuentes; verifico archivos y comportamiento de un caso acotado.
