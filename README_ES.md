## 🏗️ Arquitectura del proyecto

El proyecto sigue una arquitectura BI basada en buenas prácticas, donde los datos públicos son primero almacenados en una capa de *staging* antes de ser transformados y consumidos.

### Flujo general de datos

![Arquitectura BI](https://github.com/juanangelc/Proyecto-BI-Analisis-de-Datos-Epidemiologicos-en-Mexico/blob/main/figures/arquitectura_bi%20(1).png?raw=true)

**Flujo de trabajo:**
1. Fuentes de datos públicas  
2. Data Lake / Staging (**Azure Blob Storage**)  
3. Orquestación y ETL (**Azure Data Factory**)  
4. Data Warehouse (**Snowflake**)  
5. Modelo dimensional (estrella)  
6. Capa semántica y visualización (**Power BI**)

## 🧱 Modelado de datos
Se implementó una aproximación a modelo dimensional tipo estrella, con el objetivo de optimizar el análisis y la creación de métricas en Power BI.

### Tabla de hechos
- Contiene los registros principales de atenciones/casos.
- Centraliza las métricas base utilizadas en el análisis.

### Tablas de dimensiones
- Dimensión geográfica (estado).
- Catálogos auxiliares.
- Dimensiones derivadas a partir de variables originalmente distribuidas en múltiples columnas (por ejemplo, comorbilidades).

## 🔧 Transformaciones y decisiones técnicas
Durante el desarrollo del proyecto se tomaron varias decisiones clave, entre ellas:
- Normalización de métricas por cada 100,000 habitantes para permitir comparaciones justas entre entidades.
- Unificación de variables de comorbilidades que originalmente se encontraban en columnas separadas.
- Creación de métricas comparativas, como diferencias de promedios de días de atención.
- Enfoque en métricas interpretables y accionables para la toma de decisiones.

Dashboard completo disponible en Power BI

![Dashboard – Estados](https://github.com/juanangelc/Proyecto-BI-Analisis-de-Datos-Epidemiologicos-en-Mexico/blob/main/estados.png?raw=true)
![Dashboard – Comorbilidades](https://github.com/juanangelc/Proyecto-BI-Analisis-de-Datos-Epidemiologicos-en-Mexico/blob/main/letalidad.png?raw=true)

## 📌 Alcance y consideraciones
Este repositorio documenta el enfoque arquitectónico y analítico del proyecto.  
No se incluyen datos reales, credenciales ni configuraciones internas de plataformas empresariales.

