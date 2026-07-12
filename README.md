# Rickmore Retail Big Data Architecture

A big data and business intelligence architecture proposal for **Rickmore Retail**, a Canadian omnichannel retailer. The project addresses fragmented data, limited historical reporting, and the absence of real-time and predictive analytics by proposing a scalable **Lambda Architecture** built with Azure, Kafka, Spark, and Power BI.

## Project Overview

Rickmore Retail operates physical stores and an e-commerce platform but lacks a unified analytics environment. This project proposes an end-to-end architecture that integrates internal sales data, e-commerce activity, and social media sentiment to support real-time reporting, historical analysis, business intelligence, and advanced analytics.

## Business Problems Addressed

- Fragmented operational, e-commerce, and social media data
- Limited real-time visibility into customer and sales activity
- Lack of predictive analytics capabilities
- Inconsistent data governance and master data management
- Need for scalable, cost-conscious data processing

## Proposed Solution

The solution uses a **Lambda Architecture** with three main layers:

1. **Batch Layer** — processes historical sales and demographic data for accurate long-term analysis.
2. **Speed Layer** — processes real-time data such as clickstreams and social media sentiment.
3. **Serving Layer** — combines batch and streaming outputs for dashboards, reports, and ad-hoc analysis.

## Architecture Components

| Component | Recommended Tools | Purpose |
|---|---|---|
| Data Ingestion | Apache Kafka, Azure Data Factory | Real-time streaming and scheduled batch ingestion |
| Data Storage | Azure Data Lake | Scalable storage for structured, semi-structured, and unstructured data |
| Data Processing | Apache Spark, Spark Streaming | Batch transformation and real-time processing |
| Orchestration | Azure Synapse Pipelines | Pipeline scheduling and workflow coordination |
| Analytics and BI | Power BI | KPI dashboards, reports, drill-down analysis, and forecasting |
| Governance | Microsoft Purview | Metadata management, data lineage, discovery, and compliance |

## Data Model

The proposed star schema contains:

- **FactSales** — total sales, e-commerce sales, in-store sales, and e-commerce share
- **DimCategory** — product category and NAICS classification
- **DimMonth** — month, month name, and year attributes

This model supports efficient slicing, filtering, trend analysis, and KPI reporting in Power BI.

## Key Analytics and Visualizations

The Power BI analysis explores:

- E-commerce sales growth by product category
- E-commerce versus in-store sales distribution
- Annual e-commerce sales and share trends
- Category-level e-commerce adoption
- Total sales by year and category
- Decomposition of sales by category, sales channel, and time

### Main Findings

- Electronics and furniture show strong e-commerce adoption and sustained growth.
- Grocery and automotive remain heavily dependent on in-store sales.
- High-growth online categories require continued investment in digital infrastructure.
- Low-adoption categories may face logistical or customer-behaviour barriers.

## Implementation Roadmap

| Phase | Timeline | Activities |
|---|---|---|
| Foundation | Weeks 1–2 | Define architecture and load historical data |
| Ingestion and Storage | Weeks 3–4 | Build pipelines and deploy the storage layer |
| Real-Time and BI | Weeks 5–6 | Integrate streaming data and develop dashboards |
| Optimization | Week 7 | Test, tune, and refine the solution |
| Delivery | Week 8 | Present the solution and complete handoff |

## Repository Structure

```text
rickmore-retail-big-data-project/
├── README.md
├── presentation/
│   └── Rickmore_Retail_Big_Data_Architecture.pptx
├── docs/
│   └── project-summary.md
├── assets/
└── .gitignore
```

## Technologies

- Power BI
- Apache Kafka
- Apache Spark
- Azure Data Factory
- Azure Data Lake
- Azure Synapse Analytics
- Microsoft Purview
- Star Schema Modeling
- Lambda Architecture

## Team

- Nitigya Vasudev
- Sakshi Salvi
- Umang Sehgal
- Prince Chaudhary
- Mitali Sharma

## Academic Context

- **Course:** INFO8116 – Big Data Architecture
- **Institution:** Conestoga College
- **Term:** Summer 2025


## 📄 Project Report

[View Project Report](./Rickmore_Retail_Big_Data_Architecture.pdf)

## References

- Statistics Canada Tables 20-10-0067-01 and 20-10-0056-03
- Microsoft Azure documentation
- Apache Kafka documentation
- Apache Spark documentation
- Microsoft Power BI documentation
- Course materials for INFO8116

## Note

This repository presents an academic architecture proposal. The architecture was designed conceptually and should not be represented as a production deployment unless implementation files, source code, datasets, or deployment evidence are added later.
