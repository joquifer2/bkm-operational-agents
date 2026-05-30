# Matriz de artefactos SDD - bkm-operational-agents

## 1. Objetivo

Definir que tipo de artefactos existen en el repositorio, para que sirven y que esta permitido en cada fase SDD.

SDD significa Spec Driven Development.

## 2. Tabla de artefactos

| Artefacto | Ubicacion | Proposito | Specification | Structure | Development |
|---|---|---|---|---|---|
| Constitucion de Copilot | .github/copilot-instructions.md | Reglas globales, limites y precedencia | Si | Si | Si |
| Instructions | .github/instructions/ | Reglas operativas por contexto y fase | Si | Si | Si |
| Prompts | .github/prompts/ | Arranque, evaluacion y guias operativas | Si | Si | Si |
| Skills | .github/skills/ | Capacidades documentales reutilizables | No obligatorio | Si, sin ejecucion compleja | Si, segun aprobacion |
| Specs de repositorio | specs/ | Contratos de alcance y arquitectura documental | Si | Si | Si |
| Specs de agente | specs/ | Definicion funcional y limites del agente | Si | Si | Si |
| Contracts | specs/contracts/ | Contratos documentales de input/output del informe | Si | Si | Si |
| Gates de gobernanza | docs/gates/ | Readiness y transicion entre fases | Si | Si | Si |
| Docs de proyecto | docs/ | Contexto, taxonomia, decisiones y matriz | Si | Si | Si |
| Tasks | docs/tasks.md | Backlog documental y técnico del repositorio | Opcional | Sí | Sí |
| Workflows | workflows/ | Flujos conceptuales no ejecutables | No obligatorio | Si, conceptual | Si, si se autoriza |
| Tools | tools/ | Contratos de tools futuras | No obligatorio | Si, contractual | Si, implementable tras aprobacion |
| Politica de memoria | memory/ | Politica y limites de memoria | No obligatorio | Si | Si |
| Tests | tests/ | Evaluaciones y criterios de calidad | No obligatorio | Opcional, documental | Si, tecnico cuando aplique |

## 2.1 Artefactos obligatorios del primer caso de uso

- spec del agente de informe mensual: specs/02_spec_agente_principal_v0_1.md
- contrato del informe: specs/contracts/01_contract_informe_indicadores_planificacion_demanda.md
- skill documental: .github/skills/informe-planificacion-demanda/SKILL.md
- prompt/comando: .github/prompts/informe-planificacion-demanda.prompt.md
- workflow conceptual: workflows/01_workflow_informe_planificacion_demanda.md
- eval documental: tests/evals/evaluar_informe_planificacion_demanda.md

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
