# Executive KPI Dashboard – Superstore (Power BI)

One-page management dashboard built in **Power BI** for the Veda Technology Data Analytics internship.

## Objective
Give management a concise view of sales, profit and order performance, with dynamic filters (slicers) for Year, Region, Category and Segment.

## Dataset
Superstore sales data: 9,994 rows, 21 columns, Jan 2014 to Dec 2017. No missing values or duplicate rows.

## Tools
Power BI Desktop, Power Query, DAX

## KPI Definitions
| KPI | Formula | Meaning |
|---|---|---|
| Total Sales | `SUM(Sales)` | Total revenue |
| Total Profit | `SUM(Profit)` | Total profit earned |
| Profit Margin % | `Total Profit / Total Sales` | Profit per $100 of sales |
| Total Orders | `DISTINCTCOUNT(Order ID)` | Number of unique orders |
| Avg Order Value | `Total Sales / Total Orders` | Average revenue per order |

## DAX Measures
```
Total Sales = SUM(superstore[Sales])
Total Profit = SUM(superstore[Profit])
Profit Margin % = DIVIDE([Total Profit], [Total Sales])
Total Orders = DISTINCTCOUNT(superstore[Order ID])
Avg Order Value = DIVIDE([Total Sales], [Total Orders])
```

## Dashboard
![Dashboard](dashboard_screenshot.png)

## Key Insights
- Sales grew from $484K (2014) to $733K (2017); profit almost doubled ($49.5K to $93.4K).
- Furniture earns only a 2% margin vs about 17% for Technology and Office Supplies.
- Tables (-$17.7K) and Bookcases (-$3.5K) are loss-making sub-categories.
- Central region has the lowest margin (8%); West (15%) and East (14%) perform best.

## Files
- `Executive_KPI_Dashboard.pbix` – Power BI file
- `Executive_KPI_Dashboard_Report.pdf` – project report
- `superstore.csv` – dataset
- `dashboard_screenshot.png` – dashboard screenshot

## Author
Sneha, Data Analytics Track, Veda Technology
