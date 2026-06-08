# Tasks — bkm-operational-agents

## 1. Objetivo

Este documento actúa como backlog documental y técnico del repositorio `bkm-operational-agents`.

Su función es registrar tareas relevantes pendientes, decisiones por cerrar, artefactos por crear o validar y futuras líneas de trabajo dentro del ecosistema SDD.

No sustituye specs, contracts transversales, gates, evals, workflows ni la matriz de artefactos.

No es una lista diaria de tareas operativas.

---

## 2. Principios de uso

- Toda tarea debe estar vinculada a una fase SDD.
- Toda tarea debe tener un artefacto relacionado o una justificación clara.
- Las tareas deben representar trabajo relevante del repositorio, no microacciones.
- No deben registrarse tareas de implementación técnica mientras el proyecto siga en Specification / Structure.
- No debe duplicar tareas ya gestionadas en Notion o GitHub Issues.
- Puede servir en el futuro como fuente de referencia para crear tareas en Notion mediante MCP, pero esa integración no forma parte de la fase actual.

---

## 3. Estados permitidos

- Pendiente
- En curso
- Bloqueada
- Hecha
- Descartada

---

## 4. Tipos de tarea

- Documentación
- Spec
- Contract transversal
- Skill
- Prompt
- Workflow
- Eval
- Gate
- Readiness
- Development futuro
- Integración futura

---

## 5. Backlog actual

| ID | Tarea | Descripción | Fase SDD | Tipo | Estado | Artefacto relacionado | Criterio de cierre |
|----|--------|-------------|----------|------|---------|----------------------|-------------------|
| TASK-001 | Crear glosario ampliado del proyecto | Documentar términos técnicos y metodológicos para facilitar la interpretación del repositorio | Structure | Documentación | Pendiente | `docs/02_glosario_terminos_sdd_y_agentes.md` | Glosario creado y validado |
| TASK-002 | Validar gate de Structure | Revisar si los artefactos mínimos existen y cumplen criterios de readiness | Structure | Gate | Pendiente | `docs/gates/01_structure_gate_v0_1.md` | Gate marcado como aprobado o aprobado con ajustes |
| TASK-003 | Preparar cierre de Specification / Structure | Documentar que la fase de diseño del agente de informe mensual está completa y lista para specs técnicas | Structure | Readiness | Pendiente | `docs/gates/01_structure_gate_v0_1.md` | Documento o sección de cierre validada |
| TASK-004 | Diseñar spec técnica de datos de entrada/salida | Definir estructura técnica esperada de los datos que alimentarán el informe mensual dentro de la spec técnica | Development futuro | Spec | Pendiente | `specs/technical/01_technical_spec_data_contract_planificacion_demanda.md` | Spec técnica creada y revisada |
| TASK-005 | Diseñar spec técnica de ejecución manual/asistida | Definir cómo se ejecutará el informe con datos pegados o exportados antes de conectar BigQuery | Development futuro | Spec | Pendiente | `specs/technical/02_technical_spec_execution_informe_planificacion_demanda.md` | Spec técnica creada y revisada |
| TASK-006 | Diseñar contrato futuro de BigQuery Tool | Definir contrato de solo lectura para futura consulta BigQuery desde el agente | Development futuro | Integración futura | Pendiente | `tools/bigquery/` | Contrato creado sin implementación |
| TASK-007 | Evaluar integración futura con Notion mediante MCP | Analizar si las tareas del backlog pueden derivarse a Notion sin romper la gobernanza SDD | Development futuro | Integración futura | Pendiente | `docs/tasks.md` | Decisión documentada, sin implementación prematura |
| TASK-008 | Crear skill transversal de git sync seguro | Definir procedimiento seguro de `status/add/commit/push` con confirmaciones humanas y control de sensibles | Structure | Skill | Hecha | `.github/skills/git-sync-seguro/SKILL.md` | Skill creada y alineada con SDD |
| TASK-009 | Crear agentes metodológicos SDD | Definir y registrar agentes metodológicos para specification, architecture, planning, review, documentation, gates e implementation | Structure | Documentación | Hecha | `.github/agents/` | Agentes creados y catálogo/documentación alineados |

---

## 6. Reglas de no uso

Este archivo no debe usarse para:

- registrar tareas personales diarias;
- sustituir Notion;
- sustituir GitHub Issues;
- definir lógica funcional;
- aprobar gates;
- implementar código;
- conectar tools reales;
- ejecutar workflows;
- registrar decisiones de negocio.

---

## 7. Relación futura con Notion / MCP

En una fase posterior, este archivo podría servir como fuente de referencia para derivar tareas a Notion mediante MCP.

Esa integración solo podrá plantearse cuando el proyecto entre en una fase autorizada de Development.

Hasta entonces, `tasks.md` es únicamente un backlog documental y técnico.
