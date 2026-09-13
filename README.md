# Exploratory Data Analysis on Retail Data (Python)

Coursera-style portfolio project: exploratory data analysis on the **UCI Online Retail** dataset (UK-based online gift store transactions, 2010–2011). The notebook cleans the data, explores sales and customer behavior, and summarizes business-oriented findings.

## What’s in the repo

| File | Description |
|------|-------------|
| `online_retail.ipynb` | Full EDA notebook with charts and narrative |
| `online_retail.py` | Colab export of the notebook |
| `Online Retail.xlsx` | Dataset used by the analysis |

## Dataset columns

| Column | Meaning |
|--------|---------|
| `InvoiceNo` | Invoice / transaction id |
| `StockCode` | Product code |
| `Description` | Product name |
| `Quantity` | Units on the line |
| `InvoiceDate` | Timestamp |
| `UnitPrice` | Price per unit |
| `CustomerID` | Customer id |
| `Country` | Customer country |

## Analysis steps

1. **Load & inspect** — shape, head/tail, dtypes, missing values  
2. **Clean** — drop duplicates, keep positive unit prices, handle missing customer ids, tag completed vs returned-style rows  
3. **Feature helpers** — revenue (`Quantity × UnitPrice`), month, weekday, hour  
4. **Visualize** — country activity, top customers, top products, monthly / weekday / hourly order and revenue patterns  
5. **Outliers** — z-score style checks on quantity / price / revenue  
6. **Conclusions** — practical notes on valuing top customers, stocking popular products, and timing campaigns  

## Tech stack

Python, Pandas, NumPy, Matplotlib, Seaborn, SciPy, tabulate, Jupyter / openpyxl

## How to run

```bash
git clone https://github.com/mahmouduskudar/perform-exploratory-data-analysis-on-retail-data-with-python.git
cd perform-exploratory-data-analysis-on-retail-data-with-python
python -m venv .venv
source .venv/bin/activate   # Windows: .venv\Scripts\activate
pip install pandas numpy matplotlib seaborn scipy tabulate openpyxl jupyter
jupyter notebook online_retail.ipynb
```

If a cell still points at `/content/Online Retail.xlsx`, change it to the local file:

```python
data = pd.read_excel("Online Retail.xlsx")
```

## Source

Dataset: [UCI Online Retail](https://archive.ics.uci.edu/ml/machine-learning-databases/00352/Online%20Retail.xlsx)
