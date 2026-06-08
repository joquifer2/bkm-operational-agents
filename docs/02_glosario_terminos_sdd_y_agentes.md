# Glosario de terminos - SDD, agentes y artefactos del proyecto

## 1. Objetivo

Este glosario define los terminos base usados en `bkm-operational-agents` para evitar ambiguedades de gobernanza documental.

No redefine SOPs ni reglas funcionales de negocio.

## 2. Contexto del repositorio

- `bkm-procesos` es la source of truth funcional.
- `bkm-operational-agents` es la capa IA/operativa documental.
- Estado actual: SDD -> Specification / Structure.
- No hay Development activo.

## 3. Definiciones canonicas (obligatorias)

### Spec

Artefacto principal del repositorio para definir agentes, capacidades o componentes.

Una spec responde a:

- que es algo;
- que debe hacer;
- que limites tiene;
- que inputs/outputs acepta;
- que reglas debe respetar.

Una spec puede incluir:

- proposito;
- alcance;
- responsabilidades;
- inputs;
- outputs;
- restricciones;
- riesgos;
- reglas de gobierno;
- criterios de aceptacion;
- Definition of Done.

### Contract

Un contract NO debe ser un archivo separado por defecto.

Solo debe existir como documento separado cuando define reglas transversales que aplican a:

- varias capacidades;
- varias skills;
- o al repositorio completo.

Ejemplos validos de contract transversal:

- source of truth;
- precedencia documental;
- politica de memoria;
- politica de tools;
- reglas human-in-the-loop;
- resolucion de conflictos entre fuentes.

Ejemplos no recomendados:

- contract por agente que repite la spec;
- contract por skill que repite inputs/outputs ya definidos en spec.

### Instructions

Reglas de comportamiento para Copilot o para contextos concretos de trabajo.

Responden a como debe comportarse el asistente mientras trabaja en el repositorio.

Las instructions:

- no sustituyen specs;
- no son contratos de negocio;
- no duplican logica funcional de `bkm-procesos`;
- no redefinen SOPs.

## 4. Regla anti-sobreingenieria documental

Antes de crear un nuevo tipo de artefacto documental:

1. comprobar si la necesidad puede resolverse con una seccion en una spec existente;
2. evitar crear documentos paralelos que repliquen definiciones.

Regla adicional:

- no crear contracts separados salvo que la regla afecte a varios agentes, varias skills o al repositorio completo.

## 5. Separacion entre repositorios

### bkm-procesos

Repositorio funcional canónico. Aqui viven SOPs, dashboards, reglas de negocio y decisiones operativas.

### bkm-operational-agents

Repositorio de capa IA/operativa. Aqui viven specs, instructions, prompts, skills y governance documental.

Regla obligatoria:

- no duplicar SOPs, dashboards, reglas funcionales ni logica de negocio dentro de `bkm-operational-agents`.

## 6. Precedencia documental

En caso de conflicto:

1. `bkm-procesos` (verdad funcional)
2. specs del repositorio
3. `.github/copilot-instructions.md`
4. skills
5. prompts
6. docs/workflows/tools/memory/tests

## 7. Terminos SDD esenciales

### Specification

Fase para definir alcance, limites, reglas, riesgos y criterios de avance.

### Structure

Fase para ordenar artefactos y estructura documental no ejecutable.

### Development

Fase de implementacion tecnica. Solo tras aprobacion explicita.

### Gate

Punto formal de validacion para permitir transicion de fase.

### Readiness

Nivel de preparacion documental suficiente para avanzar sin ambiguedad.

### Human-in-the-loop

La decision final es humana; el sistema asiste, no sustituye el criterio humano.

## 8. Checklist rapido de uso

- Si necesitas definir una capacidad: actualiza la spec.
- Si necesitas una regla global: evalua contract transversal.
- Si necesitas pautar comportamiento del asistente: usa instructions.
- Si necesitas invocacion operativa: usa prompt/comando.

## 9. Cierre

Este glosario prioriza claridad, trazabilidad y simplicidad documental para evitar redundancia y sobreingenieria durante Specification / Structure.
