# n8n Automation Stack

Repositorio de flujos de trabajo avanzados para la gestión de datos y automatización de noticias.

## Workflow 1: FreshRSS to Postgres & Vector DB Bridge
Este flujo automatiza la extracción de artículos favoritos desde una base de datos FreshRSS y su posterior procesamiento.

### Características Técnicas:
- **Custom Python Injection**: Consulta optimizada a PostgreSQL usando Python para manejar lógica de favoritos (`is_favorite = 1`).
- **Multi-API Integration**: Soporte para protocolos GReader y Fever.
- **ETL Pipeline**: Extracción, transformación y carga directa en tablas estructuradas de PostgreSQL para posterior análisis.



## Workflow 2: Automated Translator Pipeline
Un pipeline de traducción automática que integra:
- **Python Custom Script**: Extracción de contenido completo (HTML) desde Postgres.
- **Self-Hosted LibreTranslate**: Traducción de artículos de Inglés a Español vía API local.
- **Upsert Logic**: Gestión eficiente de duplicados en la base de datos de destino.



