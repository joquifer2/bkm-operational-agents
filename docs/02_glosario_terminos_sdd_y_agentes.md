# Glosario de términos — SDD, agentes y artefactos del proyecto

## 1. Objetivo del documento

Este glosario recoge los términos técnicos, metodológicos y operativos utilizados en el repositorio `bkm-operational-agents`.

Su objetivo es facilitar la consulta e interpretación del proyecto para personas técnicas y no técnicas, evitando malentendidos sobre conceptos como SDD, gates, readiness, governance, skills, prompts, contracts, workflows, runtime, tools o agentes.

Este documento no define nuevas reglas funcionales. Solo explica términos ya presentes o necesarios para entender el proyecto.

---

## 2. Contexto del repositorio

`bkm-operational-agents` es el repositorio donde se diseñan capacidades IA/operativas para BKM.

No es la fuente de verdad funcional del negocio.

La fuente de verdad funcional es:

`joquifer2/bkm-procesos`

En este repositorio se documentan:

- especificaciones;
- contratos;
- instrucciones;
- skills;
- prompts;
- workflows conceptuales;
- gates;
- evaluaciones;
- límites de arquitectura;
- criterios de avance.

Actualmente el proyecto está en fase SDD de Specification / Structure.

No está todavía en fase de Development.

---

# Resumen rápido para personas no técnicas

| Término | Idea simple |
|---|---|
| SDD | Diseñar antes de construir |
| Spec | Documento que define qué debe hacer algo |
| Structure | Ordenar carpetas y documentos sin programar todavía |
| Development | Programar o implementar |
| Gate | Punto de control antes de avanzar |
| Readiness | Preparación suficiente para pasar de fase |
| Governance | Reglas para que el proyecto no se desordene |
| Skill | Capacidad estable del agente |
| Prompt | Instrucción para ejecutar una tarea |
| Command | Forma corta de invocar una tarea |
| Contract | Acuerdo de entradas, salidas y límites |
| Workflow | Secuencia de pasos |
| Eval | Criterio para saber si algo está bien |
| Tool | Conector con un sistema externo |
| Runtime | Entorno donde algo se ejecuta |
| Source of Truth | Fuente oficial de verdad |
| Human-in-the-loop | La persona sigue validando |
| No invención | No crear datos que no existen |
| Implementación prematura | Programar antes de tener claro qué construir |

# A

## Acción automática

Acción que un sistema ejecuta sin intervención humana.

Ejemplos:

- modificar un dato;
- enviar un informe;
- actualizar BigQuery;
- crear una tarea;
- ejecutar una campaña;
- registrar un ajuste.

En la fase actual, las acciones automáticas están fuera de alcance.

El agente puede redactar, interpretar y estructurar información, pero no ejecutar acciones reales.

---

## Agente

Entidad conceptual diseñada para cumplir una función concreta siguiendo reglas definidas.

En este repositorio, un agente no implica necesariamente código ejecutable.

Puede existir únicamente como especificación documental.

Ejemplo:

`Agente de informe mensual de Planificación de Demanda`

Su función es generar un informe mensual comparando la hipótesis inicial del periodo con la realidad observada al cierre.

---

## Agente documental

Agente definido solo a nivel documental.

No tiene runtime.

No ejecuta código.

No se conecta a sistemas externos.

No toma decisiones automáticas.

En este proyecto, el agente actual es documental.

---

## Agente ejecutable

Agente implementado técnicamente mediante código, runtime, tools y lógica de ejecución.

Ejemplo futuro:

Un agente que consulte BigQuery, valide datos y genere automáticamente un informe.

En la fase actual no se permite crear agentes ejecutables.

---

## Agente principal

Primer agente definido en el repositorio.

En este proyecto, el agente principal es:

`Agente de informe mensual de Planificación de Demanda`

No es un sistema multiagente.

No es un controlador operativo.

No ejecuta campañas.

No decide inversión.

---

## Alcance

Conjunto de responsabilidades que sí pertenecen a un documento, agente, fase o repositorio.

Ejemplo de alcance del agente actual:

- generar informe mensual;
- comparar plan vs realidad;
- detectar desviaciones;
- redactar aprendizajes;
- formular recomendaciones para revisión humana.

---

## Architecture Readiness Check

Comprobación de que la arquitectura documental está suficientemente preparada para avanzar.

No es una prueba técnica.

No valida código.

No valida integraciones.

Sirve para confirmar que el proyecto tiene:

- estructura documental clara;
- límites definidos;
- contratos;
- specs;
- criterios de avance;
- ausencia de implementación prematura.

---

## Artefacto

Cualquier pieza documental o técnica que forma parte del proyecto.

Ejemplos:

- spec;
- contract;
- skill;
- prompt;
- workflow;
- eval;
- gate;
- README;
- instructions.

---

## Artefacto obligatorio

Documento que debe existir para que una fase se considere suficientemente definida.

Para el primer caso de uso del repositorio, los artefactos obligatorios son:

- spec del agente;
- contrato del informe;
- skill documental;
- prompt/comando;
- workflow conceptual;
- eval documental;
- gate de Structure;
- matriz de artefactos.

---

## Artefacto opcional

Documento que puede ayudar, pero no bloquea necesariamente el avance de fase.

Ejemplo:

- notas de decisión;
- ejemplos adicionales;
- plantillas secundarias;
- documentación complementaria.

---

# B

## BigQuery Tool

Tool futura que permitiría al agente consultar BigQuery.

En la fase actual solo puede existir como contrato documental futuro.

No debe implementarse todavía.

No debe conectarse a datos reales todavía.

---

## BKM procesos

Repositorio funcional donde viven los SOPs, dashboards, reglas operativas y documentación funcional.

En este proyecto, `bkm-procesos` es la fuente de verdad funcional.

`bkm-operational-agents` no debe duplicar ni reemplazar su contenido.

---

# C

## Capacidad

Habilidad estable que un agente puede aplicar de forma repetible para resolver un tipo concreto de tarea.

Una capacidad no es una ejecución puntual, sino una competencia definida del sistema.

Ejemplo:

`Generar informes mensuales de Planificación de Demanda`

Esta capacidad puede apoyarse en varios artefactos:

- una spec que define el alcance;
- un contract que define entradas y salidas;
- una skill que describe cómo aplicar la capacidad;
- un prompt o command que permite invocarla;
- una eval que valida si el resultado es correcto.

Diferencia importante:

- **Capacidad**: qué sabe hacer el sistema.
- **Skill**: cómo se documenta esa capacidad.
- **Prompt/command**: cómo se invoca en una ejecución concreta.
- **Workflow**: en qué secuencia de pasos se aplica.

En este proyecto, una capacidad debe estar documentada antes de convertirse en implementación técnica.

## Capa IA/operativa

Capa documental donde se diseñan capacidades de asistencia basadas en IA para apoyar procesos operativos.

No sustituye los procesos.

No sustituye el criterio humano.

No sustituye la fuente funcional.

---

## Criterio de avance

Condición que debe cumplirse para pasar de una fase a otra.

Ejemplo:

No pasar a Development si no existen:

- spec aprobada;
- contrato definido;
- skill creada;
- prompt creado;
- eval definida;
- gate validado.

---

## Criterio de calidad

Regla que permite decidir si un artefacto o resultado es válido.

Ejemplo para un informe:

- no inventa datos;
- separa hipótesis inicial y realidad observada;
- no usa conversiones Ads como leads;
- no propone decisiones automáticas.

---

## Criterio de parada

Condición que obliga al agente o proceso a detenerse antes de continuar.

Ejemplos:

- falta el periodo;
- faltan datos mínimos;
- hay contradicción entre métricas;
- no se distingue plan inicial de resultado real.

---

## Command

Forma operativa de invocar una capacidad desde VS Code / Copilot.

Ejemplo:

`/informe-planificacion-demanda periodo=2026-05`

El command no contiene toda la lógica.

La lógica debe estar definida en:

- spec;
- contract;
- skill;
- prompt.

---

## Contract

Documento que define el acuerdo de funcionamiento de una capacidad.

Un contract establece:

- inputs obligatorios;
- inputs recomendados;
- outputs;
- reglas de no invención;
- límites;
- criterios de calidad.

Ejemplo:

`specs/contracts/01_contract_informe_indicadores_planificacion_demanda.md`

---

## Copilot Instructions

Archivo de reglas globales para Copilot dentro del repositorio.

Define:

- propósito del repo;
- relación con `bkm-procesos`;
- metodología SDD;
- precedencia documental;
- restricciones;
- foco inicial del agente.

Ruta habitual:

`.github/copilot-instructions.md`

---

## Contradicción documental

Situación en la que dos documentos dicen cosas incompatibles.

Ejemplo:

Un documento dice que el agente puede consultar BigQuery, pero otro dice que no hay tools reales en esta fase.

Regla:

Cuando haya contradicción, prevalece el documento de mayor precedencia.

---

## Control documental

Mecanismo para mantener el proyecto ordenado y evitar saltos prematuros a implementación.

Incluye:

- specs;
- gates;
- contracts;
- checklists;
- evals;
- precedencia documental.

---

# D

## Datos autorizados

Datos que el agente puede utilizar según la spec, skill o contract.

En la fase actual, el agente puede usar:

- datos pegados por el usuario;
- exportaciones del dashboard;
- resúmenes de BigQuery proporcionados manualmente;
- métricas visibles documentadas;
- contratos documentales.

No puede consultar sistemas reales por sí mismo.

---

## Datos faltantes

Datos necesarios para generar un informe completo que no han sido proporcionados.

El agente debe declararlos explícitamente.

No debe inventarlos.

No debe asumirlos.

No debe interpolarlos.

---

## Development

Fase en la que se implementa técnicamente lo que ya fue definido.

Puede incluir:

- código;
- runtime;
- tools reales;
- integraciones;
- automatizaciones;
- validaciones técnicas.

El proyecto actual todavía no está en Development.

---

## Documento canónico

Documento que actúa como referencia principal para una parte del proyecto.

Ejemplo:

- `bkm-procesos/procesos_publicitarios/01_proceso_planificacion_demanda.md` es el documento funcional canónico del proceso.
- `specs/02_spec_agente_principal_v0_1.md` es la spec canónica del agente principal.

---

## Duplicación funcional

Copiar o redefinir en `bkm-operational-agents` reglas que ya pertenecen a `bkm-procesos`.

No está permitido.

El repositorio de agentes puede referenciar el SOP, pero no debe sustituirlo ni reescribirlo.

---

# E

## Eval

Documento que define cómo evaluar si un resultado es correcto.

En este proyecto, una eval puede comprobar si un informe:

- respeta el SOP;
- no inventa datos;
- diferencia plan y realidad;
- no propone decisiones automáticas;
- declara datos faltantes.

Ejemplo:

`tests/evals/evaluar_informe_planificacion_demanda.md`

---

## Evidencia esperada

Artefacto o prueba documental que demuestra que un criterio está cumplido.

Ejemplo:

Para cerrar el Structure Gate, evidencias esperadas pueden ser:

- spec del agente;
- contrato del informe;
- skill;
- prompt;
- eval;
- matriz de artefactos.

---

## Ejecución

Acto de poner en marcha una capacidad o sistema.

En la fase actual, no hay ejecución real de agentes.

Solo hay diseño documental.

---

## Exportación del dashboard

Datos extraídos manualmente desde Looker Studio o BigQuery para alimentar el informe.

En la fase actual, el agente puede trabajar con exportaciones proporcionadas por el usuario.

---

# F

## Fase

Etapa del ciclo SDD.

Las fases principales son:

- Specification;
- Structure;
- Development;
- Validation.

Cada fase tiene permisos y límites distintos.

---

## Framework

Librería o entorno utilizado para construir agentes o sistemas IA.

Ejemplos:

- LangChain;
- CrewAI;
- PydanticAI.

En la fase actual no se debe elegir framework.

---

## Fuente funcional

Documento o repositorio que contiene la verdad operativa del negocio.

En este proyecto:

`bkm-procesos`

es la fuente funcional.

---

## Fuente futura autorizada

Fuente que podrá usarse más adelante, pero que todavía no está conectada.

Ejemplo:

`bkm_marts.agg_planificacion_demanda_visual`

puede ser fuente futura autorizada para el informe, pero en la fase actual no hay conexión real.

---

# G

## Gate

Punto formal de validación entre fases.

Sirve para decidir si se puede avanzar.

No es una prueba técnica.

No ejecuta código.

Ejemplo:

`docs/gates/01_structure_gate_v0_1.md`

---

## Governance

Gobernanza del proyecto.

Conjunto de reglas que aseguran que el repositorio evoluciona de forma ordenada.

Incluye:

- precedencia documental;
- límites de fase;
- gates;
- criterios de readiness;
- prohibición de implementación prematura.

---

## Governance Gate

Gate orientado a validar gobernanza, no código.

Comprueba que:

- hay separación con la fuente funcional;
- no se duplica lógica;
- no se han creado tools reales;
- no se ha elegido framework;
- no se ha saltado a Development.

---

# H

## Human-in-the-loop

Principio por el cual la decisión final sigue siendo humana.

El agente puede analizar, redactar o recomendar, pero no decidir automáticamente.

En este proyecto, el agente debe apoyar a Jordi/Carlos, no sustituir su criterio.

---

## Hipótesis inicial

Referencia de planificación registrada al inicio del periodo.

Incluye:

- leads objetivo;
- mix cartera/nueva captación;
- distribución por canal;
- distribución por zona;
- inversión prevista.

El informe compara esta hipótesis contra la realidad observada al cierre.

---

# I

## Implementación

Construcción técnica de una capacidad.

Puede incluir:

- código;
- conexión a datos;
- runtime;
- automatización;
- despliegue.

No está permitida todavía en la fase actual.

---

## Implementación prematura

Construir código, tools, runtime o automatizaciones antes de que existan specs, contracts y gates aprobados.

Es uno de los principales riesgos del proyecto.

---

## Indicadores operativos

Métricas usadas para evaluar si la planificación de demanda fue útil.

En el SOP se dividen en:

- indicadores al inicio del periodo;
- indicadores al cierre del periodo.

No deben confundirse con KPIs publicitarios diarios.

---

## Input

Dato de entrada necesario para una capacidad.

Ejemplos:

- periodo;
- leads objetivo;
- inversión prevista;
- leads reales;
- número de ajustes.

---

## Input obligatorio

Dato mínimo sin el cual el informe no debería generar conclusiones fuertes.

Ejemplos:

- periodo;
- leads objetivo;
- leads reales;
- desviación leads;
- número de ajustes.

---

## Input recomendado

Dato que mejora la calidad del informe, pero que no siempre es imprescindible.

Ejemplos:

- visitas reales;
- inversión real;
- aprendizaje del periodo;
- comentario de cierre.

---

## Instruction

Regla operativa que guía el comportamiento de Copilot o del agente.

Las instructions tienen más peso que los prompts.

Ejemplo:

`.github/instructions/sdd.instructions.md`

---

## Integración

Conexión técnica entre el agente y un sistema externo.

Ejemplos:

- BigQuery;
- Notion;
- Gmail;
- Looker Studio.

En la fase actual no hay integraciones reales.

---

# L

## Lógica funcional

Reglas de negocio del proceso.

Ejemplo:

- no usar conversiones Ads como leads;
- no usar CPL como eje principal;
- separar canal y zona;
- distinguir zonas operativas e incidencias.

La lógica funcional vive en `bkm-procesos`, no en `bkm-operational-agents`.

---

## Límite de alcance

Frontera que indica qué no puede hacer un agente, documento o fase.

Ejemplo:

El agente de informe no puede decidir inversión ni modificar datos.

---

# M

## Matriz de artefactos

Documento que enumera qué tipos de artefactos existen, dónde viven y qué función cumplen.

Ejemplo:

`docs/01_matriz_artefactos_sdd.md`

Sirve para evitar desorden documental.

---

## Métrica prohibida como eje principal

Métrica que puede existir como dato auxiliar, pero no debe dirigir la interpretación del informe.

Ejemplos:

- conversiones Ads como leads;
- CPL como métrica rectora;
- `necesidad_real_nueva_captacion` si está marcada como legacy/deprecated.

---

## Multiagente

Arquitectura formada por varios agentes especializados.

Ejemplo:

- agente analista;
- agente redactor;
- agente revisor;
- agente ejecutor.

En la fase actual no se permite crear arquitectura multiagente.

---

# N

## No aprobación

Resultado de un gate o eval cuando se detectan fallos críticos.

Ejemplos de causas:

- falta spec;
- se ha creado implementación prematura;
- se contradice el SOP;
- se inventan datos;
- se proponen decisiones automáticas.

---

## No invención

Regla que obliga al agente a no crear datos que no existen.

Si falta un dato, debe decirlo.

No debe asumirlo.

No debe inventarlo.

No debe completarlo artificialmente.

---

# O

## Orquestación

Coordinación automática entre varios pasos, agentes o tools.

Ejemplo:

consultar BigQuery → generar informe → guardarlo en Notion → enviar email.

En la fase actual no se permite orquestación automática.

---

## Output

Resultado generado por una capacidad.

Ejemplo:

- informe Markdown;
- resumen ejecutivo;
- análisis de desviaciones;
- recomendación para revisión humana.

---

# P

## Precedencia documental

Orden que indica qué documento manda sobre otro en caso de contradicción.

Precedencia recomendada:

1. `bkm-procesos`
2. specs
3. copilot-instructions
4. skills
5. prompts
6. docs / workflows / tools / memory / tests

---

## Prompt

Instrucción operativa para ejecutar una capacidad concreta.

Ejemplo:

`.github/prompts/informe-planificacion-demanda.prompt.md`

Un prompt no debe contener toda la lógica del sistema.

Debe apoyarse en:

- spec;
- contract;
- skill.

---

## Prompt de arranque

Prompt usado para iniciar un proceso de trabajo dentro del repositorio.

Ejemplo:

`00_iniciar_proyecto_sdd.prompt.md`

---

## Prompt/comando

Prompt diseñado para usarse como comando operativo.

Ejemplo:

`/informe-planificacion-demanda`

---

## Prohibición vigente

Restricción activa durante una fase.

Ejemplos actuales:

- no framework;
- no runtime;
- no multiagente;
- no tools reales;
- no workflows ejecutables;
- no código ejecutable.

---

# R

## Readiness

Estado de preparación suficiente para avanzar.

No significa que el sistema esté implementado.

Significa que hay claridad documental para pasar a la siguiente fase.

---

## Readiness Criteria

Criterios que deben cumplirse para considerar que el proyecto está preparado para avanzar.

Ejemplos:

- existe spec;
- existe contrato;
- existe skill;
- existe prompt;
- existe eval;
- no hay implementación prematura;
- se respeta la precedencia documental.

---

## Recomendación operativa

Propuesta redactada por el agente para ayudar a la revisión humana.

No es una orden.

No es una decisión cerrada.

Debe formularse con cautela y trazabilidad.

---

## Registro operativo

Lugar o sistema donde se registran decisiones, ajustes o aprendizajes reales.

En este proyecto, el agente no registra nada.

Solo redacta un informe.

---

## Restricción de arquitectura prematura

Regla que impide tomar decisiones técnicas demasiado pronto.

Ejemplos:

- elegir LangChain antes de cerrar specs;
- crear tools BigQuery antes de validar el contrato;
- crear runtime antes de pasar el gate.

---

## Runtime

Entorno donde se ejecuta realmente un agente.

Ejemplos:

- script Python;
- aplicación;
- Cloud Run;
- Docker;
- API.

No existe runtime en la fase actual.

---

# S

## SDD

Spec Driven Development.

Metodología que prioriza definir primero qué se debe construir antes de implementarlo.

Secuencia recomendada:

1. Specification
2. Structure
3. Development
4. Validation

---

## SDD Transition Gate

Gate que valida si el proyecto puede pasar de una fase SDD a otra.

Ejemplo:

pasar de Structure a Development.

---

## Skill

Capacidad estable y reutilizable.

Define cómo debe comportarse el agente ante un tipo de tarea.

Ejemplo:

`.github/skills/informe-planificacion-demanda/SKILL.md`

La skill define:

- propósito;
- cuándo usarla;
- fuentes autorizadas;
- procedimiento;
- estructura del informe;
- reglas críticas;
- salida esperada.

---

## SOP

Standard Operating Procedure.

Documento funcional que describe cómo se ejecuta un proceso.

Ejemplo:

`procesos_publicitarios/01_proceso_planificacion_demanda.md`

El SOP vive en `bkm-procesos`.

No debe duplicarse en `bkm-operational-agents`.

---

## Source of Truth

Fuente oficial de verdad.

En este proyecto:

`bkm-procesos`

es la source of truth funcional.

Si hay contradicción, prevalece sobre `bkm-operational-agents`.

---

## Spec

Documento que define qué debe hacer una capacidad.

No implementa.

No ejecuta.

No conecta sistemas.

Ejemplo:

`specs/02_spec_agente_principal_v0_1.md`

---

## Spec de agente

Documento que define:

- propósito del agente;
- rol;
- fuera de alcance;
- inputs esperados;
- output esperado;
- reglas de interpretación;
- criterios de calidad.

---

## Spec de repositorio

Documento que define el propósito general del repositorio, su relación con otros repositorios, taxonomía de artefactos, límites y precedencia.

Ejemplo:

`specs/01_spec_repo_bkm_operational_agents.md`

---

## Specification

Primera fase SDD.

Sirve para definir:

- propósito;
- alcance;
- límites;
- contratos;
- riesgos;
- criterios de salida.

No permite implementación técnica.

---

## Structure

Fase SDD de organización documental.

Permite:

- crear carpetas;
- crear esqueletos;
- organizar artefactos;
- definir matriz;
- crear skills, prompts y contracts documentales.

No permite convertir la estructura en código ejecutable.

---

# T

## Taxonomía

Clasificación ordenada de conceptos o artefactos.

Ejemplo:

clasificar artefactos en specs, contracts, skills, prompts, workflows, tools, tests.

---

## Testing técnico

Prueba técnica de código, integración o runtime.

No forma parte del gate actual.

El Structure Gate actual es documental, no técnico.

---

## Tool

Componente que permite a un agente interactuar con un sistema externo.

Ejemplos:

- BigQuery Tool;
- Gmail Tool;
- Notion Tool.

En la fase actual solo se permiten contratos futuros de tools, no tools reales.

---

## Tool real

Tool conectada efectivamente a un sistema.

Ejemplo:

una tool que consulta BigQuery de verdad.

No está permitida todavía.

---

## Trazabilidad

Capacidad de entender de dónde viene una conclusión, dato o decisión.

En este proyecto, el informe debe ser trazable:

- qué datos usa;
- qué falta;
- qué interpreta;
- qué recomienda;
- con qué nivel de confianza.

---

# V

## Validación humana

Revisión explícita realizada por una persona.

En este proyecto, el agente no se autoaprueba.

Los gates requieren validación humana.

Las recomendaciones del informe requieren revisión humana.

---

## Validation

Fase o actividad de comprobación.

Puede ser:

- documental;
- funcional;
- técnica.

En la fase actual, la validación es principalmente documental.

---

## VS Code / Copilot

Entorno previsto para trabajar con instrucciones, prompts y comandos.

Ejemplo de comando previsto:

`/informe-planificacion-demanda`

---

# W

## Workflow

Descripción de una secuencia de pasos.

Puede ser conceptual o ejecutable.

---

## Workflow conceptual

Workflow que describe pasos lógicos, pero no ejecuta nada.

Ejemplo:

`workflows/01_workflow_informe_planificacion_demanda.md`

---

## Workflow ejecutable

Workflow que automatiza acciones reales.

Ejemplo:

un GitHub Action que ejecuta código.

No está permitido en la fase actual.

---

# Z

## Zona operativa

Zona válida para planificación y lectura comercial.

Ejemplo:

- Cataluña;
- Madrid.

---

## Zona no clasificada

Registro que no ha podido asignarse correctamente a una zona operativa.

No debe interpretarse como zona comercial planificada.

---
