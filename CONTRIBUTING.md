# Contributing

Gracias por colaborar con este blueprint GCP ETL CI/CD AS/400.

## Principios

- Mantener separacion clara entre DEV, QA y PRD.
- No publicar datos reales ni credenciales.
- Documentar decisiones de arquitectura, IAM, costos y operacion.
- Priorizar reproducibilidad y trazabilidad.
- Validar que ejemplos y diagramas no contengan informacion sensible.

## Flujo recomendado

1. Crear una rama descriptiva.
2. Hacer cambios acotados por dominio: infraestructura, DAGs, Dataflow, BigQuery, docs o CI/CD.
3. Documentar pruebas realizadas.
4. Abrir un pull request con impacto, riesgos y rollback.

## Estilo tecnico

- Usar nombres claros para entornos y recursos.
- Incluir etiquetas de FinOps: `env`, `owner`, `project`, `costcenter`.
- Explicar supuestos de red, IAM y datos.
- Citar documentacion oficial cuando se agreguen servicios o patrones nuevos.
