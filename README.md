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

## Estado

Esqueleto del hito 0. Los llamadores quedan como marcadores hasta que el estándar publique sus
workflows reutilizables (hito 1 y hito 3).
