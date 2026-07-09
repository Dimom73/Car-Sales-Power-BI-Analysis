# Data Model

The original dataset was provided as a single flat table. For the Power BI report, it was transformed into a structured star schema model.

## Fact Table

### Fact_Sales

Contains the core sales transaction data.

Example fields:

- SaleID
- CarID
- SaleDate
- CustomerID
- DealerID
- Price
- Phone

## Dimension Tables

### Dim_Customers

Customer information:

- CustomerID
- Customer Name
- Gender
- Annual Income
- Income Group

### Dim_Cars

Car information:

- CarID
- Company
- Model
- Body Style
- Engine
- Transmission
- Color

### Dim_Dealers

Dealer information:

- DealerID
- Dealer Name
- Dealer Number
- Dealer Region

### Dim_Date

Date information:

- SaleDate
- Year
- Quarter
- Month
- Month Name
- Month Start

## Relationships

The model uses many-to-one relationships:

- Fact_Sales[CustomerID] → Dim_Customers[CustomerID]
- Fact_Sales[CarID] → Dim_Cars[CarID]
- Fact_Sales[DealerID] → Dim_Dealers[DealerID]
- Fact_Sales[SaleDate] → Dim_Date[SaleDate]

## Filtering Direction

The report uses single-direction filtering from dimension tables to the fact table.

This makes the model easier to understand and helps slicers and visuals filter the sales data correctly.
