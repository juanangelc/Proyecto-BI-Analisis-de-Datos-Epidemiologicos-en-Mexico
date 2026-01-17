## 🏗️ Arquitectura del proyecto

El proyecto sigue una arquitectura BI basada en buenas prácticas, donde los datos públicos son primero almacenados en una capa de *staging* antes de ser transformados y consumidos.

### Flujo general de datos

![Arquitectura BI](https://github.com/juanangelc/Proyecto-BI-Analisis-de-Datos-Epidemiologicos-en-Mexico/blob/main/arquitectura_bi.png?raw=true))

**Flujo de trabajo:**
1. Fuentes de datos públicas  
2. Data Lake / Staging (**Azure Blob Storage**)  
3. Orquestación y ETL (**Azure Data Factory**)  
4. Data Warehouse (**Snowflake**)  
5. Modelo dimensional (estrella)  
6. Capa semántica y visualización (**Power BI**)
