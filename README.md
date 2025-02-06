# Flask-Healthcare-Application

# Survey Tool for Income &amp; Expense Analysis
This project is a web-based survey tool developed using Flask, MongoDB, and Python to collect and analyze participants' income and spending habits in preparation for a new healthcare product launch. The data is visualized in Jupyter Notebook, and the web application is deployed on AWS.

# Features
- Web Form (Flask): Collects user details (Age, Gender, Income, Expenses)
- Database (MongoDB): Stores user data securely
- Data Processing (Python & R): Converts collected data to CSV format
- Data Analysis & Visualization: Generates insights from collected data
- Deployment (AWS): Hosted online for accessibility

# Requirements
The following Python packages are required for this project:

- Flask
- pymongo
- pandas
- seaborn
- matplotlib
- jupyter notebooks

# Installation & Setup
## Clone the repository 
   git clone https://github.com/Ruth-Nwawuzoh/Flask-Healthcare-Application.git
   cd survey_tool
   Or download and unzip the zipped file 'survey_tool.zip'

## Set Up a Virtual Environment
-  On Windows (PowerShell):
   python3 -m venv venv
   source venv/bin/activate   # On Windows, use `venv\Scripts\activate`
  
## Install Dependencies
   pip install -r requirements.txt
   
## Set Up MongoDB 
-  Ensure MongoDB is running locally or configure MongoDB Atlas.
-  Update the connection string in app.py:
   client = MongoClient("mongodb://localhost:27017/")

## Run Flask Application
   python app.py
   Open http://127.0.0.1:5000/ in your browser and fill out the survey form.

## Data Processing:
-  The data collected from survey will be stored in MongoDB. 
-  The User class (export_data.py) extracts survey data and    saves it as a CSV:
-  Run the following command to export MongoDB data:
   python export_data.py

## Data Visualization
-  Open the Jupyter notebook:
   jupyter notebook Data_Visualization.ipynb
-  Visualizations include:
1. Ages with highest income
2. Gender distribution across spending categories

## Deployment on AWS EC2
1. Deploy the application using AWS Elastic Beanstalk or EC2.
2. Ensure MongoDB is accessible remotely.
3. Set up environment variables for database connection.
