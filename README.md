# Retail Data Pipeline

## About
The Retail Data Pipeline is designed to process and transform retail sales data, extracting insights that support business decision-making. This pipeline ingests raw data, performs data quality checks, builds transformation models, and loads the final results into a data warehouse. Data modeling is done using fact and dimension tables to support analytical queries, providing a structured view of retail sales metrics.

### Pipeline Overview
![image](https://github.com/user-attachments/assets/d6ee3280-ada7-4eb0-bc65-5fe10d6d7977)
![Pipeline Diagram](![image](https://github.com/user-attachments/assets/b5967d34-e62d-40b1-a6af-0f8dbbf37e53)

### Data Modeling
![image](https://github.com/user-attachments/assets/e24b1b54-c25f-4935-a9d5-20ab1db0dd0f)

Here are the sources for this project:
- [Data Engineer Project: An end-to-end Airflow data pipeline with BigQuery, dbt Soda, and more!](https://www.youtube.com/watch?v=DzxtCxi4YaA&list=LL&index=2) 
- [Public Retail Project Documentation on Notion](https://robust-dinosaur-2ef.notion.site/PUBLIC-Retail-Project-af398809b643495e851042fa293ffe5b)

## Tools Used
- **Docker**: Containerizes the pipeline for consistent and isolated execution across environments.
- **Astro CLI**: Used to manage and deploy the Airflow workflows that orchestrate the pipeline.
- **Airflow**: Orchestrates the pipeline tasks, managing data flow and dependencies.
- **Soda**: Enables data quality checks throughout the pipeline stages.
- **dbt**: Handles data transformation and modeling, turning raw data into a structured format.
- **Google Cloud Platform (GCP)**: Provides cloud infrastructure for the pipeline.
- **BigQuery**: Data warehouse for storing and querying the transformed data.

## How to Run the Pipeline
- Install Astro CLI by following the instructions [here](https://www.astronomer.io/docs/astro/cli/overview) or by running:
  ```bash
  brew install astro
- Initialize and start Astro Project
  ```bash
  astro dev init
  astro dev start
 - Access the Astro CLI Bash Shell
	```bash 
	astro dev bash
 - Run the pipeline manually (for testing individual tasks):
	```bash 
	airflow tasks test retail <task_name> 2024-01-01
