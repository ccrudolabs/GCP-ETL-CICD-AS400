# GCP ETL + CI/CD con integración AS/400

Este repositorio contiene una arquitectura completa para replicar y procesar datos provenientes de un sistema IBM AS/400 utilizando servicios nativos de Google Cloud Platform.

---

## 📌 Arquitectura

![Arquitectura](GCP.png)

- **AS/400**: Sistema legado origen de los datos
- **Extraction**: Proceso de extracción vía ODBC, FTP, API u otros conectores
- **Cloud Composer**: Orquestación con Airflow
- **Dataflow**: Transformación y procesamiento de datos
- **BigQuery**: Almacenamiento y análisis de datos
- **Looker**: Visualización y dashboards
- **Cloud Build**: CI/CD para automatizar despliegues
- **GitHub + Terraform**: Infraestructura como código

---

## 🧱 Infraestructura como Código (IaC)

Archivo: `main.tf`

Despliega:
- Composer Environment
- IAM roles
- Configuración regional

```bash
terraform init
terraform apply -var 'project_id=your-project' -var 'region=us-central1'
```

---

## 🚀 CI/CD con Cloud Build

Archivo: `cloudbuild.yaml`

- Copia DAGs a Composer Bucket
- Automatiza actualizaciones

```bash
gcloud builds submit --config=cloudbuild.yaml
```

---

## 🔁 ETL con Airflow + Dataflow

Archivo: `dag_as400_etl.py`

- Define flujo de tareas
- Ejecuta plantilla de Dataflow
- Puede adaptarse para Beam personalizado

---

## 📊 Visualización con Looker

- Explora datasets de BigQuery
- Conecta métricas y tableros
- Controla acceso con IAM y políticas de filas

---

## 📦 Contenido del ZIP

- `main.tf`: Infraestructura en Terraform
- `cloudbuild.yaml`: CI/CD automatizado
- `dag_as400_etl.py`: DAG de ejemplo

---

## 📄 Créditos

Autor: Carlos Crudo  
Organización: CloudSolutionsIoT®  
Sitio: https://cloudsolutionsiot.com

---