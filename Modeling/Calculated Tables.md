# [Calculated Tables](https://docs.microsoft.com/en-us/power-bi/transform-model/desktop-calculated-tables)
Calculated tables let you add new tables based on data you've already loaded into the model. Instead of querying and loading values into your new table's columns 
from a data source, you create a Data Analysis Expressions (DAX) formula to define the table's values.

E.g. Say I have table `AllSalesData` and I want a copy: 
```
CopyOfAllSalesData = AllSalesData
```

Various functions can also be applied. For example, use `UNION()` to stack tables on top of one another (note: they must have the same set of columns):
```
CopyOfAllSalesData = UNION(AllSalesData2019,AllSalesData2020, etc.)
```

Other functions:
- NATURALINNERJOIN
- NATURALLEFTOUTERJOIN
- INTERSECT (equivalent of a UNION but only for DUPLICATE data)
- EXCEPT (equivalent of a UNION but only for rows that exist in table A but not B)
