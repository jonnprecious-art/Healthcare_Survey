# Healthcare_Survey
Healthcare Spending Survey & Analysis Tool
Location: Washington, DC | Project Type: Full-Stack Data Engineering

# Executive Summary
This project is a comprehensive data collection and analysis pipeline developed for a healthcare industry product launch. It features a Flask web application hosted on AWS, a MongoDB cloud backend, and a Jupyter Notebook suite for statistical visualization.

# Technical Architecture
Cloud Hosting: Amazon Web Services (AWS Elastic Beanstalk)
Web Framework: Flask (Python)
Database: MongoDB Atlas (Cloud NoSQL)
Data Processing: Python Object-Oriented Programming (User class)
Analysis: Pandas, Matplotlib, and Seaborn

# Repository Structure
Plaintext
├── application.py          # Flask app (Renamed for AWS compatibility)
├── data_processor.py       # "User" class & MongoDB-to-CSV logic
├── requirements.txt        # System dependencies for AWS deployment
├── templates/
│   └── index.html          # Survey form with dynamic expense fields
├── analysis.ipynb          # Jupyter Notebook for client visualizations
├── Procfile                # AWS deployment instructions
└── README.md               # Project documentation

# Setup & Deployment Instructions
## 1. Local Environment

If running locally, ensure MongoDB is active and install dependencies:

Bash
pip install -r requirements.txt
python application.py
## 2. Database Configuration

This project uses MongoDB Atlas for cloud persistence.

The connection string is managed via environment variables to ensure security.

Data Schema: Age, Gender, Total Income, and an Expenses object (Utilities, Entertainment, School Fees, Shopping, Healthcare).

## 3. AWS Deployment (Elastic Beanstalk)

Zip the project: Compress application.py, templates/, data_processor.py, and requirements.txt.

Upload: Create a new Python application in the AWS Elastic Beanstalk console.

Environment: Set the PYTHONPATH to /var/app/current.

Access: The live survey is accessible via the Elastic Beanstalk environment URL.

## Data Analysis Workflow
Once data is collected via the AWS-hosted form:

Extraction: The data_processor.py script connects to the cloud database, instantiates User objects, and exports the records to survey_results.csv.

Visualization:

Income Analysis: Identifies peak earning years by age group.

Spending Distribution: A segmented analysis of healthcare vs. lifestyle spending across genders.

Client Reporting: Charts are exported in .png format for direct integration into the project's PowerPoint presentation.

## Author
[Precious Donald] R and Python Developer | Data Analytics Graduate Student
