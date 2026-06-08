# Prompt - /informe-planificacion-demanda

## Uso

Generar el informe mensual de indicadores operativos de Planificacion de Demanda.

## Comando esperado

`/informe-planificacion-demanda periodo=<YYYY-MM>`

Tambien debe funcionar si el usuario no indica periodo, en cuyo caso se le debe pedir.

## Instruccion

Usa la skill:

`.github/skills/informe-planificacion-demanda/SKILL.md`

y la spec:

`specs/02_spec_agente_principal_v0_1.md`

para generar un informe mensual de Planificacion de Demanda.

## Entradas esperadas

El usuario debe proporcionar:

- periodo;
- datos de planificacion inicial;
- datos de cierre;
- tablas o resumenes exportados si existen.

Si faltan datos obligatorios, no redactes conclusiones fuertes. Indica primero que falta.

## Salida

Informe Markdown estructurado segun la skill.

## Limites

- No modificar archivos.
- No consultar sistemas reales.
- No inventar datos.
- No crear KPIs nuevos.
- No proponer automatizaciones.
- No decidir acciones.
