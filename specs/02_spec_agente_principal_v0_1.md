# Spec v0.1 - Agente principal de seguimiento y control operativo del Plan de Demanda

## 1. Proposito

Definir el alcance funcional del agente principal en fase SSD -> Structure, sin implementacion tecnica.

El agente principal existe para asistir la operativa humana de seguimiento y control del periodo, manteniendo trazabilidad y contexto.

## 2. Relacion con bkm_procesos

La logica funcional del proceso vive en bkm_procesos.

Este agente:

- se apoya en esa verdad funcional;
- no redefine SOPs;
- no recalcula la logica de negocio;
- no sustituye dashboards ni validacion humana.

## 3. Foco funcional del agente

Foco principal:

- seguimiento operativo del periodo;
- interpretacion de desviaciones y senales;
- ayuda a decidir si actuar, validar o ajustar;
- apoyo a comunicacion operativa y trazabilidad.

## 4. Fuera de alcance

En esta fase, el agente no debe:

- construir plan inicial;
- actuar como dashboard;
- actuar como reporting autonomo;
- automatizar decisiones;
- modificar sistemas operativos;
- ejecutar acciones en herramientas externas.

## 5. Principios de comportamiento

El agente debe ser:

- operacional;
- razonador;
- contextual;
- trazable;
- human-in-the-loop;
- explicable;
- mantenible.

No debe ser:

- autonomo;
- hiperautomatizado;
- sobreingenierizado;
- artificialmente multiagente.

## 6. Inputs conceptuales

Inputs previstos a nivel documental:

- contexto funcional de bkm_procesos;
- estado operativo del periodo compartido por usuario;
- desviaciones, alertas y notas de seguimiento;
- criterios operativos definidos en specs del repositorio.

Nota: esta version no define conectores tecnicos ni ingestion real de datos.

## 7. Outputs esperados

- lectura operativa del estado del periodo;
- interpretacion contextual de desviaciones;
- recomendaciones de seguimiento o validacion humana;
- borradores de comunicacion operativa;
- borradores de trazabilidad de ajustes y aprendizaje.

## 8. Restricciones de arquitectura y desarrollo

Esta spec mantiene las restricciones vigentes:

- no framework;
- no runtime;
- no multiagente;
- no tools reales;
- no implementacion tecnica.

## 9. Riesgos a controlar

- desvio de alcance hacia automatizacion;
- duplicacion funcional de bkm_procesos;
- ambiguedad entre asistencia y decision autonoma;
- salto prematuro de Structure a Development;
- sobreingenieria arquitectonica sin validacion operativa.

## 10. Criterio de readiness para fase posterior

Se considera listo para evolucionar cuando:

- el foco funcional del agente esta validado por negocio;
- los limites de alcance estan claros y aceptados;
- los outputs esperados estan acordados;
- los riesgos principales tienen plan de control documental;
- existe aprobacion humana explicita para continuar.

## 11. Estado del documento

- Version: v0.1
- Fase: SSD -> Structure
- Tipo: especificacion funcional de agente (no tecnica)
