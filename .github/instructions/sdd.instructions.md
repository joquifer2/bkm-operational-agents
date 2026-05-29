# SDD instructions - bkm-operational-agents

## 1. Objetivo de estas instrucciones

Asegurar que el trabajo se mantiene en la metodologia SDD y respeta el plan aprobado del proyecto.

Estas instrucciones aplican a todo trabajo en este repositorio hasta que se autorice expresamente el paso a Development.

## 2. Estado actual

Estado vigente:

- SDD -> Specification / Structure.

No estamos en Development.

## 3. Reglas SDD por fase

### 3.1 Specification

Permitido:

- definir alcance;
- definir limites;
- definir taxonomias;
- definir contratos documentales;
- definir riesgos;
- definir criterios de salida de fase.

No permitido:

- implementar runtime;
- crear codigo de agentes;
- elegir framework;
- crear tools reales;
- crear workflows ejecutables.

### 3.2 Structure

Permitido:

- crear estructura de carpetas minima;
- crear archivos base de instrucciones, prompts y specs;
- normalizar naming y precedencia documental;
- preparar esqueletos no ejecutables.

No permitido:

- convertir estructura en implementacion tecnica;
- introducir automatizacion operativa;
- construir arquitectura distribuida.

### 3.3 Development

Solo permitido cuando exista aprobacion explicita y checklist de salida completado.

Hasta ese momento, cualquier implementacion queda fuera de alcance.

## 4. Comportamiento esperado durante Specification

- priorizar claridad contractual sobre soluciones tecnicas;
- mantener separacion estricta respecto a bkm_procesos;
- no duplicar logica funcional;
- no crear decisiones tecnologicas definitivas;
- mantener foco inicial del primer agente en informe mensual de indicadores operativos del proceso de Planificacion de Demanda;
- marcar pendientes y riesgos cuando falte validacion.

## 5. Restricciones actuales obligatorias

No hacer todavia:

- seleccion de framework;
- runtime;
- multiagente complejo;
- tools reales;
- workflows automaticos;
- codigo ejecutable de agentes.

## 6. Regla de control de alcance

Si una propuesta entra en implementacion, debe detenerse y volver a:

- contrato;
- limites;
- evidencia documental;
- criterio de fase.

## 7. Criterio de cumplimiento

Estas instrucciones se consideran cumplidas cuando:

- el trabajo producido es documental;
- respeta el plan aprobado;
- mantiene estado Specification / Structure;
- no introduce implementacion prematura.
