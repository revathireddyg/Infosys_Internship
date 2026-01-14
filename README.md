This project demonstrates a complete data ingestion pipeline for a real-world Customer Support Ticket dataset.
It covers data cleaning, validation, transformation, enrichment, encoding, and normalization, preparing the data for machine learning models and knowledge graph construction.

The dataset contains 8,469 customer support tickets with 17+ attributes.
Each record represents a single customer interaction with the support system.
The data includes:
Customer demographic information
Product details associated with the ticket
Ticket metadata such as type, priority, channel, and status
Unstructured text fields (ticket subject and description)
Response and resolution timestamps
Customer satisfaction ratings
This mix of structured and unstructured data makes it suitable for demonstrating real-world ingestion challenges.


## Table of Contents:
-[Data Ingestion](Data Ingestion)
-


## Data Ingestion
The raw dataset is loaded from a CSV file using Pandas.
Initial exploration is performed using head() and info() to understand the schema, data types, and potential quality issues.
This step establishes a baseline understanding of the data before any transformations are applied.
