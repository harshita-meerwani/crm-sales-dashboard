📊 CRM Sales Performance Dashboard — Power BI

A fully interactive CRM analytics project built in **Microsoft Power BI**, analyzing a B2B sales pipeline across agents, regions, products, and sectors.

![Executive Dashboard](Executive%Dashboard.png)
![Sales Performance & Insights](Sales%Performance%Dashboard.png)

---

## 🗂️ Project Structure

```
crm-powerbi-dashboard/
│
├── CRM_Sales_Dashboard.pbix       # Main Power BI file
│
├── data/
│   ├── sales_pipeline.csv         # 500 sales opportunities (core fact table)
│   ├── accounts_csv.csv           # 85 client accounts with sector & revenue info
│   ├── sales_teams.csv            # 35 agents mapped to managers & regional offices
│   ├── products.csv               # 7 products with pricing
│   └── data_dictionary.csv        # Field descriptions for all tables
│
└── screenshots/
    ├── Executive Dashboard.png   # Executive Sales Dashboard
    └── Sales Performance Dashboard.png   # Sales Performance & Insights
```

---

## 📈 Dashboard Pages

### 1. Executive Sales Dashboard
High-level KPIs and strategic overview for leadership:
- **728K** Total Revenue | **500** Opportunities | **66.2%** Win Rate | **2.2K** Avg Deal Size
- Top 10 Sales Agents by revenue
- Opportunity distribution by deal stage (Won / Engaging / Lost)
- Revenue breakdown by Regional Office (West, Central, East)
- Total Revenue by Product with interactive filters for Region, Product, and Agent

### 2. Sales Performance & Insights
Operational detail for sales managers:
- Opportunities per Sales Agent (bar chart, all 30+ agents)
- Count of Opportunities & Close Value per Manager
- Revenue by Sector × Product matrix (9 sectors, 6 products)
- Total Revenue by Office Location (world map)
- Region filter (West / Central / East)

---

## 🗃️ Data Model

| Table | Rows | Key Fields |
|---|---|---|
| `sales_pipeline` | 500 | opportunity_id, sales_agent, product, account, deal_stage, close_value |
| `accounts_csv` | 85 | account, sector, revenue, employees, office_location |
| `sales_teams` | 35 | sales_agent, manager, regional_office |
| `products` | 7 | product, series, sales_price |

**Relationships:** `sales_pipeline` is the central fact table, joined to `accounts`, `sales_teams`, and `products` on their respective key columns.

---

## 🛠️ Tools Used

- **Microsoft Power BI Desktop** — data modeling, DAX measures, report design
- **CSV** — raw data source files

---

## 🚀 How to Use

1. Clone or download this repository
2. Open `CRM_Sales_Dashboard.pbix` in **Power BI Desktop**
3. If prompted, update the data source paths to point to the `/data` folder
4. Refresh the data and explore the dashboards

---

## 💡 Key Insights

- **Darcel Schlecht** leads all agents with ~71K in revenue and the highest opportunity count (38)
- **West region** generates the most revenue at 317K, nearly 1.6× East (194K)
- **GTX Plus Pro** is the top-revenue product (180K), while **MG Special** trails at 11K
- **Medical** and **Retail** sectors show strong cross-product revenue diversity
- Win rate of **66.2%** suggests a healthy pipeline with room to convert the 17.8% currently Engaging

---

## 📌 Notes

- Revenue figures in `accounts_csv.csv` are in **millions of USD**
- `close_value` in `sales_pipeline.csv` is in **USD**
- Deal stages follow the flow: `Prospecting → Engaging → Won / Lost`

---
