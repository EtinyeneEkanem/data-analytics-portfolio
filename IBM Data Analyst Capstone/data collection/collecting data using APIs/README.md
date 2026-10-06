# Collecting Job Data Using APIs
### Project Overview
This project is part of the IBM Data Analyst Capstone Project.It demonstrates how to collect and analyze job-posting information through an API using Python.

The main objective is to determine the number of job postings available for different **technologies** across selected **US locations**. The collected results are then organized into an Excel spreadsheet for further analysis and visualization.


### Project Objective
The project uses a Jobs API to answer questions such as:

• How many job postings are available for a particular technology?

• How many job postings are available in a particular location?

• How does demand for different technologies vary across locations?

The analysis focuses on the following locations:

• Los Angeles

• New York

• San Francisco

• Washington DC

• Seattle

• Austin

• Detroit

The following technologies are evaluated:

• C

• C#

• C++

• Java

• JavaScript

• Python

• Scala

• Oracle

• SQL Server

• MySQL Server

• PostgreSQL

• MongoDB


### Dataset
The original dataset used for this IBM lab comes from the Jobs on Naukri.com
dataset published by PromptCloud on Kaggle. 

For the IBM exercise, a modified subset of the original dataset is provided
through the IBM Skills Network environment. The original CSV data was
converted to JSON so that it could be accessed through the Jobs API.

The dataset contains fields including:

• Job Title

• Job Experience Required

• Key Skills

• Role Category

• Location

• Functional Area

• Industry

• Role

The project therefore does not query a live commercial job board directly.
Instead, the IBM-provided Jobs API serves the supplied job dataset through a
local Flask application.


### API
The Jobs API runs locally at:

http://127.0.0.1:5000/data

The API accepts query parameters such as:

Key Skills

Location

For example, the notebook sends a request for jobs requiring Python:

payload = {**"Key Skills"**: **"Python"**}

response = requests.get(api_url, params=payload)

data = response.json()

number_of_jobs = len(data)

The same approach is used to search for jobs by location.


### How It Works
The project follows this workflow:

IBM Jobs Dataset
  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;  &#8595;  
  
JSON Data

   
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;  &#8595;
       
Flask Jobs API

   
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;  &#8595;
       
Python Requests

   
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;  &#8595;
       
Filter by Technology / Location

   
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;  &#8595;
       
Count Job Postings

    
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; &#8595;
       
Excel Spreadsheet     
       
### Technologies Used

• Python — programming language

• Requests — making HTTP API requests

• Pandas — data manipulation and DataFrame creation

• JSON — API data format

• OpenPyXL — creating and working with Excel workbooks

• Jupyter Notebook — development and execution environment

• Flask — local API used by the IBM Jobs API notebook

### Project Contributions
#### Feature Extension: In-Notebook Results Verification
**Contributed by:** Etinyene Ekanem

Added an in-notebook verification feature to validate job data collected through the API. Using **Pandas**, the collected results are transformed into DataFrames that display the number of job postings by location and technology.

An additional **location-by-technology matrix** was created to show and compare the number of job postings for each technology across different locations. This provides a quick visual validation of the API results and complements the required Excel file generation, making it easier to verify and analyze the collected job data directly within the Jupyter Notebook.

### Project Files
The main notebook is:

**Collecting Jobs Data Using APIs.ipynb**

The generated Excel output is:

**job-postings.xlsx**

**technology_job_postings.xlsx**

The repository also contains the other notebooks and datasets used
throughout the wider IBM Capstone Project.

### Running the Project
1. Install Python
Python 3.x is recommended.
2. Install the required packages
pip install -r requirements.txt
3. Start the Jobs API
   
The IBM-provided Jobs_API.ipynb notebook contains the Flask application
required to serve the job data.

Run all cells in the Jobs API notebook before running the main notebook.
The API should become available at:
http://127.0.0.1:5000/data

4. Open the main notebook
   
Open: 

             Collecting Jobs Data Using APIs.ipynb
             
Run the notebook cells to:

1. Connect to the Jobs API.
2. Query job postings by technology.
3. Query job postings by location.
4. Count the returned job records.
5. Compare technologies across locations.
6. Store the results in an Excel spreadsheet.

### Example API Query
The following example retrieves job postings requiring Python:

**import requests**

api_url = "http://127.0.0.1:5000/data"

payload = {"Key Skills": "Python"}

response = requests.get(api_url, params=payload)

if response.ok:

    data = response.json()
    
    number_of_jobs = len(data)
    
print(number_of_jobs)

The notebook also demonstrates filtering by location:

payload = {"Location": "Los Angeles"}

response = requests.get(api_url, params=payload)

if response.ok:

    data = response.json()
    
    number_of_jobs = len(data)

### Output
The final results are saved to excel spreadsheet as:

⦁	**job-postings.xlsx**

⦁	**technology_job_postings.xlsx**

### Key Learning Outcomes
This project demonstrates practical experience with:

• Working with REST APIs

• Sending HTTP GET requests

• Passing query parameters to an API

• Processing JSON responses

• Counting records returned by an API

• Using Python for data collection

• Using Pandas for data manipulation

• Exporting data to Excel

• Preparing data for subsequent analysis and visualization

### Data Source
The IBM lab identifies the original dataset as Jobs on Naukri.com, published by
PromptCloud on Kaggle. The lab uses a modified subset of that dataset
supplied through IBM Skills Network.

For reproducibility, use the dataset and Jobs API files provided with the IBM
course rather than attempting to substitute the complete original dataset.

### Project Context
This notebook represents the data-collection stage of the IBM Data Analyst Capstone Project. The resulting job-posting data can subsequently be used for exploratory analysis, visualization, and dashboard development.

### Acknowledgements
This project is based on the IBM Skills Network Data Analyst Capstone Project materials.

Original job data source:

**PromptCloud — Jobs on Naukri.com**

IBM Skills Network provides the modified dataset and API environment used in the exercise.

### Author

Etinyene Ekanem

IBM Data Analyst Capstone Project. 
