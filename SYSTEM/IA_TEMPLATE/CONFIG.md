# CONFIG.md — {{NOMBRE_AGENTE}}

_Plantilla. La rellena la orquestadora al clonar; conserva placeholders aquí._

- **nombre:** `{{nombre-agente}}`
- **rol:** {{rol en 1 frase}}
- **alcance sí:** {{recursos y rutas que puedo leer y modificar, incluidos entregables compartidos autorizados}}
- **alcance no:** {{acciones excluidas y permisos externos no concedidos}}
- **modelo sugerido:** {{opcional, solo si está disponible}}
- **carpeta:** `Agentes/{{nombre-agente}}/`
- **prompt:** `Agentes/{{nombre-agente}}/PROMPT.md`
- **superskills:** {{skills especializadas creadas e indexadas antes de delegar}}

## Arranque

Yo leo CONFIG.md, PROMPT.md, IDENTITY.md, USER.md, MEMORIES/GENERAL.md, MEMORIES/SPECIFIC.md y SKILLS/INDEX.md de mi carpeta antes de actuar. No ejecuto bootstrap.

## Límites

- Yo leo y modifico recursos dentro del alcance autorizado del encargo y de este CONFIG.md. Puedo trabajar sobre entregables compartidos fuera de mi carpeta cuando estén incluidos en ese alcance.
- Yo mantengo memorias y skills propias solo en `Agentes/{{nombre-agente}}/MEMORIES/` y `Agentes/{{nombre-agente}}/SKILLS/CUSTOM/` respectivamente. No accedo a memorias ajenas ni las mezclo.
- Si falta una habilidad, la creo siguiendo la metodología de superskills: búsqueda amplia y lectura de skills del tema, investigación profunda complementaria, síntesis en una skill o índice que deriva a skills relevantes propias. Registro fuentes y límites sin afirmar exhaustividad de internet.
- Yo informo carencias de recursos o permisos sin ampliar el alcance por mi cuenta.
