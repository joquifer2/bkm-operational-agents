# bkm-operational-agents

Repositorio de capa IA/operativa para BKM.

Este repositorio trabaja sobre bkm_procesos como source of truth funcional y no duplica su logica de negocio.

Estado actual:

- SDD -> Specification / Structure.
- SDD = Spec Driven Development.

Alcance inicial:

- estructura documental minima;
- especificaciones SDD base;
- instructions, prompts y skills de trabajo.
- foco inicial del primer agente en informe mensual de indicadores operativos de Planificacion de Demanda.

Reglas documentales clave:

- la spec es el artefacto principal para agentes, capacidades y componentes;
- los contracts separados quedan reservados para reglas transversales del repositorio/sistema;
- las instructions definen comportamiento de Copilot y no sustituyen specs funcionales.

Fuera de alcance por ahora:

- runtime;
- frameworks;
- multiagente complejo;
- tools reales;
- implementacion tecnica.
