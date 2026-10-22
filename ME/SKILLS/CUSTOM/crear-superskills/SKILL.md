---
name: crear-superskills
description: Mi flujo para crear superskills mediante búsqueda y lectura de skills e investigación profunda. Yo la uso cuando enfrento una actividad nueva sin skill, quiero consolidar conocimiento, o me piden crear o mejorar una skill. Busco skills relacionadas, investigo a fondo con info reciente, creo una sola skill o skill hub, retiro solo temporales propios y guardo en la carpeta de skills de su propietario.
---

# Crear superskills

## Definición del usuario

> busques todas las skills por internet que encuentres de un tema, luego hagas una investigacion profunda sobre ese mismo tema para complementarlo. Si se puede se unificara todo en una sola Skill sino se creara una skill index, que derivara a otras relevantes.

## Qué entiendo por superskill

Yo busco ampliamente las skills de internet que encuentre sobre el tema, leo las relevantes y después investigo el mismo tema en profundidad para complementarlas. Sintetizo todo en una sola skill si es cohesivo; si no, creo una skill índice que deriva a otras skills relevantes del mismo propietario. Registro fuentes, aportes, descartes y límites; no afirmo haber cubierto todo internet.

Yo creo skills para no repetir trabajo y para no ocupar mi contexto con cosas obvias. Solo guardo lo que realmente necesito y en un solo lugar.

Mi regla: cada vez que voy a hacer algo, lo hago con una skill, sin importar lo que sea. Si no tengo skill, la creo primero y luego la uso. Así documento y aprendo de cada cosa que hago.

Yo uso esta skill cuando:
- Me enfrento a una actividad nueva de la cual no tengo una skill
- Aunque ya sepa resolverla, igual la documento como skill
- Me piden crear, consolidar o limpiar skills

Yo no uso el flujo original de `skill-creator` de SKILLS.SH para el proceso. Solo lo consulto como referencia de formato (qué lleva un SKILL.md, qué son scripts, references, assets).

## Mi flujo obligatorio

Yo sigo estos 5 pasos en orden, sin saltarme ninguno. Si una fuente o herramienta no está disponible, uso una alternativa y declaro el límite; no invento investigación.

### Paso 1 - Busco todas las skills relacionadas que encuentro

Yo primero busco, nunca creo a ciegas:
1. Identifico propietario y reviso su índice y skills: `ME/SKILLS/` para la orquestadora o `Agentes/<nombre>/SKILLS/` para el hijo configurado. No inspecciono skills ajenas sin autorización.
2. Uso mi skill `find-skills`: ejecuto `npx skills find [query]` con varias queries (término principal, sinónimos, categoría)
3. Reviso https://skills.sh/ si necesito más contexto
4. Abro y leo el contenido de las skills relevantes, no solo nombres o resúmenes. Registro nombre, URL, aportes, solapamientos y carencias. Distingo resultados encontrados de contenido realmente leído.
5. Amplío términos, repositorios y catálogos hasta cubrir las facetas del encargo; explico qué fuentes no pude leer y qué límites tuvo la búsqueda. No prometo exhaustividad de todo internet.

Si ya existe una skill que cubre el tema, no creo una duplicada. La mejoro o la uso como base.

### Paso 2 - Investigo de forma profunda y reciente

Yo uso `investigar-profundo` si está disponible para mi propietario; en otro caso aplico aquí el mismo objetivo de contrastar fuentes primarias, errores, alternativas y límites sin depender de skills ajenas. Yo investigo el tema a fondo antes de escribir:
1. Busco documentación oficial y guías actuales (uso el año actual, 2026)
2. Busco recomendaciones, consejos, errores comunes y buenas prácticas recientes
3. Comparo lo que dicen las skills leídas vs lo que dice la documentación actual; registro coincidencias, conflictos, aportes y descartes con URL y fecha consultada.
4. Me quedo solo con lo no-obvio y lo que justifica su costo en tokens: yo ya soy capaz, no necesito explicaciones básicas

Yo no copio todo. Yo sintetizo. Guardo evidencia proporcionada de consultas, skills leídas, aportes y límites en la skill final o en una referencia enlazada; no copio repositorios enteros ni confundo nombres encontrados con contenido consultado.

### Paso 3 - Creo una sola skill, o una skill hub

Con toda la información, yo decido un solo formato:

- **Una sola skill**: si el tema es cohesivo y cabe en un `SKILL.md` de menos de 500 líneas. Todo va ahí.
- **Skill hub**: si el tema es amplio o tiene variantes. Creo un `SKILL.md` índice corto que redirige:
  - a otras skills relevantes del mismo propietario, creadas o adaptadas cuando haga falta, con enlace y criterio de selección.
  - Puedo añadir `references/*.md` para evidencia o detalle, pero no sustituyen las skills derivadas cuando elijo una skill índice.

Estructura que yo creo:
```
<carpeta-skills-del-propietario>/CUSTOM/<nombre-skill>/
├── SKILL.md (obligatorio, en primera persona, español, conciso)
├── references/ (opcional, solo si SKILL.md supera ~200 líneas o hay variantes)
└── scripts/ (opcional, solo si repito el mismo código o necesito determinismo)
```

Yo añado recursos solo si apoyan el trabajo. Yo no creo `README.md`, `CHANGELOG.md`, `INSTALLATION_GUIDE.md` ni archivos auxiliares. Solo lo esencial para hacer el trabajo.

Yo escribo el `SKILL.md` con:
- frontmatter con `name` y `description` claros (qué hace + cuándo usarla)
- instrucciones en primera persona, en infinitivo/imperativo conciso
- ejemplos cortos, no explicaciones largas

### Paso 4 - Retiro solo mis temporales

Yo retiro solo los temporales y borradores que creé para esta tarea. Antes de eliminar una skill existente, reviso sus referencias y el alcance autorizado; no borro habilidades ajenas ni limpio toda la carpeta. Si consolido con autorización, actualizo sus consumidores y conservo las capacidades necesarias.

Mi regla: una responsabilidad = una skill. Si ya hay una adecuada, la uso o la mejoro sin duplicarla.

### Paso 5 - Guardo e indexo por propietario

Yo guardo skills de la orquestadora en `ME/SKILLS/CUSTOM/<nombre-skill>/SKILL.md` y las de un hijo en `Agentes/<nombre>/SKILLS/CUSTOM/<nombre-skill>/SKILL.md`. La orquestadora puede configurar las del hijo; el hijo solo crea o mejora las suyas. No instalo globalmente ni duplico la misma habilidad en carpetas de herramientas.

Yo actualizo el SKILLS/INDEX.md del propietario con enlace y disparador; compruebo frontmatter, enlaces y un caso de uso observable. Al montar un subagente dejo sus superskills creadas e indexadas antes de delegar: un índice vacío no cuenta como configuración. Una superskill resulta de la búsqueda de skills, su lectura y la investigación profunda complementaria descritas arriba; verifico además su utilidad con el caso de uso.

## Evidencia de este método

Yo consolidé el flujo local de crear-skills, las reglas de orquestar-agentes y la definición explícita del usuario; contrasté formato y carga progresiva con [Agent Skills](https://agentskills.io/specification) y casos de uso con [su guía de evaluación](https://agentskills.io/skill-creation/evaluating-skills), consultadas el 2026-10-22. El caso crear-prompts registra la búsqueda de skills y síntesis con investigación primaria aplicada. Esta skill define el método; no sustituye la investigación temática al crear cada superskill.

## Ejemplo de decisión

- Tema "revisar PRs en este repo" → una sola skill `ME/SKILLS/CUSTOM/revisar-prs/SKILL.md`
- Tema "desarrollo frontend" (react, testing, deploy, docs) → skill hub `ME/SKILLS/CUSTOM/frontend/SKILL.md` que deriva a skills CUSTOM de React, pruebas y despliegue del mismo propietario, con criterios para elegir cada una; retiro solo mis temporales.
