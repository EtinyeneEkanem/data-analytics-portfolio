## Web Scraping with Python
## Project Overview
This project is part of the IBM Data Analyst Professional Certificate Capstone Project. It demonstrates how to extract structured information from an HTML webpage using Python, store the extracted data in a dictionary, convert the dictionary into a Pandas DataFrame, and export the resulting dataset to a CSV file.

The project uses IBM Skills Network's Programming Languages webpage to collect information about programming languages and their average annual salaries. This exercise demonstrates a fundamental data analytics workflow: extracting, structuring, and storing web-based data for further analysis.

 ## Objectives
⦁	Retrieve webpage content using Python's requests library.

⦁	Parse HTML content using BeautifulSoup.

⦁	Extract programming language names from the second table column and average annual salaries from the fourth table column.

⦁	Store the extracted information in a Python dictionary.

⦁	Convert the dictionary into a Pandas DataFrame.

⦁	Export the DataFrame to a CSV file for further analysis and reporting.

### Data Source
Source: IBM Skills Network — Programming Languages

URL: https://cf-courses-data.s3.us.cloud-object-storage.appdomain.cloud/IBM-DA0321EN-SkillsNetwork/labs/datasets/Programming_Languages.html

The webpage provides programming language information used in the IBM web scraping lab. The extraction focuses on the programming language name and average annual salary.

### Tools and Technologies
| **Tool** | **Purpose** | 
| -------- | -------- |                             
|Python	   |  Data extraction and processing|
|Requests	 |  Download webpage HTML|
|BeautifulSoup	| Parse HTML and extract table data|
|Pandas	 |  Convert dictionary data into a DataFrame|
|CSV	   |     Store the extracted data|
|Jupyter Notebook |	Develop and document the workflow|

 ### Methodology
The project follows these steps:
1. **Import libraries:** Import requests, BeautifulSoup, and pandas.
2. **Retrieve webpage content:** Send an HTTP request to the source URL and obtain the HTML response.
3. **Parse HTML:** Create a BeautifulSoup object to navigate the webpage structure.
4. **Locate the table:** Identify the relevant HTML table containing the required information.
5. **Extract columns:** Iterate through the table rows and extract the programming language name from the second column and the average annual salary from the fourth column.
6. **Create a dictionary:** Store the extracted values under descriptive keys.
7. **Create a DataFrame:** Convert the dictionary into a structured Pandas DataFrame.
8. **Export to CSV:** Save the DataFrame as popular-languages.csv for future use.

### Implementation
The web-scraping process was implemented in the Jupyter Notebook **web_scraping.ipynb**. The notebook covers extracting data from the second and fourth columns of the target HTML table, storing the extracted values in a Python dictionary, converting the dictionary into a Pandas DataFrame, and exporting the resulting dataset to a CSV file.

For the complete Python code and execution results, see **web_scraping.ipynb**.

### Output
The project generates a CSV file named:

**popular-languages.csv**

The resulting DataFrame contains two columns:

| **Column**	        |       **Description**|
|---------------------|-----------------------|
|Language	            |       Name of the programming language|
|Average Annual Salary |	  Average annual salary associated with the language, as displayed on the webpage|

The CSV file can be opened in Microsoft Excel, loaded into Python, or imported into other data analysis tools.

### Project Structure
ibm-web-scraping-capstone/

│

├── README.md

├── web_scraping.ipynb

├── popular-languages.csv

└── requirements.txt

### How to Run the Project
1. Clone or download the repository.
2. Navigate to the project directory.
3. Install the required dependencies.
4. Open web_scraping.ipynb in Jupyter Notebook or JupyterLab.
5. Run the notebook cells in sequence.
6. Verify that popular-languages.csv has been created in the working directory.

### Skills Demonstrated
⦁	Web scraping with Python

⦁	HTML parsing and table extraction

⦁	HTTP requests and response validation

⦁	Python dictionaries and list manipulation

⦁	Data structuring with Pandas

⦁	CSV export and file handling

⦁	Data collection and preparation

⦁	Reproducible analytical workflows

### Acknowledgment
This project was completed as part of the IBM Data Analyst Professional Certificate learning pathway and uses the programming languages webpage provided by IBM Skills Network.

**Author:** [Etinyene Ekanem]

**Project:** IBM Data Analyst Capstone — Web Scraping

**Technologies:** Python, Requests, BeautifulSoup, Pandas

.............................................................................................................................................................................

*This project demonstrates how raw information from an HTML webpage can be transformed into a structured dataset ready for downstream data analysis*.
