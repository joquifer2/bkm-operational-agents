# Copilot instructions - bkm-operational-agents

## 1. Proposito del repositorio

Este repositorio define la capa IA/operativa de BKM sobre la verdad funcional existente.

No es un repositorio de SOPs ni de logica funcional de negocio.

Su objetivo es documentar y organizar:

- contratos de comportamiento IA;
- especificaciones del sistema de agentes operativos;
- instrucciones, prompts y skills de Copilot;
- politicas de uso, limites y trazabilidad;
- criterios de calidad para evolucionar de Specification a Structure y Development.

## 2. Relacion con bkm_procesos

bkm_procesos es la source of truth funcional y operativa del negocio.

En bkm_procesos viven:

- SOPs;
- dashboards;
- reglas funcionales;
- documentacion operativa;
- especificaciones funcionales.

Regla obligatoria:

- No duplicar logica funcional en este repositorio.
- No mover documentacion funcional desde bkm_procesos.
- No reinterpretar SOPs como si fueran especificaciones tecnicas de runtime.

Cuando exista conflicto entre documentos, prevalece la verdad funcional de bkm_procesos.

## 3. Metodologia SDD

Este repositorio debe evolucionar por fases SDD (Spec Driven Development):

- Specification: definicion de alcance, contratos, limites, riesgos y criterios de avance.
- Structure: organizacion documental y esqueletos minimos no ejecutables.
- Development: implementacion tecnica, solo tras cierre formal de fases previas.

Estado actual esperado:

- SDD -> Specification / Structure.

No se permite saltar a Development sin completar los criterios de salida definidos en specs.

## 4. Precedencia documental

Orden de precedencia:

1. bkm_procesos como verdad funcional.
2. specs del repo bkm-operational-agents.
3. este archivo de copilot-instructions.
4. skills en .github/skills.
5. prompts en .github/prompts.
6. docs, workflows, tools, memory y tests.

Ningun artefacto de menor precedencia puede contradecir a uno de mayor precedencia.

## 5. Restricciones de arquitectura prematura

Hasta nuevo aviso, esta prohibido:

- elegir framework definitivo;
- definir runtime de agentes;
- crear arquitectura multiagente compleja;
- crear orquestacion automatica;
- crear tools reales conectadas a sistemas;
- crear workflows ejecutables.

No se permiten decisiones tecnologicas irreversibles en fase Specification / Structure.

## 6. Filosofia del sistema

El sistema debe ser:

- operacional;
- razonador;
- contextual;
- trazable;
- human-in-the-loop;
- mantenible;
- explicable;
- modular.

El sistema no debe ser:

- autonomo;
- hiperautomatizado;
- sobreingenierizado;
- artificialmente multiagente.

## 7. Enfoque operativo

Este repositorio construye capacidades de asistencia operativa y control documental.

No sustituye:

- el criterio humano;
- la validacion operativa;
- la toma de decision final de negocio.

## 8. Foco inicial del primer agente

El foco inicial del sistema se centra en un unico agente documental:

- nombre funcional recomendado: Agente de informe mensual de Planificacion de Demanda;
- nombre tecnico sugerido: demand_planning_report_agent;
- comando operativo previsto: /informe-planificacion-demanda.

Alcance del agente:

- generar el informe mensual de indicadores operativos del proceso de Planificacion de Demanda;
- comparar hipotesis inicial del periodo vs realidad observada al cierre;
- trabajar solo con datos ya preparados o proporcionados por el usuario.

Limites explicitos:

- no planifica;
- no decide inversion;
- no ejecuta acciones;
- no modifica datos;
- no registra ajustes;
- no sustituye validacion humana;
- no crea KPIs nuevos;
- no usa conversiones Ads como leads;
- no usa CPL como eje principal;
- no incorpora tipologia de campana en v1 (queda para posible v2).

## 9. Regla de no implementacion prematura

Mientras no se autorice Development:

- no crear codigo ejecutable de agentes;
- no crear runtime;
- no crear integraciones reales;
- no crear automatizacion operativa.

Primero se cierran contratos documentales y estructura base.

## 10. TASKS GOVERNANCE

El archivo `docs/tasks.md` actua como backlog documental y tecnico del repositorio.

Su funcion es mantener trazabilidad de trabajo pendiente relevante dentro del ecosistema SDD.

Antes de cerrar cualquier trabajo significativo, evaluar si dicho cambio afecta al backlog.

Actualizar `docs/tasks.md` unicamente cuando ocurra alguna de las siguientes situaciones:

- se crea un nuevo artefacto relevante;
- se identifica una nueva linea de trabajo futura;
- se detecta una dependencia importante;
- se alcanza un readiness gate;
- se completa una tarea registrada;
- una tarea deja de ser necesaria;
- aparece una nueva necesidad de Specification, Structure o Development futuro.

No registrar:

- commits;
- cambios de formato;
- correcciones menores;
- tareas personales;
- actividad diaria;
- microacciones.

El backlog debe reflejar trabajo significativo del repositorio, no actividad operativa cotidiana.

## 11. Comprobacion de cierre para cambios significativos

Antes de considerar completado un cambio significativo:

1. Revisar si afecta a Specs.
2. Revisar si afecta a Contracts.
3. Revisar si afecta a Skills.
4. Revisar si afecta a Prompts.
5. Revisar si afecta a Gates.
6. Revisar si requiere actualizacion de `docs/tasks.md`.

Si la respuesta es si, actualizar el artefacto correspondiente.
