# Retail Sales Analysis (EDA)

An exploratory data analysis project using Python, pandas and matplotlib. The notebook examines transaction values, product categories, customer demographics and sales patterns over time.

> **Important:** This is a practice project based on a synthetic/fictional dataset. It demonstrates an entry-level EDA workflow; its findings should not be interpreted as insights about a real retailer.

## Project questions

- Is the dataset complete and internally consistent?
- What are the headline sales metrics, and how are transaction amounts distributed?
- How does revenue vary by product category, gender and age group?
- How do sales vary by weekday and month?

## Dataset

- **Source:** [Retail Sales Dataset on Kaggle](https://www.kaggle.com/datasets/mohammadtalib786/retail-sales-dataset) by `mohammadtalib786`.
- **License:** [CC0 1.0 Universal (Public Domain)](https://creativecommons.org/publicdomain/zero/1.0/).
- **Size:** 1,000 transactions and 9 columns.
- **Date range:** January 1, 2023 – January 1, 2024.
- **Fields:** transaction ID, date, customer ID, gender, age, product category, quantity, price per unit and total amount.
- **Data caveats:** the currency is not specified; each customer appears once; the dataset description identifies the data as fictional/synthetic.

The original CSV is included in this repository. The dataset is available under the CC0 1.0 license.

## Tools and methods

- Python
- pandas for loading, validation, aggregation and pivot tables
- matplotlib for charts
- Jupyter Notebook

The notebook includes missing-value and duplicate checks, identifier checks, date parsing, basic range checks, a revenue consistency check (`Total Amount = Quantity × Price per Unit`), descriptive statistics, category and demographic comparisons, and weekday/monthly analysis.

## Key findings

- **1,000 transactions** generated **456,000** in recorded sales. The average transaction amount is **456.00**, while the median is **135.00**. The currency is unspecified.
- Transaction amounts are strongly right-skewed: the 90th percentile is **1,200**, and the maximum is **2,000**.
- Revenue is distributed fairly evenly across Electronics (**34.4%**), Clothing (**34.1%**) and Beauty (**31.5%**).
- Average transaction amounts are nearly identical for female (**456.55**) and male (**455.43**) customers.
- Saturday has the highest recorded weekday revenue (**78,815**). May 2023 is the highest-revenue complete month (**53,150**); September 2023 is the lowest (**23,620**).

These are descriptive patterns in a small synthetic sample, not causal findings. January 2024 contains only two transactions and is excluded from monthly comparisons. Only one year of data is available, so seasonality cannot be assessed.

## Repository structure

```text
retail-sales-analysis/
├── data/
│   └── README.md
├── notebooks/
│   └── 01_initial_exploration.ipynb
├── .gitignore
├── README.md
└── requirements.txt
```

## Run locally

Python 3.10+ is recommended.

```bash
# Create and activate a virtual environment
python -m venv .venv

# Windows PowerShell
.venv\Scripts\Activate.ps1

# macOS / Linux
source .venv/bin/activate

# Install dependencies
python -m pip install -r requirements.txt

# Start Jupyter
jupyter lab
```

Open `notebooks/01_initial_exploration.ipynb` and run **Restart Kernel and Run All Cells**. The notebook expects the CSV at `data/retail_sales_dataset.csv`.

## Limitations and next steps

This is an initial descriptive analysis, not a complete business analysis. The dataset has no product-level details, store/channel information, discounts, specified currency or repeat customers. A useful next project would use a richer real-world dataset and investigate customer retention, product performance or sales forecasting with a clearly defined business question.
