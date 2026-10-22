# PROTOCOL.md — Crear un agente

_Yo sigo la skill orquestar-agentes; este es el resumen operativo._

1. Yo reviso REGISTRY.md y reutilizo un agente adecuado o defino nombre, rol, objetivo, entradas, salida, alcance permitido y excluido.
2. Yo clono SYSTEM/IA_TEMPLATE/ en Agentes/<nombre>/ sin sobrescribir un agente existente. No ejecuto bootstrap en hijos.
3. Yo configuro CONFIG.md, PROMPT.md e IDENTITY.md; uso crear-prompts para el contrato. Conservo USER.md y memorias sin inventar datos personales.
4. Yo creo superskills especializadas antes de delegar, siguiendo crear-superskills: búsqueda amplia en internet, lectura de skills relevantes e investigación profunda complementaria. Unifico en una skill si es cohesivo; si no, creo una skill índice que deriva a otras skills relevantes del propietario. Registro fuentes, aportes y límites sin prometer exhaustividad.
5. Yo guardo las skills en Agentes/<nombre>/SKILLS/CUSTOM/ y completo SKILLS/INDEX.md con enlaces reales y disparadores. Un índice vacío no basta.
6. Yo verifico frontmatter y enlaces, correspondencia entre encargo y skill, permisos coherentes y un caso representativo de selección y resultado. Conservo placeholders en la plantilla, no en el contrato configurado.
7. Yo registro nombre, rol, carpeta, fecha y estado en REGISTRY.md y delego con arranque, encargo y aceptación. Reviso la entrega y sus comprobaciones.

Yo autorizo en CONFIG.md las rutas compartidas necesarias para el encargo; el aislamiento afecta memorias y skills propias, no impide editar entregables compartidos autorizados. No mezclo memorias ni borro skills ajenas. Yo mantengo IA_TEMPLATE/ genérica y puedo mejorarla cuando el usuario pide mantenimiento, sin personalizar sus placeholders.
