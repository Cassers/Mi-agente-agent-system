# SYSTEM/README.md

_La IA principal es orquestadora con memoria propia en `ME/` (sí se personaliza con bootstrap)._

## Estructura

```
./ME/                        <- mi memoria como orquestadora principal, sí se personaliza
./ME/SKILLS/CUSTOM/orquestar-agentes/SKILL.md  <- yo siempre soy orquestadora (skill)
./SYSTEM/
  ORCHESTRATOR.md            <- puntero a la skill
  PROTOCOL.md                <- resumen operativo
  REGISTRY.md                <- índice de agentes
  IA_TEMPLATE/               <- se clona para cada agente
    CONFIG.md
    PROMPT.md                <- prompt especializado
    IDENTITY.md
    USER.md
    MEMORIES/GENERAL.md
    MEMORIES/SPECIFIC.md
    SKILLS/INDEX.md
./Agentes/
  README.md                  <- los agentes viven aquí: ./Agentes/<nombre>/
  <nombre>/                  <- clon con prompt + skills propios
```

## Reglas

1. `ME/` es mi memoria orquestadora: sí se personaliza con bootstrap.
2. `IA_TEMPLATE/` se clona sin datos reales; su estructura e instrucciones sí se mantienen cuando el usuario lo solicita, conservando placeholders.
3. Cada `Agentes/<nombre>/` recibe un prompt verificable con `crear-prompts` y superskills creadas e indexadas antes de delegar. Yo busco ampliamente skills del tema en internet, leo las relevantes e investigo en profundidad para complementarlas; unifico en una skill o creo una skill índice que deriva a otras relevantes del propietario. Registro fuentes y límites de búsqueda.
4. Solo la orquestadora crea agentes en `Agentes/`. Memorias y skills permanecen aisladas; CONFIG.md puede autorizar lectura y edición de entregables compartidos fuera de la carpeta propia.
5. La superskill de prompts vive en `ME/SKILLS/CUSTOM/crear-prompts/SKILL.md`; el procedimiento de autoría, en `ME/SKILLS/CUSTOM/crear-superskills/SKILL.md`. Un índice vacío no configura un agente.
