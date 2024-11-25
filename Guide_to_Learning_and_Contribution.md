1. 🎓 An Apache Airflow DAG and a Python script for automating data extraction and preprocessing from the BBC News website are included in this repository. An outline of the process and the difficulties experienced during implementation can be found below.


Overview of Workflow
Data Extraction: The script scrapes headlines and descriptions from the BBC News homepage using BeautifulSoup and libraries.

Preprocessing of Text: The captured text data is cleaned and formatted with the use of the preprocess_text function.

Data Storage and Version Control: Data Version Control (DVC) is used to track versions and guarantee reproducibility, and preprocessed data is saved in a CSV file.

Development of an Apache Airflow DAG: To automate the daily data extraction and preprocessing operations, an Airflow DAG called bbc_news_dag is constructed.

Difficulties with Installing Apache Airflow: Compatibility problems and system dependencies made installing Apache Airflow using Docker difficult.
DVC Push Problem: Perhaps as a result of synchronization problems with the Google account, a problem occurred when pushing data to the distant DVC repository.
Upkeep of Repositories
This README file contains thorough descriptions of the assignment that are kept up to date in the GitHub repository.

Use
Use these steps to execute the data preparation workflow:

Use pip install -r requirements.txt to install the necessary libraries.
Run the fetch_and_preprocess_data.py Python script.
To automate the process, you can import the bbc_news_dag.py file and optionally set up Apache Airflow.
In conclusion
Notwithstanding difficulties with DVC push issues and Apache Airflow installation, the deployment effectively automates the data extraction and preparation from the website for BBC News. The data workflow's reproducibility and version control are guaranteed by the DVC integration.


2. 🌐 Contribution Objectives Production of Content Write Blog Posts: I have written blogs about DevOps tools on Medium, which have aided in my exploration and education.

