# Role Playing Dimensions
Related: Guidance on [Active & Inactive Relationships](https://docs.microsoft.com/en-us/power-bi/guidance/relationships-active-inactive)

A Role Playing Dimension is when two tables have more than one relationship between them. In this case, one is Inactive, because tables can have only one active 
relationship. This does not mean that the inactive relationship cannot be leveraged. Using the `USERELATIONSHIP()` function permits this.

Consider this setup:  
<p align="center"><img width="309" alt="image" src="https://user-images.githubusercontent.com/29554021/156819921-bf1d934a-8ea1-42d9-94c9-98aae41a1c9a.png"></p>

Here the fact table is connected to the DateTable in two ways: 1) DueDateKey > DateKey, and 2) OrderDateKey > DateKey. Only the former is active.

To get a visualization on OrderDate going, say to show order Month, use `USERELATIONSHIP`:
```
BMonthOrderDate=USERELATIONSHIP(FactInternetSales[OrderDateKey],DateTable[DateKey])
```

Use this to get total sales by period (day, month, whatever):
```
SalesAmountOrderDate=
      CALCULATE(
            SUM(FactInternetSales[SalesAmount]),
            USERELATIONSHIP(
                  FactInternetSales[OrderDateKey],
                  DateTable[DateKey]
            )
      )
```

<p align="center"><img width="629" alt="image" src="https://user-images.githubusercontent.com/29554021/156820781-5f8e847b-b5dd-4188-8616-6d72e2adbc33.png"></p>

This is somewhat messy and could be simplified by creating a separate date table (a copy of the first) with a relationship to the Fact table. There would then only be single relationships between the Fact table and the two Date Dimension tables.

Note thate `USERELATIONSHIPS()` defines the relationship, while `RELATED()` calls for a value from the column of a related table.
