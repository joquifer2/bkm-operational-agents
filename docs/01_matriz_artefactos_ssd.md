# Matriz de artefactos SSD - bkm-operational-agents

## 1. Objetivo

Definir que tipo de artefactos existen en el repositorio, para que sirven y que esta permitido en cada fase SSD.

## 2. Tabla de artefactos

| Artefacto | Ubicacion | Proposito | Specification | Structure | Development |
|---|---|---|---|---|---|
| Constitucion de Copilot | .github/copilot-instructions.md | Reglas globales, limites y precedencia | Si | Si | Si |
| Instructions | .github/instructions/ | Reglas operativas por contexto y fase | Si | Si | Si |
| Prompts | .github/prompts/ | Arranque, evaluacion y guias operativas | Si | Si | Si |
| Skills | .github/skills/ | Capacidades documentales reutilizables | No obligatorio | Si, sin ejecucion compleja | Si, segun aprobacion |
| Specs de repositorio | specs/ | Contratos de alcance y arquitectura documental | Si | Si | Si |
| Specs de agente | specs/ | Definicion funcional y limites del agente | Si | Si | Si |
| Gates de gobernanza | docs/gates/ | Readiness y transicion entre fases | Si | Si | Si |
| Docs de proyecto | docs/ | Contexto, taxonomia, decisiones y matriz | Si | Si | Si |
| Workflows | workflows/ | Flujos conceptuales no ejecutables | No obligatorio | Si, conceptual | Si, si se autoriza |
| Tools | tools/ | Contratos de tools futuras | No obligatorio | Si, contractual | Si, implementable tras aprobacion |
| Politica de memoria | memory/ | Politica y limites de memoria | No obligatorio | Si | Si |
| Tests | tests/ | Evaluaciones y criterios de calidad | No obligatorio | Opcional, documental | Si, tecnico cuando aplique |

## 3. Reglas transversales

- bkm_procesos es siempre source of truth funcional.
- bkm-operational-agents no duplica SOPs, reglas ni dashboards.
- Ningun artefacto de menor precedencia contradice a uno de mayor precedencia.

## 4. Prohibiciones vigentes en esta iteracion

- No elegir framework.
- No definir runtime.
- No crear arquitectura multiagente.
- No crear tools reales conectadas.
- No crear workflows ejecutables.
- No crear implementacion tecnica de agentes.

## 5. Criterio de calidad de la matriz

La matriz es valida cuando:

- cubre los artefactos minimos del repo;
- distingue con claridad permitido/no permitido por fase;
- mantiene coherencia con .github/copilot-instructions.md y specs/;
- evita decisiones tecnicas irreversibles en Specification / Structure.
