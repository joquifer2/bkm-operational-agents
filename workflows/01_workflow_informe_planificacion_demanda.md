# Workflow conceptual - Informe de Planificacion de Demanda

## 1. Objetivo

Describir el flujo conceptual para generar el informe mensual de indicadores operativos.

## 2. Naturaleza

Workflow conceptual, no ejecutable.

No implementa automatizacion.
No conecta con BigQuery.
No ejecuta agentes reales.

## 3. Flujo

1. Usuario solicita /informe-planificacion-demanda.
2. Usuario indica periodo.
3. Usuario proporciona datos o exportacion.
4. El agente valida datos minimos.
5. El agente identifica datos faltantes.
6. El agente redacta informe.
7. Usuario revisa.
8. Usuario decide si guardar o trasladar el informe a otro sistema.

## 4. Criterios de parada

El agente debe detenerse y pedir aclaracion si:

- falta el periodo;
- faltan datos minimos;
- hay contradiccion entre metricas;
- no se puede diferenciar plan inicial de resultado real.
