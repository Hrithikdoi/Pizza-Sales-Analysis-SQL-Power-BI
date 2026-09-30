# Pizza Sales Analysis

SQL Server analysis and Power BI dashboard for a year of pizza sales at a single restaurant. The SQL queries calculate the core sales KPIs and break sales down by day, month, category, size and pizza. The Power BI report presents the results.

## Dataset

- 48,620 order lines from 21,350 orders
- 1 January 2015 to 31 December 2015
- 32 pizza types across 4 categories (Classic, Supreme, Chicken, Veggie) and 5 sizes (S, M, L, XL, XXL)
- Columns include order ID, date, time, pizza name, category, size, quantity, unit price and total price

## Tools Used

- SQL Server
- Power BI
- CSV

## Key Metrics

| Metric | Value |
|---|---|
| Total revenue | 817,860 |
| Total orders | 21,350 |
| Total pizzas sold | 49,574 |
| Average order value | 38.31 |
| Average pizzas per order | 2.32 |

## Key Findings

- **Friday is the busiest day** with 3,538 orders. Sunday is the slowest with 2,624.
- **July is the busiest month** with 1,935 orders. October is the slowest with 1,646.
- **Large pizzas bring in the most revenue** at 45.9% of the total, followed by Medium (30.5%) and Small (21.8%). XL and XXL together account for under 2%.
- **Revenue is spread evenly across categories.** Classic leads with 26.9% and Veggie is lowest with 23.7%.
- **Chicken pizzas top the revenue ranking.** The Thai Chicken (43,434), Barbecue Chicken (42,768) and California Chicken (41,410) are the top three.
- **The Classic Deluxe sells the most pizzas** (2,453 units).
- **The Brie Carre is the weakest seller.** It has the lowest revenue (11,588) and the lowest quantity sold (490).
- **January category split:** Classic 26.7%, Supreme 25.7%, Veggie 24.4%, Chicken 23.2%.
- **Q1 size split:** Large 46.4%, Medium 29.8%, Small 22.1%, XL 1.6%, XXL 0.1%.

## SQL Analysis

The queries in `SQL/SQL_Queries.sql` cover:

1. Total revenue, average order value, total pizzas sold, total orders, average pizzas per order
2. Orders by day of the week and by month
3. Percentage of sales by pizza category (January)
4. Percentage of sales by pizza size (Q1)
5. Top 5 and bottom 5 pizzas by revenue, quantity and number of orders

SQL concepts used: aggregate functions, `COUNT(DISTINCT)`, `GROUP BY`, `ORDER BY`, `TOP`, subqueries, `CAST`, `DATENAME` and `DATEPART`.

## Power BI Dashboard

`PowerBI/Pizza_sales_report.pbix` contains the interactive report built on the same dataset.

## Repository Structure

```
Pizza-Sales-Analysis-SQL-Power-BI/
├── Dataset/
│   └── pizza_sales.csv
├── SQL/
│   └── SQL_Queries.sql
├── PowerBI/
│   └── Pizza_sales_report.pbix
└── README.md
```

## How to Use

1. Import `pizza_sales.csv` into SQL Server as a table named `pizza_sales`. Set `order_date` to a `DATE` type (the file uses dd-mm-yyyy).
2. Run the queries in `SQL_Queries.sql`.
3. Open the `.pbix` file in Power BI Desktop to explore the dashboard.

## Author

Hrithik Doiphode
