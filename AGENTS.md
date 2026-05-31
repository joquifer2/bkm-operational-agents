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

| ID | Nombre funcional | Spec | Proceso fuente | Estado | Comando | Skill | Contract | Eval |
|---|---|---|---|---|---|---|---|---|
| AGENT-001 | Agente de informe mensual de Planificación de Demanda | `specs/02_spec_agente_principal_v0_1.md` | `bkm-procesos/procesos_publicitarios/01_proceso_planificacion_demanda.md` | Structure | `/informe-planificacion-demanda` | `.github/skills/informe-planificacion-demanda/SKILL.md` | `specs/contracts/01_contract_informe_indicadores_planificacion_demanda.md` | `tests/evals/evaluar_informe_planificacion_demanda.md` |

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

Antes de añadir un nuevo agente a este catálogo debe existir, como mínimo:

- proceso fuente en `bkm-procesos`;
- spec del agente;
- alcance definido;
- fuera de alcance definido;
- estado SDD asignado.

No se debe crear un agente nuevo sin proceso funcional asociado.

## 6. Reglas de mantenimiento

Actualizar este archivo cuando:

- se crea un nuevo agente;
- cambia el estado SDD de un agente;
- se crea o cambia su comando;
- se crea o cambia su skill;
- se crea o cambia su contract;
- se crea o cambia su eval;
- un agente queda deprecado.

No usar este archivo para documentar la lógica completa del agente.

La lógica vive en la spec correspondiente.