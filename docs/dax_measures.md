# DAX Measures

This project uses DAX measures to calculate the main business KPIs used in the Power BI report.

## Total Sales

```DAX
Total Sales = SUM(Fact_Sales[Price ($)])
```

Calculates total revenue from car sales.

## Sales Count

```DAX
Sales Count = COUNT(Fact_Sales[SaleID])
```

Counts the number of sales transactions.

## Average Price

```DAX
Average Price = AVERAGE(Fact_Sales[Price ($)])
```

Calculates the average selling price.

## Max Price

```DAX
Max Price = MAX(Fact_Sales[Price ($)])
```

Shows the highest sale price.

## Min Price

```DAX
Min Price = MIN(Fact_Sales[Price ($)])
```

Shows the lowest sale price.

## Average Annual Income

```DAX
Average Annual Income = AVERAGE(Dim_Customers[Annual Income])
```

Calculates average customer annual income.

## Total Sales %

```DAX
Total Sales % =
[Total Sales] / CALCULATE([Total Sales], ALL(Dim_Cars[Company]))
```

Shows the selected category contribution compared to total sales.

## Notes

These measures support KPI cards, company analysis, customer analysis, dealer analysis, and sales trend reporting.
