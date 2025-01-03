# Company Scraper

## Overview

**Company Scraper** is a Jupyter Notebook designed to extract detailed information about companies listed on the [Fatturato Italia](https://www.fatturatoitalia.it/) website, specifically within the Friuli-Venezia Giulia region. The notebook navigates through multiple pages of company listings, collects individual company links, and extracts relevant data, consolidating it into a CSV file for easy analysis.

## Features

- **Automated Link Collection:** Iterates through 1,046 pages to gather links to individual company profiles.
- **Data Extraction:** Retrieves company name, address, city, province, and VAT number from each profile.
- **Rate Limiting:** Implements a 20-second delay between requests to prevent server overload.
- **Error Handling:** Handles HTTP request exceptions.
- **Data Consolidation:** Compiles all extracted data into a single CSV file.

## Prerequisites

- **Python 3.7 or higher**
- **Jupyter Notebook**
- **Python Libraries:**
  - `requests`
  - `pandas`
  - `beautifulsoup4`

## Installation

### Clone the Repository

```bash
git clone https://github.com/yourusername/company-scraper.git
cd company-scraper
```

### Create a Virtual Environment (Optional)

```bash
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
```

### Install Dependencies

```bash
pip install -r requirements.txt
```

*If you don't have a `requirements.txt`, install directly:*

```bash
pip install requests pandas beautifulsoup4
```

### Install Jupyter Notebook (If Not Already Installed)

```bash
pip install jupyter
```

## Usage

### Launch Jupyter Notebook

Navigate to the project directory and start Jupyter Notebook:

```bash
jupyter notebook
```

### Open the Notebook

In the Jupyter interface, open `company-scraper.ipynb`.

### Run the Notebook

- Execute each cell sequentially by selecting the cell and pressing `Shift + Enter`.
- Monitor the output directly within the notebook cells.
- The notebook will print each URL it processes and display extracted company information.

### Output

- Data is saved to `companies_batch_0_100.csv` in the project directory upon completion.


### Collect Company Links

- Iterates through 1,046 pages of company listings.
- Extracts links from the first column of each table on the page.
- Stores all links in a Pandas DataFrame.

### Extract Company Information

- Visits each collected link.
- Extracts:
  - Company Name
  - Address
  - City
  - Province
  - VAT Number
- Stores the data in a Pandas DataFrame.

### Save Data

- Concatenates all DataFrames into a single DataFrame.
- Exports the data to `companies_batch_0_100.csv`.

## Customization

### Adjusting Delay Between Requests

Modify the `time.sleep(20)` line in the notebook to change the delay duration.

### Changing Output Filename

Update the filename in the `to_csv` method to prevent overwriting existing files.


## License

This project is licensed under the MIT License.


**Disclaimer:** Use this notebook responsibly. Unauthorized scraping can lead to legal consequences or IP blocking.
