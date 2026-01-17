# Proyecto-BI-Analisis-de-Datos-Epidemiologicos-en-Mexico

El proyecto sigue una arquitectura BI basada en buenas prácticas, donde los datos públicos son primero almacenados en una capa de staging antes de ser transformados y consumidos.

Fuentes de datos públicas
        ↓
Data Lake / Staging (Azure Blob Storage)
        ↓
Orquestación y ETL (Azure Data Factory)
        ↓
Data Warehouse (Snowflake)
        ↓
Modelo dimensional (estrella)
        ↓
Capa semántica y visualización (Power BI)
