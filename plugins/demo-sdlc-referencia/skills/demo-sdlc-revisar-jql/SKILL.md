---
name: revisar-jql
description: Revisa una consulta JQL y señala los filtros que faltan antes de ejecutarla. Úsalo cuando alguien escriba o pegue una consulta JQL.
metadata:
  tags: jira, jql, revision
---

# Revisar una consulta JQL

## Cuándo usar esto

Cuando alguien escribe o pega una consulta JQL y quiere saber si va a devolver lo que espera antes de
ejecutarla contra un proyecto grande.

## Qué comprobar

1. Que la consulta acota el proyecto. Sin `project = ...` recorre todo el Jira y tarda.
2. Que acota el tiempo cuando pregunta por actividad, con `updated >= ...` o `created >= ...`.
3. Que el orden es explícito con `ORDER BY`, porque sin él el orden no está garantizado.
4. Que los estados que nombra existen en el flujo del proyecto y no son de otro.

## Qué devolver

La consulta corregida, y debajo una línea por cada filtro que faltaba, diciendo qué habría pasado sin
él. Si la consulta ya está bien, dilo y no la reescribas.
