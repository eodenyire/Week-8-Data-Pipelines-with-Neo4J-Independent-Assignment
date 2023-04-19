# Week-8-Data-Pipelines-with-Neo4J-Independent-Assignment
Week 8 Data Pipelines with Neo4J Independent Assignment

###Data Pipeline with Neo4j and Postgres<br>
This project is a data pipeline that extracts data from a Neo4j graph database, transforms it using Pandas, and loads it into a Postgres relational database. The pipeline is implemented in Python and uses the neo4j, pandas, and psycopg2 libraries for connecting to Neo4j, data manipulation, and connecting to Postgres, respectively.<br>
The pipeline is designed for a telecommunications company that wants to optimize their business processes.<br>

### Prerequisites
To run this data pipeline, you will need the following:<br>
i.	A Google account<br>
ii.	Access to Google Colab<br>
iii.	A Neo4j Aura account<br>
iv.	A Postgres database on Google Cloud<br>

You will also need to install the following Python libraries: <br>
i.	neo4j<br>
ii.	pandas<br>
iii.	psycopg2<br>

You can install these libraries using pip: <br>
i.	pip install neo4j pandas psycopg2<br>

## Project Structure
The project structure is as follows:<br>
       - data_pipeline.ipynb<br>
       - README.md<br>
The data_pipeline.ipynb file contains the Python code for the data pipeline, while the README.md file is this file that you are reading right now.<br>

## Setup<br>
## 1.	Neo4j <br>
The Neo4j database used in this project is hosted on Neo4j Aura, a cloud-based Neo4j service. To use this service, you will need to sign up for an account and create a new database instance. Once you have created an instance, you will need to obtain the instance URI and credentials (username and password). These details should be stored in the neo4j_uri, neo4j_user, and neo4j_password variables in the data_pipeline.ipynb file.<br>
i.	To set up the Neo4j connection, you will need to do the following:<br>
ii.	Create a new Neo4j Aura database.<br>
iii.	Connect to the Neo4j Aura database using the Neo4j Browser.<br>
iv.	In the Neo4j Browser, create the necessary nodes and relationships to represent the telecommunications data.<br>
v.	Update the neo4j_uri, neo4j_user, and neo4j_password variables in the telecom_data_pipeline.py file to match your Neo4j Aura credentials.<br>

## 2.	Postgres <br>
The Postgres database used in this project is hosted on Google Cloud SQL. To use this service, you will need to create a new instance and database. Once you have created an instance and database, you will need to obtain the instance IP address, database name, username, and password. These details should be stored in the pg_host, pg_database, pg_user, and pg_password variables in the data_pipeline.ipynb file.<br>
To set up the Postgres connection, you will need to do the following:<br>
i.	Create a new Postgres database on Google Cloud.<br>
ii.	Create a new Compute Engine instance on Google Cloud to run the Postgres database.<br>
iii.	In the Compute Engine instance, install Postgres and create a new user with the necessary permissions to access the database.<br>
iv.	Update the pg_host, pg_database, pg_user, and pg_password variables in the telecom_data_pipeline.py file to match your Postgres credentials.<br>

## Python Libraries
To run the data pipeline, you will need to install the neo4j, pandas, and psycopg2 libraries. You can install these libraries using the following commands:<br>
!pip install neo4j pandas psycopg2 <br>

## Running the Pipeline <br>
To run the data pipeline, you can simply open the data_pipeline.ipynb file in Google Colab and run each cell in order. <br>

The pipeline consists of the following steps:<br>
i.	Extracting data from Neo4j: The extract_data function uses the neo4j library to connect to the Neo4j database and extract data using a Cypher query.<br>
ii.	Transforming data using Pandas: The transform_data function takes the extracted data and performs data cleaning and manipulation using the pandas library.<br>
iii.	Loading data into Postgres: The load_data function takes the transformed data and loads it into the Postgres database using the psycopg2 library.<br>
The transformed data will be loaded into the Postgres database. <br>

## Data Schema <br>
The data schema used in this project consists of a single table named telecom_data with the following fields:<br>
i.	customer_id (integer): The unique identifier of the customer.<br>
ii.	subscription_id (integer): The unique identifier of the subscription.<br>
iii.	service_id (integer): The unique identifier of the service.<br>
iv.	start_date (date): The start date of the subscription.<br>
v.	end_date (date): The end date of the subscription.<br>
vi.	price (float): The price of the subscription.<br>

## Data Transformations <br>
The transform_data function performs the following transformations on the extracted data:<br>
i.	Converts date fields to datetime objects using the pd.to_datetime function.<br>
ii.	Removes null values using the dropna function.<br>

## Conclusion<br>
This data pipeline project demonstrates how to extract data from a Neo4j graph database, transform it using Pandas, and load it into a PostgreSQL database. The project provides a template that can be adapted for various use cases that require data extraction from a graph database and loading into a relational database for easier querying and analysis. The README file provides clear instructions on how to set up and run the data pipeline, and it also explains the data schema and the transformations performed on the data.<br>

With the availability of cloud services like Neo4j Aura and Google Cloud Compute Engine, it has become easier to implement this kind of project without the need for on-premise infrastructure. The code can be modified and extended to handle larger datasets, and additional features can be added to make it more robust and scalable. 
The project serves as a useful reference for anyone looking to extract data from a graph database like Neo4j and load it into a relational database like PostgreSQL.
By following the setup and running instructions, you can quickly and easily deploy the pipeline to your own environment.<br>

