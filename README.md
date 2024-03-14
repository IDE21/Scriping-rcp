# Scriping-rcp

# Raymond Weil Watch Scraper Project

This project extracts detailed product information for watches from the official Raymond Weil website.

Project Structure:

*   scriping-rcp.py:  A Python script for scraping the watch data and storing it in a CSV file.
*   scriping-rcp.ipynb: A Jupyter Notebook version of the scraping script for interactive exploration and potential modifications.
*   shell_script.sh (Optional): A shell script to automate execution of the Python script and provide error handling. 

Dependencies:

*   Python 3 
*   Requests
*   BeautifulSoup4
*   csv
*   [Jupyter Notebook (for using scriping-rcp.ipynb)](https://jupyter.org/)

Installation

1.  Clone this repository:
        git clone [invalid URL removed]
    

2.  Install dependencies:
        cd raymond-weil-scraper
    pip install requests beautifulsoup4 csv 
    

Usage:

Python Script

1.  Execute the script:
        python3 scriping-rcp.py
    
2.  The extracted watch data will be saved in scriping-result.csv. 

Jupyter Notebook

1.  Launch Jupyter Notebook:
        jupyter notebook
    
2.  Open scriping-rcp.ipynb and run the cells to scrape the data.

Shell Script (Optional)

1.  Make the shell script executable:
        chmod +x shell_script.sh
    
2.  Run the script:
        ./shell_script.sh
    

Data Description (scriping-result.csv)

The CSV file contains the following columns:

*   Reference_Number
*   watch_URL
*   type
*   brand
*   .... (other extracted watch attributes)

Additional Notes:

*   The code handles the website's cookie consent banner.
*   Consider adding more robust error handling for real-world deployment.

Example Code Snippet (from scriping-rcp.py):

python
import requests
from bs4 import BeautifulSoup
# ... other imports

def get_product_details(product_url):
    response = requests.get(product_url, headers=headers)
    # ... code to extract product details

Last file I uploaded is a csv file (The result of the project).
