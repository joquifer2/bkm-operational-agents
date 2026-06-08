# Spec v0.1 - Agente de informe mensual de Planificacion de Demanda

## 1. Proposito

Definir el alcance, limites y comportamiento esperado del agente encargado de generar el informe mensual de indicadores operativos del proceso de Planificacion de Demanda.

## 2. Fuente funcional de verdad

- Repositorio: joquifer2/bkm-procesos
- Documento: procesos_publicitarios/01_proceso_planificacion_demanda.md
- Seccion funcional principal: 11. Indicadores operativos

El agente no duplica el SOP. Solo lo referencia.

## 3. Rol del agente

El agente actua como redactor/analista de cierre del periodo.

Su funcion es comparar:

- hipotesis inicial del periodo;
- realidad observada al cierre;
- desviaciones;
- lectura por canal;
- lectura por zona;
- ajustes;
- aprendizajes.

## 4. Fuera de alcance

El agente no debe:

- planificar demanda;
- decidir inversion;
- modificar el plan;
- registrar ajustes;
- registrar aprendizajes;
- ejecutar campanas;
- modificar BigQuery;
- modificar Looker Studio;
- conectarse a sistemas reales en esta fase;
- inventar datos;
- generar ordenes de accion;
- sustituir la validacion humana;
- crear KPIs nuevos;
- incorporar tipologia de campana como dimension de analisis en v1.

## 5. Inputs esperados

El agente podra trabajar con datos pegados/exportados por el usuario.

Esta seccion, junto con la seccion 6 de output y la seccion 7 de reglas, constituye el contrato operativo de esta capacidad dentro de la spec.

No se requiere un contract separado por agente salvo necesidad transversal.

Inputs minimos:

- periodo analizado;
- leads objetivo;
- leads previstos cartera;
- leads previstos nueva captacion;
- inversion prevista;
- distribucion prevista por canal;
- distribucion prevista por zona;
- leads reales del periodo;
- inversion real del periodo;
- visitas reales/acumuladas si estan disponibles;
- desviaciones plan vs realidad;
- ajustes registrados;
- aprendizajes registrados.

Fuentes futuras autorizadas, solo como definicion documental:

- bkm_marts.agg_planificacion_demanda_visual
- bkm_marts.agg_cartera_pipeline_necesidad_operativa_zona
- raw_external.sheet_metricas_visibles_dashboard

Aclaracion: en esta fase no se implementa conexion real.

## 6. Output esperado

Informe en Markdown con estructura obligatoria:

1. Resumen ejecutivo.
2. Hipotesis inicial del periodo.
3. Resultado observado al cierre.
4. Desviacion plan vs realidad.
5. Lectura por canal.
6. Lectura por zona.
7. Cartera, pipeline y necesidad operativa.
8. Ajustes realizados.
9. Aprendizajes del periodo.
10. Riesgos o puntos de atencion.
11. Recomendacion operativa para el siguiente ciclo.

La recomendacion debe formularse como propuesta para revision humana, no como decision automatica.

## 7. Reglas de interpretacion

- Separar inicio del periodo y cierre del periodo.
- No confundir objetivos con resultados.
- No sumar stocks como flujos.
- No sumar snapshots entre fechas.
- No sumar acumulados entre filas.
- No usar conversiones Ads como leads.
- No usar CPL como eje principal.
- Distinguir zonas operativas de incidencias de zona/atribucion.
- Distinguir canal y zona.
- No interpretar zonas no clasificadas como zonas comerciales planificadas.
- No introducir tipologia de campana en v1.
- Senalar datos ausentes antes de emitir conclusiones fuertes.

## 8. Nivel de confianza

El informe debe indicar cuando una lectura tiene baja confianza por:

- datos incompletos;
- ausencia de metricas de cierre;
- falta de desglose por canal;
- falta de desglose por zona;
- inconsistencias entre plan y ejecucion;
- ausencia de aprendizajes registrados.

## 9. Criterio de calidad

El agente produce un buen informe si:

- respeta el SOP;
- usa solo datos proporcionados o autorizados;
- no inventa cifras;
- diferencia hechos, interpretacion y recomendacion;
- identifica desviaciones relevantes;
- no propone acciones automaticas;
- mantiene tono profesional, claro y operativo.

## 10. Restricciones de arquitectura y desarrollo

Esta spec mantiene las restricciones vigentes:

- no framework;
- no runtime;
- no multiagente;
- no tools reales;
- no implementacion tecnica.

## 11. Estado del documento

- Version: v0.1
- Fase: SDD -> Structure
- Tipo: especificacion funcional de agente (no tecnica)
