# Specification v0.1 - Repositorio bkm-operational-agents

## 1. Proposito del repositorio

bkm-operational-agents define la capa IA/operativa para asistencia y control documental sobre la operativa de BKM.

Este repositorio no define la verdad funcional del negocio. Su finalidad es organizar especificaciones, instrucciones y artefactos de razonamiento operativo bajo metodologia SDD (Spec Driven Development).

## 2. Relacion con bkm_procesos

bkm_procesos es la source of truth funcional y operativa.

bkm-operational-agents:

- referencia la verdad funcional;
- no la duplica;
- no la reemplaza;
- no migra contenido funcional.

En caso de contradiccion, prevalece bkm_procesos.

## 2.1 Foco inicial del primer agente

El primer agente del sistema se limita a generar el informe mensual de indicadores operativos del proceso de Planificacion de Demanda, comparando la hipotesis inicial del periodo con la realidad observada al cierre, a partir de datos ya preparados o proporcionados por el usuario.

Queda fuera de alcance en esta fase:

- no planifica;
- no decide inversion;
- no ejecuta acciones;
- no modifica datos;
- no registra ajustes;
- no sustituye validacion humana;
- no crea KPIs nuevos;
- no usa conversiones Ads como leads;
- no usa CPL como eje principal;
- no incorpora distribucion por tipologia de campana en v1 (queda para posible v2).

## 3. Que pertenece aqui y que no

### 3.1 Si pertenece

- especificaciones SDD de repositorio, agentes y capacidades;
- instrucciones de Copilot;
- prompts de trabajo;
- skills documentales;
- especificaciones del sistema de agentes;
- contracts separados solo cuando sean transversales;
- politicas de workflows, tools y memoria;
- criterios de validacion y checklist de avance.

### 3.2 No pertenece

- SOPs funcionales;
- reglas de negocio;
- dashboards funcionales;
- implementacion de runtime;
- orquestacion automatica;
- tools reales conectadas a sistemas;
- codigo de agentes ejecutables.

## 4. Taxonomia de artefactos

- .github/copilot-instructions.md: constitucion global del repositorio.
- .github/instructions/: reglas operativas por metodo o contexto.
- .github/agents/: agentes metodologicos SDD para gobernar specification, architecture, planning, review, gates e implementation.
- .github/prompts/: prompts reutilizables de arranque, evaluacion y trabajo.
- .github/skills/: skills documentales y de capacidad, no ejecutables complejas por ahora.
- docs/: documentacion de contexto y decisiones del proyecto.
- specs/: especificaciones formales de repositorio y capacidades.
- workflows/: definiciones conceptuales de flujo, no ejecucion.
- tools/: contratos de herramientas futuras, no implementacion.
- memory/: politica de memoria y limites.
- tests/: validaciones documentales y de calidad.

## 4.1 Definiciones canonicas

Spec:

- artefacto principal para describir que es algo, que debe hacer, que limites tiene, que inputs/outputs acepta y que reglas debe respetar;
- puede incluir proposito, alcance, responsabilidades, inputs, outputs, restricciones, riesgos, reglas de gobierno, criterios de aceptacion y Definition of Done.

Contract:

- no debe ser un archivo separado por defecto;
- solo debe existir separado si define reglas transversales del repositorio o del sistema completo;
- ejemplos validos: source of truth, precedencia documental, politica de memoria, politica de tools, human-in-the-loop y resolucion de conflictos entre fuentes.

Instructions:

- reglas de comportamiento para Copilot o para contextos concretos de trabajo;
- no sustituyen specs;
- no duplican logica funcional de bkm_procesos;
- no redefinen SOPs.

Regla anti-sobreingenieria documental:

- antes de crear un nuevo tipo de artefacto documental, comprobar si puede resolverse con una seccion dentro de una spec existente;
- no crear contracts separados salvo que la regla afecte a varios agentes, varias skills o al repositorio completo.

## 5. Estructura de carpetas

Estructura minima esperada:

- .github/
- .github/instructions/
- .github/agents/
- .github/prompts/
- .github/skills/
- docs/
- specs/
- workflows/
- tools/
- memory/
- tests/

## 6. Politica de prompts

Los prompts deben:

- tener una finalidad concreta;
- ser reutilizables;
- respetar la precedencia documental;
- mantener foco en SDD.

Los prompts no deben:

- introducir implementacion tecnica;
- imponer frameworks;
- contradecir specs o instructions.

## 7. Politica de instructions

Las instructions deben:

- fijar reglas globales o de fase;
- definir comportamiento esperado;
- explicitar limites de alcance.

Las instructions tienen mayor precedencia que prompts y skills.

## 8. Politica de skills

Las skills en esta fase deben ser:

- ligeras;
- documentales;
- orientadas a soporte de Specification / Structure.

Aun no se permiten skills ejecutables complejas ni acoplamiento a runtime.

## 9. Politica de workflows

Los workflows en esta fase son:

- conceptuales;
- descriptivos;
- no ejecutables.

No se permite automatizacion ni orquestacion tecnica.

## 10. Politica de tools

Las tools en esta fase son contratos futuros.

Permitido:

- definir intencion y limites de uso.

No permitido:

- implementacion real;
- integracion con sistemas;
- ejecucion automatica.

## 11. Politica de memoria

La memoria en esta fase es documental.

Permitido:

- definir criterios de que recordar y por que.

No permitido:

- persistencia operativa real;
- estado transaccional;
- sustitucion de contratos documentales.

## 12. Riesgos principales

- arquitectura prematura;
- eleccion temprana de framework;
- salto indebido a Development;
- sobreingenieria multiagente;
- duplicacion de logica funcional de bkm_procesos;
- confusion entre contratos documentales e implementacion.

## 13. Limites de la fase actual

Fase actual: SDD -> Specification / Structure.

Limites:

- sin framework;
- sin runtime;
- sin orquestacion;
- sin agentes ejecutables;
- sin tools reales;
- sin workflows automaticos.

## 14. Precedencia documental

Orden de precedencia:

1. bkm_procesos como verdad funcional.
2. specs del repositorio.
3. .github/copilot-instructions.md.
4. .github/agents/.
5. .github/skills/.
6. .github/prompts/.
7. docs, workflows, tools, memory, tests.

## 15. Checklist para pasar a Development

Antes de Development, debe existir:

- Specification v0.x aprobada;
- Structure minima creada y validada;
- limites de alcance aceptados;
- riesgos documentados;
- reglas de precedencia operativas;
- criterios de evaluacion inicial definidos;
- aprobacion explicita para iniciar implementacion.

Sin estos puntos, Development no debe iniciarse.
