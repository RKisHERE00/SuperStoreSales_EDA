# US Superstore Retail EDA & Customer RFM Analysis

## 📌 Project Overview

This project performs exploratory data analysis (EDA), sales trend analysis, geographic analysis, customer segmentation, and advanced analytics on the **US Superstore retail dataset**.

The analysis uses Python to transform raw transactional data into business-oriented insights covering:

- Sales and revenue performance
- Product and category performance
- Customer segments
- Geographic sales distribution
- Shipping and fulfillment
- Monthly sales trends and seasonality
- Customer RFM (Recency, Frequency, Monetary) segmentation
- Pareto (80/20) revenue concentration
- Time-series decomposition

The processed customer-level information is also exported for use in **Power BI or Tableau**.

---

## 📂 Dataset

The notebook uses a `SuperStoreSales.csv` dataset containing **9,800 transaction records and 18 original columns**.

Important fields include:

- `Order ID`
- `Order Date`
- `Ship Date`
- `Ship Mode`
- `Customer ID`
- `Customer Name`
- `Segment`
- `Country`
- `City`
- `State`
- `Postal Code`
- `Region`
- `Product ID`
- `Category`
- `Sub-Category`
- `Product Name`
- `Sales`

The dataset contains US retail transactions covering customers, products, locations, shipping methods, and sales.

> **Note:** The notebook currently loads the CSV using a local Windows file path. Update the `pd.read_csv()` path to match your local dataset location before running it.

---

## 🛠️ Technologies Used

- **Python**
- **NumPy**
- **Pandas**
- **Matplotlib**
- **Seaborn**
- **Statsmodels**
- **Jupyter Notebook**

---

## 🔍 Analysis Workflow

### 1. Data Loading & Exploration

The project begins by loading the Superstore dataset and examining:

- Dataset dimensions
- Column names
- Data types
- Descriptive statistics
- Missing values
- Duplicate records

The dataset contains **9,800 rows and 18 original columns**. No duplicate rows were found.

---

### 2. Data Cleaning & Feature Engineering

The following transformations are performed:

- Converts `Order Date` and `Ship Date` to datetime format
- Creates `Shipping Days`
- Extracts `Order Year`
- Extracts `Order Month`
- Creates `Order YearMonth`

These features support shipping analysis and time-based sales analysis.

---

### 3. Business KPIs

The notebook calculates high-level business metrics including:

- **Total Sales Revenue:** $2,261,536.78
- **Unique Orders:** 4,922
- **Unique Customers:** 793
- **Average Order Value:** $459.48

These KPIs provide a quick overview of the business's overall performance.

---

## 📊 Exploratory Data Analysis

### Product Performance

Sales are aggregated by category and sub-category to identify the strongest revenue-generating product lines.

The analysis identifies **Phones** and **Chairs** among the highest-revenue sub-categories, while **Technology** is highlighted as a major revenue-driving category.

### Customer Segments & Regions

Revenue is analyzed across:

- Consumer
- Corporate
- Home Office

Geographic performance is also compared across:

- West
- East
- Central
- South

The analysis highlights the **West and East regions** as major contributors to overall revenue.

### Shipping Analysis

Shipping modes are analyzed based on:

- Order volume
- Average shipping time

The notebook compares:

- Standard Class
- Second Class
- First Class
- Same Day

`Shipping Days` is calculated from the difference between `Ship Date` and `Order Date`.

### Sales Trends

Monthly revenue is visualized to identify changes in sales over time and potential seasonal patterns.

---

## 👥 Customer RFM Analysis

The project implements **RFM analysis** to segment customers based on:

### Recency
How recently a customer placed an order.

### Frequency
How frequently a customer orders.

### Monetary
How much revenue a customer has generated.

Each metric is converted into a quartile-based score, producing an overall `RFM_Score`.

Customers are then assigned to five business personas:

| Persona | Description |
|---|---|
| **Champions (VIP)** | Highly recent, frequent, and high-value customers |
| **Loyal Customers** | Consistent repeat customers |
| **Recent Buyers** | Recent customers with relatively low frequency |
| **At-Risk (High Value)** | Historically valuable customers who have become inactive |
| **Lost Customers** | Customers with low engagement and extended inactivity |

These segments can be used to guide targeted marketing and retention strategies.

---

## 🎯 Advanced Analytics

### Pareto Analysis

A Pareto analysis ranks products by revenue and calculates cumulative revenue contribution.

The notebook investigates whether approximately **20% of products account for roughly 80% of total revenue**, helping identify products that deserve higher inventory and merchandising priority.

### Geographic Analysis

The project identifies the top-performing states and cities by sales.

The analysis highlights **California and New York** as leading revenue-generating states, with major urban markets such as **New York City and Los Angeles** contributing significantly.

### Time-Series Decomposition

Monthly sales are decomposed into:

- Observed
- Trend
- Seasonal
- Residual

The analysis identifies a recurring **Q4 sales increase**, particularly during October–December, followed by a decline in January.

---

## 💾 Output

The notebook exports a processed dataset:

```text
superstore_processed_rfm.csv
```

This file contains the original transaction data together with customer-level RFM information, including:

- `Persona`
- `RFM_Score`

The processed dataset can be imported into:

- Power BI
- Tableau
- Other BI and visualization tools

---

## 📁 Suggested Repository Structure

```text
superstore-retail-analysis/
│
├── README.md
├── Superstore_Retail_Analysis.ipynb
├── SuperStoreSales.csv
├── superstore_processed_rfm.csv
└── requirements.txt
```

---

## ▶️ How to Run

### 1. Clone or download the project

Place the notebook and dataset in your project directory.

### 2. Install dependencies

```bash
pip install numpy pandas matplotlib seaborn statsmodels jupyter
```

### 3. Update the dataset path

Change the `pd.read_csv()` path in the notebook to the location of your `SuperStoreSales.csv` file.

### 4. Run the notebook

```bash
jupyter notebook
```

Open the notebook and run the cells from top to bottom.

---

## 📈 Key Business Takeaways

The analysis produces several actionable insights:

- Focus inventory planning on high-revenue products identified through Pareto analysis.
- Prioritize the West and East regions for major revenue opportunities.
- Prepare additional fulfillment capacity before the Q4 seasonal peak.
- Use RFM personas to personalize customer retention and marketing campaigns.
- Target high-value at-risk customers with win-back campaigns.
- Reward Champions/VIP customers with loyalty benefits and early access.
- Use the processed RFM dataset as a foundation for a Power BI or Tableau dashboard.

---

## 📝 Resume Description

**US Superstore Retail EDA & Customer RFM Analysis | Python, Pandas, Seaborn, Statsmodels**

- Analyzed 9,000+ retail transactions using Python, Pandas, and Seaborn to identify sales trends, seasonal patterns, product performance, and regional revenue distribution.
- Built an RFM-based customer segmentation pipeline that classified customers into five actionable business personas.
- Applied Pareto analysis and time-series decomposition to identify major revenue drivers and seasonal demand patterns, producing recommendations for inventory, marketing, and customer retention.

---

## 👤 Project

**Data Science / Exploratory Data Analysis Project**

Built using Python and Jupyter Notebook.
