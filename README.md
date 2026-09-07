# agents-modernization

Repositorio de dominio **modernization**: las unidades publicables del equipo de modernización.

| Carpeta | Qué contiene |
|---|---|
| `plugins/` | Unidades agrupadas: un plugin con varios artefactos |
| `skills/` | Skills no agrupados, cada uno su propia unidad |
| `agents/` | Agentes no agrupados |
| `commands/` | Prompts no agrupados |
| `.github/workflows/` | Los cuatro llamadores de los workflows reutilizables del estándar |
| `.github/CODEOWNERS` | Quién aprueba cada ruta |

Toda unidad publicable lleva `.claude-plugin/plugin.json` y `GOVERNANCE.json`, sea plugin o artefacto
individual. No hay `GOVERNANCE.json` en la raíz: nada se hereda por vecindad.

Las unidades se crean y modifican con el asistente de autoría del estándar, nunca a mano.

## Lo que hay aquí es una demostración, no el dominio real

`demo-sdlc-referencia` existe para probar el ciclo de vida de punta a punta, no porque el equipo de
modernización la necesite. **Su dominio y su dueño son de conveniencia**, elegidos para que la demo
funcione en esta organización:

| Dato | Valor en la demo | Qué será en BCP |
|---|---|---|
| Dominio | `modernization`, por ser el primero que el plan levanta | El dominio real al que pertenezca cada unidad |
| `owner.team` | `lt-modernization` | El equipo dueño de verdad, tomado de los equipos que BCP ya tiene |
| `owner.contact` | Un buzón de ejemplo | El buzón real del equipo, nunca el de una persona |

Nada de eso se migra tal cual. Al llevar el marco a BCP, el dueño de cada unidad lo declara el equipo
que la mantiene, y `agentic-standard/config/teams.json` mapea cada papel al equipo real.

## Estado

Hito 1 cerrado. El llamador del registro (`register.yml`) es real y aplica las reglas del estándar en
cada push a una rama de trabajo. Los otros tres siguen siendo marcadores hasta que el estándar
publique sus reutilizables: `verify.yml` en el hito 3, `tag.yml` y `publish.yml` en el hito 5.

`main` no admite fusiones todavía, y es lo previsto: su protección exige tres comprobaciones que emite
`verify.yml`. El flujo del registro ocurre en la rama de trabajo, que es donde se comprueba.
