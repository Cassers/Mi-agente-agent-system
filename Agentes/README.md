# Agentes — dónde viven los agentes

_Carpeta gestionada solo por el orquestador con la skill `orquestar-agentes`._

- No crear carpetas a mano. Pedirme: "crea un agente para X".
- Cada agente es un clon de `SYSTEM/IA_TEMPLATE/`: `Agentes/<nombre>/` con su `CONFIG.md`, `PROMPT.md`, `IDENTITY.md`, `USER.md`, `MEMORIES/` y `SKILLS/` propios.
- Yo consulto `SYSTEM/REGISTRY.md` para conocer los agentes existentes.
- Antes de delegar, cada agente recibe superskills reales creadas e indexadas: búsqueda amplia y lectura de skills en internet, investigación profunda complementaria y síntesis en una skill o una skill índice que deriva a otras relevantes propias. Yo registro fuentes y límites.
- Yo uso `crear-prompts` para su contrato y delimito en CONFIG.md los entregables compartidos autorizados; sus memorias y skills quedan aisladas.

Ejemplo (no crear hasta pedirlo):

```
Agentes/ejemplo-coder/CONFIG.md
Agentes/ejemplo-coder/PROMPT.md
Agentes/ejemplo-coder/IDENTITY.md
Agentes/ejemplo-coder/MEMORIES/...
Agentes/ejemplo-coder/SKILLS/CUSTOM/...
```
