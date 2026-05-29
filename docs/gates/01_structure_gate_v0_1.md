# Structure Gate v0.1 - Governance and Readiness

## 1. Objetivo del gate

Este gate define el criterio formal para pasar de SDD -> Structure a una fase posterior.

En esta version, el gate es de gobernanza y readiness arquitectonica documental.
No es un testing tecnico ni una validacion de implementacion.

## 2. Naturaleza del gate

Este gate se considera:

- governance gate;
- readiness criteria;
- SDD transition gate;
- architecture readiness check.

Queda fuera de alcance:

- testing tecnico;
- ejecucion de codigo;
- validacion de runtime;
- pruebas de integracion.

## 3. Alcance del gate

El gate verifica que el repositorio mantiene:

- separacion clara con bkm_procesos como source of truth funcional;
- consistencia documental en Specification y Structure;
- precedencia documental operativa;
- restricciones de arquitectura prematura;
- limites de alcance de la fase actual.

## 4. Criterios de readiness (obligatorios)

### 4.1 Gobernanza documental

- Existe una constitucion global en .github/copilot-instructions.md.
- Existe una especificacion base del repositorio en specs/.
- Existe una instruction SDD activa en .github/instructions/.
- Existe un prompt de arranque SDD en .github/prompts/.

### 4.2 Consistencia de alcance

- bkm_procesos aparece explicitamente como verdad funcional.
- bkm-operational-agents se limita a capa IA/operativa documental.
- No hay duplicacion de logica funcional.
- No se desplaza documentacion funcional desde bkm_procesos.

### 4.3 Restricciones de arquitectura prematura

- No se ha elegido framework.
- No se ha definido runtime.
- No se ha definido arquitectura multiagente.
- No se han creado tools reales.
- No hay implementacion tecnica ejecutable.

### 4.4 Readiness para evolucionar

- Existe taxonomia de artefactos y estructura de carpetas.
- Existe matriz de artefactos con permitido/no permitido por fase.
- Existe spec v0.1 del agente de informe mensual con foco documental.
- Existe contrato documental del informe mensual.
- Existe skill documental del informe mensual.
- Existe prompt/comando /informe-planificacion-demanda.
- Existe eval documental del informe mensual.
- Existe checklist de salida documental para fase posterior.

## 5. Evidencias esperadas

- docs/gates/01_structure_gate_v0_1.md
- docs/01_matriz_artefactos_sdd.md
- specs/01_spec_repo_bkm_operational_agents.md
- specs/02_spec_agente_principal_v0_1.md
- specs/contracts/01_contract_informe_indicadores_planificacion_demanda.md
- .github/copilot-instructions.md
- .github/instructions/sdd.instructions.md
- .github/prompts/00_iniciar_proyecto_sdd.prompt.md
- .github/skills/informe-planificacion-demanda/SKILL.md
- .github/prompts/informe-planificacion-demanda.prompt.md
- tests/evals/evaluar_informe_planificacion_demanda.md

## 6. Criterio de decision del gate

El gate puede quedar en uno de estos estados:

- Aprobado: todos los criterios obligatorios cumplidos.
- Aprobado con ajustes: faltan ajustes menores de redaccion o consistencia, sin impacto de alcance.
- No aprobado: faltan criterios criticos de gobernanza o se detecta implementacion prematura.

## 7. Autoridad de aprobacion

La aprobacion del gate requiere validacion humana explicita.

Este gate no permite autoaprobacion automatica por parte del agente.

## 8. Checklist de cierre del gate

- [ ] Se confirma alcance SDD -> Structure.
- [ ] Se confirma precedencia documental.
- [ ] Se confirma no duplicacion funcional respecto a bkm_procesos.
- [ ] Se confirma no framework, no runtime, no multiagente.
- [ ] Se confirma no tools reales ni implementacion tecnica.
- [ ] Se confirma spec del agente de informe mensual v0.1 publicada.
- [ ] Se confirma matriz de artefactos publicada.
- [ ] Se confirma aprobacion humana registrada.

## 9. Resultado esperado de esta iteracion

Cerrar una base documental solida y gobernable para una siguiente iteracion de Structure, sin adelantar decisiones de Development.
