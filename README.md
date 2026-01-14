# AI Based Knowledge Graph Builder

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

## Technologies Used
Python
Pandas & NumPy
Scikit-learn
Regular Expressions
VS Code

## Step 1: Data Ingestion
The raw dataset is loaded from a CSV file using Pandas.
Initial exploration is performed using head() and info() to understand the schema, data types, and potential quality issues.
This step establishes a baseline understanding of the data before any transformations are applied.

## Step 2: Data Validation
To ensure reliability, the data is validated by:
Checking mandatory columns
Removing records with invalid customer age values
Inspecting missing values across all fields
Validation helps prevent incorrect or misleading insights later in the pipeline.

## Step3: Data Cleaning
Cleaning focuses on improving overall data quality:
Missing values are handled logically (e.g., resolution details only apply to closed tickets)
Duplicate records are removed
Fields are prepared for consistent processing
This step ensures that the dataset reflects realistic and usable information.

## Step4: Date & Time Transformation
Several columns contain dates and timestamps stored as strings.
These fields are converted into proper datetime formats to enable:
Time-based analysis
Feature engineering
SLA calculations
This transformation is essential for any operational or performance-related analytics.

## Step5: Feature Engineering
New features are derived from existing data to capture operational insights:
Resolution Time (Hours) is calculated using response and resolution timestamps
Unique identifiers are generated for customers, products, and tickets
Feature engineering bridges the gap between raw data and meaningful analysis.

## Step6: Text Preprocessing
Ticket subject and description fields contain noisy, unstructured text.
To prepare these fields for NLP and analysis:
Text is converted to lowercase
Punctuation and extra whitespace are removed
Content is normalized into a clean format
This step makes textual data machine-readable and analytics-ready.

## Step7: Data Standardization
To ensure consistency across records:
Ticket status, priority, and channel values are standardized
Inconsistent naming and casing issues are resolved
Standardization is critical when combining data from multiple sources or feeding it into models.

## Step8: Data Enrichment
Customer Segment: Categorizes customers based on age groups
SLA Breach Indicator: Flags tickets that exceed a resolution time threshold
Urgency Score: Assigns a severity level based on ticket priority

## Step9: Machine Learning Preparation
The final stage prepares data specifically for machine learning tasks.
Encoding
Categorical variables such as ticket status, priority, channel, and type are label-encoded to convert them into numerical form.
Normalization
Numerical features including customer age, resolution time, and satisfaction rating are normalized using Min-Max scaling to ensure uniform value ranges.
Separate datasets are maintained for:
Semantic / Knowledge Graph use
Machine Learning models


