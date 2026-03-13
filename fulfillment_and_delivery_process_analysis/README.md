# Analysis of Fulfilment and Delivery Process — Müsli Company

## 📌 Project Overview

A müsli distribution company approached our team to help understand and improve their delivery process. The goal was to develop KPIs to track the health of their business and identify bottlenecks across each stage of the order fulfilment workflow — from order received to customer delivery.

Working as a team, we mapped the full logistics workflow, combined multiple data sources, engineered performance KPIs and conducted descriptive and diagnostic analysis to validate company assumptions against actual data. Findings were visualised and presented to stakeholders with actionable recommendations.

### Business Context & Workflow
The order process follows these stages:
1. **Order Received** — customers can order any day; warehouse operates Mon–Fri only
2. **Warehouse Processing** — order processed and made ready to ship (normally 2 days)
3. **Truck Departure** — trucks leave Mon, Wed and Fri; orders leave the day after ready (express: same day)
4. **Transit** — logistics provider averages 3-day delivery; delivers to customers Mon–Fri only

---

## 🛠️ Tools & Tech Stack

| Tool | Purpose |
|---|---|
| Python | Core programming language |
| Pandas | Data cleaning, transformation and EDA |
| NumPy | Numerical operations and simulation |
| Matplotlib | Data visualisation |
| Seaborn | Statistical visualisation |
| Miro | Workflow mapping and business process flowchart |
| Jupyter Notebooks | Interactive analysis environment |
| GitHub | Version control and collaboration |

---

## 🗂️ Data Model / Dataset

- **Source:** Excel files provided by the company
- **Four data sources combined:**

| Dataset | Description |
|---|---|
| **Orders** | Full transaction history with order dates and on-truck scan dates |
| **Order Process Data** | Intern-recorded "Ready to Ship" dates for a subset of orders |
| **Campaign Data** | Exact delivery dates collected via QR code marketing promotion |
| **Internal Data Study** | Additional internal operational data |

---

## 🔄 Workflow

### 1. Business Understanding
- Mapped the end-to-end order process in a flowchart using Miro
- Defined KPIs to track performance at each stage of the fulfilment workflow
- Documented business logic rules (warehouse schedule, truck departures, express processing)

### 2. Data Preparation
- Built reusable Python cleaning functions to standardise and clean each dataset
- Selectively merged datasets depending on the KPI being measured — combining only the relevant data sources for each specific KPI calculation

### 3. KPI Engineering
- Defined and engineered KPIs as new columns to measure performance at each stage of the fulfilment process
- Applied business logic rules (warehouse schedule, truck departures, express processing, weekend handling) to calculate time-based KPIs

| KPI | Definition |
|---|---|
| **Order to Ready for P.U.** | Time from order placed to package ready for pick-up (internal processing time) |
| **Ready for P.U. to Shipping** | Time from pick-up ready to package collected and shipped (pick-up/collection time) |
| **Shipping to Delivered** | Time from shipment dispatched to delivered to customer (transit/carrier time) |
| **Order to Delivery (Delivery Lead Time)** | Total end-to-end time from order placed to customer delivery |

### 4. Descriptive Analytics
- Performed EDA to understand data availability, descriptive statistics, missing values and outliers
- Compared actual KPI values against warehouse manager assumptions — quantifying matches and mismatches

### 5. Diagnostic Analytics
- Analysed time taken at each stage of the order process and the range of values per KPI
- Identified bottlenecks, outliers and stages with concerning reliability levels

### 6. Visualisation & Presentation
- Visualised findings through Matplotlib and Seaborn
- Delivered a 10–15 minute stakeholder presentation with actionable recommendations

### 7. Statistical Analysis (Supplement)
- Independently conducted after the main project
- Assessed KPI distributions through skewness analysis and boxplots
- Selected appropriate methods (z, t-distribution or bootstrap) to calculate confidence intervals for each KPI

---

## ▶️ How to Run the Project

1. **Clone the repository**
   ```bash
   git clone git@github.com:amandawang90-spec/neuefische-data-analysis-180825-muesli_eda_project.git
   cd fulfilment_and_delivery_process_analysis
   ```

2. **Install dependencies**
   ```bash
   pip install pandas numpy matplotlib seaborn openpyxl jupyter
   ```

3. **Add the data**
   - Place the Excel files in the `data/` folder
   - Note: raw data files are not pushed to GitHub (listed in `.gitignore`)

4. **Run the notebooks**
   - Open Jupyter Notebook
   - Run notebooks in order from EDA through to visualisation

---

## 📈 Key Findings & Insights

- **Assumption Validation** — compared warehouse manager assumptions against actual data to identify matches and mismatches at each stage of the fulfilment process
- **Bottleneck Identification** — specific shipment steps were identified as consistent bottlenecks causing delays across the logistics chain
- **KPI Variation** — analysis of average processing times and variation revealed stages with concerning reliability levels
- **Business Recommendations** — presented actionable improvement options to stakeholders, comparing the impact of daily logistics pick-up vs. express warehouse processing

> 📝 Detailed findings and visualisations are available in the project notebooks and stakeholder presentation.

---

## 📁 Project Structure

```
fulfilment-delivery-process-analysis/
│
├── data/                  # Raw Excel files (not pushed to GitHub)
├── notebooks/
│   ├── 01_eda.ipynb                      # Data cleaning, KPI engineering & EDA
│   └── 02_advanced_statistical_analysis.ipynb  # Distribution checks, skewness & confidence intervals
├── report/                # Stakeholder presentation (Google Slides)
└── README.md
```

---

## 👥 Team Project

This project was completed collaboratively using a structured Git workflow — branching, committing and merging via pull requests on GitHub. Workflow mapping and business process analysis were conducted as a team using Miro.

---