# azure-kimball-synthetic-pipeline
```markdown
# Azure Kimball Synthetic Pipeline

This project demonstrates an end-to-end Azure-native implementation of a Kimball-modeled data analytics pipeline for anti-trafficking intelligence, using synthetic data.

## Overview

This repository showcases a fully orchestrated solution built with Microsoft Azure tools, aligning with the following phases:

1. **Dimensional Modeling (Kimball Method)**  
   - Defined business processes and facts (e.g., incidents, hotline calls, online ads)  
   - Identified dimensions (e.g., victims, traffickers, locations)  
   - Built star schema and a reusable bus matrix

2. **Synthetic Data Generation**  
   - Python scripts using OpenAI for structured, realistic mock data  
   - Entities include: `Victim`, `Trafficker`, `Incident`, `Ad`, `HotlineCall`, and `Location`  
   - Ensures privacy-safe, reproducible datasets aligned with the dimensional blueprint

3. **Azure Lakehouse Pipeline (Bronze, Silver, Gold Layers)**  
   - Ingestion via Azure Data Factory  
   - Data stored in Azure Data Lake Gen2  
   - Transformation handled in Azure Synapse using T-SQL pipelines

4. **Power BI Semantic Model & Dashboarding**  
   - Model includes relationships and reusable DAX measures  
   - Visuals: heatmaps, network graphs, Sankey flows, risk scorecards, and more  
   - Agency-friendly design with accessibility and interpretability in focus

## Tools & Services Used

- **Azure Data Factory** – Orchestration and pipeline automation  
- **Azure Synapse Analytics** – Data transformation and modeling  
- **Azure Data Lake Gen2** – Unified storage for all layers  
- **Azure OpenAI + Python** – Synthetic data generation  
- **Power BI** – Semantic layer and interactive dashboards  

## Folder Structure

```

azure-kimball-synthetic-pipeline/

├── data\_generation/         # Python scripts to generate synthetic datasets

├── modeling/                # Star schema, bus matrix, dimension/fact definitions

├── lakehouse\_pipeline/      # Scripts for Bronze → Silver → Gold transformations

├── powerbi/                 # PBIX files and DAX model logic

├── docs/                    # Supporting documentation

````

## Getting Started

1. Clone the repo  
   ```bash
   git clone https://github.com/your-username/azure-kimball-synthetic-pipeline.git
````

2. Set up your environment

   * Configure Azure credentials
   * Install dependencies listed in `data_generation/requirements.txt`

3. Run synthetic data generation

   ```bash
   python data_generation/generate_data.py
   ```

4. Use the modeling outputs to build your Lakehouse and Power BI visuals.

## Author

**Umair Sajid** – Senior Data & AI Consultant
📧 [umaiesajid@gmail.com](mailto:umaiesajid@gmail.com)

```
