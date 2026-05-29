# Contract - Informe de indicadores operativos de Planificacion de Demanda

## 1. Objetivo

Definir el contrato documental del informe mensual que generara el agente de Planificacion de Demanda.

## 2. Periodicidad

Mensual, al cierre del periodo o cuando el usuario solicite revision del periodo.

## 3. Inputs obligatorios

- `periodo`
- `leads_objetivo`
- `leads_previstos_cartera`
- `leads_previstos_nueva_captacion`
- `inversion_prevista`
- `distribucion_prevista_canal`
- `distribucion_prevista_zona`
- `leads_reales_periodo`
- `desviacion_leads_abs`
- `desviacion_leads_pct`
- `numero_ajustes`
- `estado_periodo`

## 4. Inputs recomendados

- `visitas_objetivo`
- `visitas_reales`
- `inversion_real`
- `cartera_activa_snapshot_inicio`
- `pipeline_visitas_snapshot_inicio`
- `demanda_util_disponible_snapshot_inicio`
- `necesidad_leads_snapshot_inicio`
- `leads_reales_por_canal`
- `inversion_real_por_canal`
- `leads_reales_por_zona`
- `inversion_real_por_zona`
- `aprendizaje_periodo`
- `comentario_cierre`
- `accion_recomendada_siguiente_periodo`

## 5. Outputs

El informe debe devolver Markdown.

Estructura obligatoria:

- titulo;
- periodo;
- resumen ejecutivo;
- lectura inicial;
- lectura de cierre;
- desviaciones;
- canal;
- zona;
- cartera/pipeline/necesidad;
- ajustes;
- aprendizajes;
- recomendacion para revision humana;
- datos faltantes o cautelas.

## 6. Reglas de no invencion

Si falta un dato:

- no inventarlo;
- no interpolarlo;
- no asumirlo;
- marcarlo como no disponible;
- reducir nivel de confianza de la conclusion afectada.

## 7. Metricas prohibidas como eje principal

- conversiones Ads como leads reales;
- CPL como metrica rectora del proceso;
- necesidad_real_nueva_captacion como KPI principal si esta marcada como legacy/deprecated;
- tipologia de campana en v1.

## 8. Tono

Profesional, claro, directo, orientado a decision humana y trazabilidad.
