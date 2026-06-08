# Skill - Informe de Planificacion de Demanda

## Proposito

Generar informes mensuales de indicadores operativos del proceso de Planificacion de Demanda, comparando la hipotesis inicial del periodo con la realidad observada al cierre.

## Cuando usar esta skill

Usar esta skill cuando el usuario pida:

- generar el informe mensual de Planificacion de Demanda;
- analizar indicadores operativos del periodo;
- comparar plan vs realidad;
- preparar cierre del periodo;
- redactar aprendizajes del periodo;
- ejecutar el comando /informe-planificacion-demanda.

## Fuente funcional de verdad

- joquifer2/bkm-procesos/procesos_publicitarios/01_proceso_planificacion_demanda.md

La skill no duplica el SOP ni lo modifica.

## Datos autorizados

La skill puede usar:

- datos pegados por el usuario;
- exportaciones del dashboard;
- resumenes de BigQuery proporcionados por el usuario;
- metricas visibles documentadas;
- reglas definidas en la spec del agente y en contracts transversales del repositorio.

En esta fase no se conecta directamente a BigQuery.

## Procedimiento

1. Identificar el periodo.
2. Verificar datos minimos.
3. Separar hipotesis inicial y realidad observada.
4. Analizar desviacion global.
5. Analizar canal.
6. Analizar zona.
7. Analizar cartera, pipeline y necesidad operativa.
8. Revisar ajustes y aprendizajes.
9. Redactar informe.
10. Declarar datos faltantes o cautelas.

## Estructura obligatoria del informe

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

## Reglas criticas

- No inventar datos.
- No crear KPIs nuevos.
- No decidir inversion.
- No ordenar acciones.
- No sustituir validacion humana.
- No usar conversiones Ads como leads.
- No usar CPL como eje principal.
- No sumar stocks como flujos.
- No sumar snapshots entre fechas.
- No sumar acumulados entre filas.
- Distinguir zonas operativas de incidencias de zona/atribucion.
- No incorporar tipologia de campana en v1.

## Salida esperada

Markdown listo para revisar, copiar o guardar como informe operativo.
