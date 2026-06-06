# Security Policy

## Alcance

Este repositorio documenta una arquitectura GCP para flujos ETL desde AS/400 con CI/CD, ambientes DEV/QA/PRD, Dataflow, Composer, BigQuery y gobierno operativo.

## Informacion sensible

No se deben publicar:

- credenciales GCP,
- service account keys,
- archivos `.json` con claves,
- datos extraidos de AS/400,
- dumps, backups o muestras con datos reales,
- tokens de CI/CD,
- variables de entorno productivas.

## Buenas practicas

- Usar placeholders en ejemplos.
- Mantener secretos en Secret Manager o mecanismo equivalente.
- Separar configuracion por entorno.
- Versionar infraestructura sin estados Terraform ni credenciales.
- Validar IAM minimo privilegio antes de desplegar.

## Reporte

Reportar vulnerabilidades o exposiciones sensibles de forma privada por LinkedIn:

- https://www.linkedin.com/in/carloscrudo/
