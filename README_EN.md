## 🏗️ Project Architecture

The project follows a BI architecture aligned with industry best practices, where public data is first stored in a *staging* layer before being transformed and consumed for analytics.

### General Data Flow

![Data Architecture Diagram](https://github.com/juanangelc/Proyecto-BI-Analisis-de-Datos-Epidemiologicos-en-Mexico/blob/main/figures/EN_schema.png?raw=true
)

**Workflow:**
1. Public data sources  
2. Data Lake / Staging (**Azure Blob Storage**)  
3. Orchestration and ETL (**Azure Data Factory**)  
4. Data Warehouse (**Snowflake**)  
5. Dimensional model (star schema)  
6. Semantic layer and visualization (**Power BI**)

---

## 🧱 Data Modeling

A star-schema–based dimensional modeling approach was implemented to optimize analytical performance and metric creation in Power BI.

### Fact Table
- Contains the main records related to cases / healthcare events.
- Centralizes the base metrics used throughout the analysis.

### Dimension Tables
- Geographic dimension (state).
- Supporting lookup tables.
- Derived dimensions created from variables originally spread across multiple columns (e.g., comorbidities).

---

## 🔧 Transformations and Technical Decisions

Several key technical decisions were made during the development of the project, including:
- Normalization of metrics per 100,000 inhabitants to enable fair comparisons across regions.
- Consolidation of comorbidity variables that were originally stored in separate columns.
- Creation of comparative metrics, such as differences in average days of care.
- Focus on interpretable and actionable metrics to support decision-making.

### Dashboard

![Power BI Dashboard](https://github.com/juanangelc/Proyecto-BI-Analisis-de-Datos-Epidemiologicos-en-Mexico/blob/main/figures/EN_states.png?raw=true)

The complete dashboard is available in Power BI.

---

## 📌 Scope and Considerations

This repository documents the architectural and analytical approach of the project.  
No real data, credentials, or internal configurations from enterprise platforms are included.

### Business Impact
This architecture enables scalable analytics, consistent metrics, and efficient dashboard performance.

### Key Learnings
- Designing scalable BI pipelines using cloud-native tools.
- Translating raw public data into business-ready metrics.
