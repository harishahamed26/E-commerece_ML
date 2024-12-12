# E-commerce project End-to-End Retail Data Pipeline with Apache Airflow, AWS DynamoDB, and Flask


## Description:
This project creates an automated data pipeline to process and analyze online retail transactions using Apache Airflow, DynamoDB, and Flask. The pipeline cleans and processes raw retail data, calculates key performance metrics (such as Recency, Frequency, Monetary (RFM) segmentation), and stores the insights in Amazon DynamoDB. A Flask API is then used to expose the data for further analysis or consumption. The project follows a modular and scalable architecture, making it suitable for real-time analytics applications.

## Flow of the Project:
### Data Ingestion:

Raw retail data (such as transactions from an online store) is loaded into the system.
Data is pre-processed to clean and filter it (remove missing values, handle outliers).
Airflow DAG:

Airflow orchestrates the pipeline.
The DAG (Directed Acyclic Graph) schedules and manages tasks like data cleaning, segmentation, and uploading to DynamoDB.

### Data Processing:

Recency, Frequency, and Monetary (RFM) metrics are calculated.
Customers are segmented based on their purchasing behavior.

### DynamoDB Storage:

The processed insights (Customer segments, Frequency, Monetary, etc.) are stored in Amazon DynamoDB.
Flask API:

A Flask web service is created to expose the results of the analysis.
Users can query the API to get customer segment data.

### Deployment:

The entire pipeline is containerized using Docker for easy deployment.
The solution can be deployed on AWS Elastic Beanstalk for scalability.
