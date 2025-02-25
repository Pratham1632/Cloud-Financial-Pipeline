# Cloud-based Financial Data Pipeline

## Overview
This project implements a cloud-based ETL pipeline for financial transaction data. The pipeline extracts data from a CSV file, transforms it, and loads it into an AWS S3 bucket and a Redshift database. The workflow is orchestrated using Apache Airflow.

## Features
- Extracts financial transaction data from CSV files
- Performs data cleaning and transformation
- Loads transformed data into AWS S3 and Redshift
- Uses Apache Airflow for scheduling and automation
- Implements logging and error handling

## Tech Stack
- **Programming Language:** Python
- **Data Processing:** Pandas, PySpark
- **Cloud Services:** AWS S3, AWS Redshift
- **Orchestration:** Apache Airflow
- **Database:** PostgreSQL (Redshift)

## Project Structure
```
📂 cloud-financial-data-pipeline
│── 📁 data_samples
│   ├── sample_transactions.csv
│── 📁 scripts
│   ├── etl_pipeline.py
│   ├── data_transformation.py
│   ├── aws_integration.py
│   ├── airflow_dag.py
│── README.md
```

## Setup Instructions
### Prerequisites
- Python 3.8+
- AWS account with S3 and Redshift access
- Apache Airflow installed
- Required Python libraries (see `requirements.txt`)

### Installation
1. Clone the repository:
   ```bash
   git clone https://github.com/your-repo/cloud-financial-data-pipeline.git
   cd cloud-financial-data-pipeline
   ```
2. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```
3. Configure AWS credentials:
   ```bash
   aws configure
   ```
4. Set up Airflow:
   ```bash
   airflow db init
   airflow scheduler & airflow webserver
   ```

## Usage
1. Run the ETL pipeline manually:
   ```bash
   python scripts/etl_pipeline.py
   ```
2. Upload transformed data to AWS S3 and Redshift.
3. Schedule and monitor workflows using Airflow.

## Error Handling & Debugging
- Logs are printed for each stage of the ETL process.
- AWS errors are caught and displayed in `aws_integration.py`.
- Temporary files are deleted after upload to S3.
