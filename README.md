# n8n Automation Stack

Repositorio de flujos de trabajo avanzados para la gestión de datos y automatización de noticias.

## Workflow 1: FreshRSS to Postgres & Vector DB Bridge
Este flujo automatiza la extracción de artículos favoritos desde una base de datos FreshRSS y su posterior procesamiento.
- **Custom Python Injection**: Consulta optimizada a PostgreSQL usando Python para manejar lógica de favoritos (`is_favorite = 1`).
- **Multi-API Integration**: Soporte para protocolos GReader y Fever.
- **ETL Pipeline**: Extracción, transformación y carga directa en tablas estructuradas de PostgreSQL para posterior análisis.



## Workflow 2: Automated Translator Pipeline
Un pipeline de traducción automática que integra:
- **Python Custom Script**: Extracción de contenido completo (HTML) desde Postgres.
- **Self-Hosted LibreTranslate**: Traducción de artículos de Inglés a Español vía API local.
- **Upsert Logic**: Gestión eficiente de duplicados en la base de datos de destino.


## Workflow 3: Weather Data Intelligence & Normalization (PRIMER FLLUJO CREADO EN N8N)
Sistema de agregación meteorológica multifuente que combina APIs tradicionales y scraping avanzado.
- **LLM-Powered Scraping**: Uso de Firecrawl para extraer datos estructurados de AccuWeather mediante modelos de lenguaje.
- **Data Normalization**: Script en JavaScript para convertir diversas fuentes (OpenWeather, MeteoChile, Scraping) a un esquema de datos único (estándar OWM).
- **Government API Integration**: Consumo de servicios oficiales de climatología con filtrado dinámico.


## Workflow 4: Dynamic Image Metadata Ingestion (INCOMPLETO)
Un flujo interactivo diseñado para asegurar el cumplimiento de derechos de autor en activos visuales.
- **EXIF Analysis**: Extracción automática de metadatos de archivos binarios (JPG/PNG).
- **Dynamic Form Generation**: Uso de JavaScript para evaluar campos faltantes (Autor, Fuente, Licencia) y generar formularios UI en tiempo real solo cuando es necesario.
- **Smart Conditional Logic**: Bifurcación de flujos basada en la integridad de los datos de entrada.
