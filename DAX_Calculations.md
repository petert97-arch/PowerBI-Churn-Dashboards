Total Orders = 
DISTINCTCOUNT('SalesDB_2026-04-30-1407'[Order_ID])


Average Unit Price = 
AVERAGE('SalesDB_2026-04-30-1407'[Unit_Price])


Total Revenue = 
SUM('SalesDB_2026-04-30-1407'[Revenue])



Total Quantity Sold = 
SUM('SalesDB_2026-04-30-1407'[Quantity])



Average Days Inactive = 
AVERAGE('SalesDB_2026-05-07-1000'[Days_Since_Last_Purchase])



Churn Rate = 
DIVIDE(
    [Churned Customers],
    [Total Customers]
)



Churned Customers = 
CALCULATE(
    DISTINCTCOUNT('SalesDB_2026-05-07-1000'[Customer_Name]),
    'SalesDB_2026-05-07-1000'[Churn_Status] = "Churned"
)



Churned Revenue = 
CALCULATE(
    SUM('SalesDB_2026-05-07-1000'[Total_Revenue]),
    'SalesDB_2026-05-07-1000'[Churn_Status] = "Churned"
)


Total Customers = 
DISTINCTCOUNT('SalesDB_2026-05-07-1000'[Customer_Name])


