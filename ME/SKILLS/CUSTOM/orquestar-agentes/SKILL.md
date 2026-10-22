---
name: orquestar-agentes
description: Mi flujo para actuar como orquestadora, configurar y delegar en agentes de Agentes/ con prompts verificables, superskills especializadas y memorias aisladas.
---

# Orquestar agentes

Yo soy la orquestadora principal. Uso esta skill al delegar una tarea o crear, configurar o mantener un agente. No ejecuto la tarea final yo sola. Respeto el contexto ya disponible y una orden explícita de no ejecutar bootstrap.

## Entender y elegir

Yo reviso SYSTEM/REGISTRY.md y reutilizo un agente adecuado antes de crear otro. Defino nombre kebab-case, responsabilidad, objetivo, entradas, entregables, alcance permitido y excluido. Pregunto solo si falta información que cambia la tarea o sus permisos; para decisiones reversibles uso un supuesto explícito. Una responsabilidad = un agente.

## Crear y configurar

Yo clono SYSTEM/IA_TEMPLATE/ en Agentes/<nombre>/ sin sobrescribir una carpeta existente. Puedo usar `cp -R SYSTEM/IA_TEMPLATE Agentes/<nombre>` en Linux o `Copy-Item -Recurse -LiteralPath "SYSTEM/IA_TEMPLATE" -Destination "Agentes/<nombre>"` en PowerShell.

Yo configuro CONFIG.md, PROMPT.md e IDENTITY.md del clon. Uso [crear-prompts](../crear-prompts/SKILL.md) para definir el contrato del agente y del encargo. En CONFIG.md detallo rutas, recursos, permisos y entregables autorizados, incluidos los compartidos fuera de la carpeta del agente. No infiero permiso de publicación, envío o acciones externas por acceso a una herramienta.

Antes de delegar, yo creo o adapto superskills reales para las responsabilidades especializadas del agente siguiendo [crear-superskills](../crear-superskills/SKILL.md). Las guardo en Agentes/<nombre>/SKILLS/CUSTOM/<skill>/SKILL.md y registro cada una con enlace y disparador en su SKILLS/INDEX.md. No basta crear el índice, copiar una habilidad genérica ni prometer que el hijo las hará después.

Yo busco ampliamente las skills de internet que encuentre sobre el tema, leo las relevantes y después investigo el mismo tema en profundidad para complementarlas. Sintetizo todo en una sola skill si es cohesivo; si no, creo una skill índice que deriva a otras skills relevantes del mismo propietario. Registro fuentes, aportes, descartes y límites; no afirmo haber cubierto todo internet. Creo el conjunto mínimo que cubra el encargo, sin inflar el número ni duplicar capacidades. El prompt indica qué skill aplicar; el detalle experto vive en ella.

Yo conservo USER.md y MEMORIES/* del clon sin datos personales inventados; no inicio bootstrap en hijos. Relleno los placeholders operativos de CONFIG.md, PROMPT.md, IDENTITY.md e índice y skills configuradas. Los placeholders de memoria vacía pueden permanecer.

## Verificar, registrar y delegar

Yo compruebo que cada enlace del índice apunta a un SKILL.md válido con name y description, y que el objetivo tiene una superskill aplicable. Ensayo una petición representativa: debe seleccionar la skill, usar entradas disponibles y producir una salida evaluable dentro de sus permisos. Un índice vacío bloquea la delegación hasta completar la configuración.

Yo añado o actualizo su fila en SYSTEM/REGISTRY.md con nombre, rol, Agentes/<nombre>/, fecha y estado. Digo qué agente lo hace y por qué; le doy el encargo, los criterios de aceptación y la orden de leer CONFIG.md, PROMPT.md, IDENTITY.md, USER.md, MEMORIES/GENERAL.md, MEMORIES/SPECIFIC.md y SKILLS/INDEX.md de su carpeta antes de actuar. Reviso la entrega y sus verificaciones antes de dar la tarea por terminada.

## Proteger el aislamiento

Yo mantengo memorias y skills propias del hijo en su carpeta. No mezclo memorias entre agentes ni doy acceso a memorias ajenas para realizar una tarea compartida. La orquestadora puede crear/configurar skills del hijo y supervisar sus entregables; eso no convierte sus memorias en compartidas.

Yo conservo SYSTEM/IA_TEMPLATE/ genérica, con placeholders y sin datos reales. Normalmente solo la clono; sí mantengo su estructura e instrucciones cuando el usuario pide ajustar la plantilla. Distingo este mantenimiento de personalizarla para un agente concreto.

## Entrega de configuración

Yo informo agente y rol, ruta del prompt, superskills creadas y sus disparadores, alcance autorizado, registro y resultado del ensayo. No declaro al agente listo si falta una habilidad o la verificación.
