# Pizza Sales Analysis: SQL Server and Power BI

Analysis of a full year of sales for a single pizza restaurant. SQL Server queries calculate the core sales KPIs and break sales down by day, month, category, size and pizza. A two-page Power BI report presents the same results.

## Dashboard Preview

![Home page]\(images/home.png)
![Best and worst sellers]\(images/best-worst-sellers.png)

## Dataset

- 48,620 order lines from 21,350 orders, 1 January 2015 to 31 December 2015
- 32 pizzas across 4 categories (Classic, Supreme, Chicken, Veggie) and 5 sizes (S, M, L, XL, XXL)
- Columns: pizza ID, order ID, pizza name ID, quantity, order date, order time, unit price, total price, size, category, ingredients, pizza name

## Key Metrics

| Metric | Value |
|---|---|
| Total revenue | 817,860 |
| Total orders | 21,350 |
| Total pizzas sold | 49,574 |
| Average order value | 38.31 |
| Average pizzas per order | 2.32 |

## Key Findings

- **Friday is the busiest day** with 3,538 orders, followed by Thursday (3,239) and Saturday (3,158). Sunday is the slowest with 2,624.
- **July is the busiest month** with 1,935 orders. October is the slowest with 1,646.
- **Large pizzas bring in the most revenue** at 45.9%, followed by Medium (30.5%) and Small (21.8%). XL and XXL together are under 2%.
- **Categories are close.** Classic leads at 26.9%, then Supreme (25.5%), Chicken (24.0%) and Veggie (23.7%).
- **Chicken pizzas take the top three revenue spots:** Thai Chicken (43,434), Barbecue Chicken (42,768) and California Chicken (41,410).
- **The Classic Deluxe sells the most pizzas** (2,453 units).
- **The Brie Carre is the weakest seller.** It has the lowest revenue (11,588) and the lowest quantity sold (490).
- **January category split:** Classic 26.7%, Supreme 25.7%, Veggie 24.4%, Chicken 23.2%.
- **Q1 size split:** Large 46.4%, Medium 29.8%, Small 22.1%, XL 1.6%, XXL 0.1%.

## SQL Analysis

The queries in `SQL/SQL_Queries.sql` (SQL Server) cover:

1. Total revenue, average order value, total pizzas sold, total orders, average pizzas per order
2. Orders by day of the week and by month
3. Share of sales by pizza category for January
4. Share of sales by pizza size for Q1
5. Top 5 and bottom 5 pizzas by revenue, quantity and number of orders

SQL used: aggregate functions, `COUNT(DISTINCT)`, `GROUP BY`, `TOP`, subqueries, `CAST`, `DATENAME`, `DATEPART`.

## Power BI Report

`PowerBI/Pizza_sales_report.pbix` has two pages with page navigation between them:

- **Home:** KPI cards, orders by day and month, sales by category and size
- **Best/Worst Sellers:** top and bottom pizzas by revenue, quantity and orders

The report uses DAX measures for Total Revenue, Total Orders, Total Pizzas Sold, Average Order Value and Average Pizzas Per Order, plus slicers for date and pizza category.

## Repository Structure

```text
Pizza-Sales-Analysis-SQL-Power-BI/
├── Dataset/
│   └── pizza_sales.csv
├── SQL/
│   └── SQL_Queries.sql
├── PowerBI/
│   └── Pizza_sales_report.pbix
├── images/
│   ├── home.png
│   └── best-worst-sellers.png
└── README.md
```

## How to Use

1. Import `pizza_sales.csv` into SQL Server as a table named `pizza_sales`. Set `order_date` to a `DATE` type (the file uses dd-mm-yyyy).
2. Run the queries in `SQL_Queries.sql` one at a time.
3. Open the `.pbix` file in Power BI Desktop.

## Author

**Hrithik Doiphode**
GitHub: https://github.com/Hrithikdoi
