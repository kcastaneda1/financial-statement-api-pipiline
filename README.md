# Financial Statement API Pipeline

## Overview

This project demonstrates a Python-based data pipeline for extracting, transforming, and analyzing financial statement data using the Alpha Vantage API.

It is designed to replicate a simplified **equity research workflow**, where raw financial data is programmatically ingested, structured, and prepared for downstream analysis such as financial modeling and valuation.

---

## Features

* Retrieve **Income Statement, Balance Sheet, and Cash Flow** data via API
* Secure API key management using environment variables
* Transform nested JSON responses into structured datasets
* Convert financial data into **pandas DataFrames** for analysis
* Modular design for scalability and future financial modeling integration

---

## Tech Stack

* Python 3.10
* requests
* pandas
* numpy
* json
* openpyxl
* reduce
* python-dotenv

---

## Installation

1. Clone the repository:

```
git clone https://github.com/kcastaneda1/financial-statement-api-pipeline.git
```

2. Navigate into the project directory:

```
cd financial-statement-api-pipeline
```

3. Install dependencies:

```
pip install -r requirements.txt
```

---

## Environment Setup

Create a `.env` file in the root directory and add your Alpha Vantage API key:

```
ALPHAVANTAGE_API_KEY=your_api_key_here
```

> Note: The `.env` file is excluded from version control via `.gitignore` to ensure sensitive credentials are not exposed.

---

## Usage

Run the main script:

```
python src/main.py
```

You can modify the ticker symbol within the script to retrieve financial data for different companies.

---

## Example Output

Sample (truncated) response from the API:

```
{
  "symbol": "AAPL",
  "annualReports": [
    {
      "fiscalDateEnding": "2024-09-30",
      "totalRevenue": "394328000000",
      "netIncome": "99803000000"
    }
  ]
}
```

After processing, the data can be structured into a pandas DataFrame for further analysis.

---

## Project Structure

```
alphavantage-financial-api/
│
├── src/
│   └── main.py
│
├── .env
├── .gitignore
├── requirements.txt
├── README.md
```

---

## Future Improvements

* Implement financial ratio calculations (ROE, ROA, margins)
* Add discounted cash flow (DCF) valuation model
* Build automated multi-company comparison tools
* Integrate data visualization (matplotlib / dashboards)
* Expand support for additional financial data providers

---

## Motivation

This project was developed to strengthen practical skills at the intersection of **data analytics and equity research**.

It reflects an effort to move beyond manual analysis by building programmatic workflows for financial data extraction and transformation—key capabilities in modern investment research and financial analysis roles.

---

## Disclaimer

This project is for educational and informational purposes only and does not constitute financial advice.
