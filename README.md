


### 📷 Dashboard Preview

![Overview](images/dashboard_overview.png)
![Trend Analysis](images/trend_analysis.png)
![Top Consultants](images/top_consultants.png)
![Specialization](images/specialization_analysis.png)
![Regional Analysis](images/regional_analysis.png)
![Drill-Down](images/detailed_drilldown.png)





# 📊 Recruitment Analytics — Power BI Dashboard

An interactive Power BI dashboard that analyzes recruitment and job posting data to deliver actionable insights on conversion rates, consultant performance, specialization trends, and regional comparisons.

![Power BI](https://img.shields.io/badge/Power%20BI-F2C811?style=for-the-badge&logo=powerbi&logoColor=black)
![DAX](https://img.shields.io/badge/DAX-Measures-blue?style=for-the-badge)
![Status](https://img.shields.io/badge/Status-Active-brightgreen?style=for-the-badge)

---

## 📁 Repository Structure

```
├── dashboard/
│   └── my project11.pbix               # Power BI report file
├── data/
│   ├── Hands on Hospital_HR.xlsx        # HR dataset
│   └── PowerBI_Dashboard_Project_A.xlsx # Project dataset
├── dax/
│   └── measures.dax                     # All DAX measure definitions
├── images/
│   └── (dashboard screenshots)
├── docs/
│   └── data_dictionary.md               # Column definitions & data types
├── .gitignore
└── README.md
```

---

## 🎯 Project Objective

Analyze recruitment/job data and deliver insights through an interactive Power BI dashboard. The dataset contains **job postings, job statuses, recruitment consultant data, specializations, regional data, and trends over time** — enabling stakeholders to identify patterns, optimize consultant performance, and improve closure rates across specializations and regions.

---

## ❓ Business Questions Addressed

### A. Overall Job Metrics
- What is the total number of jobs posted?
- What is the split between open and closed jobs?
- What is the overall conversion ratio (Closed Jobs ÷ Total Jobs)?

### B. Trend Analysis
- How has the conversion ratio trended over months?
- How has the total number of jobs evolved month by month?
- How do job closure trends look across different months?

### C. Top Performers Analysis
- Who are the top 10 recruitment consultants based on conversion ratio?
- How do different consultants perform over time?

### D. Jobs by Specialization
- What is the distribution of jobs by medical specialization?
- What are the conversion ratios across different specializations?
- Which specializations have the highest and lowest job closure rates?

### E. Jobs by Region & State
- How do conversion ratios vary by region?
- How do different states compare in terms of job closures and open jobs?

### F. Specialization & Region Trends
- How does conversion ratio trend vary by specialization across months?
- How do different regions trend in terms of conversion ratio?

### G. Detailed Job Listing & Filtering
- Drill down into individual job records (Job ID, Posting Date, Specialization, Region, State, Consultant)
- Filter by Sales Consultant, Region, Specialization, and Status (Open/Closed)

---

## 📐 Data Model (Star Schema)

The dashboard uses a **star schema** optimized for Power BI performance:

- **FactJobs** (center): Job ID, Posting Date, Status, Region, State, Sales Consultant, Specialization, Conversion Indicator
- **DimDate**: Date, Month, Year, Quarter
- **DimConsultant**: Consultant ID, Consultant Name
- **DimSpecialization**: Specialization ID, Specialization Name
- **DimRegion**: Region ID, Region Name, State

**Why Star Schema?**
- ⚡ Fast query performance in Power BI
- 🧩 Simplifies building trend, comparison, and drill-down visuals
- 🔗 Clean relationships between facts and dimensions

---

## 📊 Dashboard Pages & Visuals

| Page | Visual Type | Description |
|------|-------------|-------------|
| **Overview** | KPI Cards | Total Jobs, Open Jobs, Closed Jobs, Conversion Ratio |
| **Trend Analysis** | Line Charts | Conversion Ratio trend by month; Jobs trend by month |
| **Top Performers** | Bar Chart | Top 10 Consultants ranked by Conversion Ratio |
| **Specialization** | Pie + Bar Charts | Jobs distribution & Conversion Ratio by specialization |
| **Regional Analysis** | Map + Bar Charts | Conversion Ratio by region; State-wise breakdown |
| **Drill-Down Details** | Table + Slicers | Interactive table with all job fields and filters |

### 🔍 Filters / Slicers Available
- Date Range
- Sales Consultant
- Region
- Specialization
- Status (Open / Closed)

---

## 📏 DAX Measures

| Measure | Formula | Purpose |
|---------|---------|---------|
| **Total Jobs** | `COUNTROWS(FactJobs)` | Count of all job postings |
| **Open Jobs** | `CALCULATE(COUNTROWS(FactJobs), FactJobs[Status] = "Open")` | Jobs still open |
| **Closed Jobs** | `CALCULATE(COUNTROWS(FactJobs), FactJobs[Status] = "Closed")` | Successfully closed jobs |
| **Conversion Ratio** | `DIVIDE([Closed Jobs], [Total Jobs])` | Percentage of jobs closed vs. total |

---

## 🚀 Getting Started

1. Clone or download this repository
2. Open `dashboard/my project11.pbix` in Power BI Desktop
3. Update data source connections and refresh
4. Explore the dashboard pages and use slicers to filter

---

## 📬 Contact

**Saranya** — [@saranya-data-analyst](https://github.com/saranya-data-analyst)

---

> *Built with ❤️ using Power BI*
