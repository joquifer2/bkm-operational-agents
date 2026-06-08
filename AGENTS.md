# AGENTS.md — Catálogo de agentes del repositorio

## 1. Propósito

Este archivo actúa como catálogo central de agentes definidos en `bkm-operational-agents`.

No sustituye `.github/copilot-instructions.md`.

No define reglas globales del repositorio.

No duplica specs.

Solo indexa los agentes existentes y sus artefactos principales.

## 2. Relación con instrucciones globales

Las reglas generales del repositorio viven en:

`.github/copilot-instructions.md`

Todo agente listado aquí debe respetar:

- la metodología SDD;
- la precedencia documental;
- la source of truth funcional en `bkm-procesos`;
- la prohibición de implementación prematura.

## 3. Agentes registrados

| ID | Nombre funcional | Spec | Proceso fuente | Estado | Comando | Skill | Eval |
|---|---|---|---|---|---|---|---|
| AGENT-001 | Agente de informe mensual de Planificación de Demanda | `specs/02_spec_agente_principal_v0_1.md` | `bkm-procesos/procesos_publicitarios/01_proceso_planificacion_demanda.md` | Structure | `/informe-planificacion-demanda` | `.github/skills/informe-planificacion-demanda/SKILL.md` | `tests/evals/evaluar_informe_planificacion_demanda.md` |

## SDD — Agentes metodológicos

Los siguientes agentes son parte de la capa metodológica SDD y no representan capacidades funcionales del negocio. Su función es gobernar el ciclo SDD del repositorio.

| ID | Nombre | Archivo | Responsabilidad | Estado |
|---|---|---|---|---|
| SDD-AGENT-001 | Specification Agent | `.github/agents/specification.agent.md` | Convertir necesidades en specifications | Active |
| SDD-AGENT-002 | Architect Agent | `.github/agents/architect.agent.md` | Diseñar arquitectura desde specs aprobadas | Active |
| SDD-AGENT-003 | Tasks Planner Agent | `.github/agents/tasks-planner.agent.md` | Convertir specs y arquitectura en tareas trazables | Active |
| SDD-AGENT-004 | Reviewer Agent | `.github/agents/reviewer.agent.md` | Revisar coherencia, riesgos y trazabilidad | Active |
| SDD-AGENT-005 | Documentation Agent | `.github/agents/documentation.agent.md` | Mantener documentación clara y navegable | Active |
| SDD-AGENT-006 | QA Gate Agent | `.github/agents/qa-gate.agent.md` | Validar gates entre fases SDD | Active |
| SDD-AGENT-007 | Implementation Agent | `.github/agents/implementation.agent.md` | Implementar solo trabajo definido y autorizado | Active |

## 4. Estados posibles

- Proposed
- Specification
- Structure
- Ready for Development
- Development
- Validation
- Active
- Deprecated

## 5. Reglas de alta de nuevos agentes

Antes de añadir un nuevo agente funcional a este catálogo debe existir, como mínimo:

- proceso fuente en `bkm-procesos`;
- spec del agente;
- alcance definido;
- fuera de alcance definido;
- estado SDD asignado.

No se debe crear un agente nuevo sin proceso funcional asociado.

Para agentes metodológicos SDD debe existir, como mínimo:

- responsabilidad metodológica definida;
- archivo del agente en `.github/agents/`;
- alineación explícita con la fase SDD y la precedencia documental;
- límites claros para evitar implementación prematura.

## 6. Reglas de mantenimiento

Actualizar este archivo cuando:

- se crea un nuevo agente;
- cambia el estado SDD de un agente;
- se crea o cambia su comando;
- se crea o cambia su skill;
- se crea o cambia su eval;
- se crea o cambia un agente metodológico SDD;
- un agente queda deprecado.

No usar este archivo para documentar la lógica completa del agente.

La lógica vive en la spec correspondiente.