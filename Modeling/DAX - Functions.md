# DAX Functions
For colleagues, [here's](https://docs.google.com/spreadsheets/d/1OUsL7HiE5-LWipUaVlhm-NqBi4pY7wS3/edit#gid=1585899868) a list of important functions along with syntax and descriptions.

`Note: This is *not* a comprehensive list. This is a list of the most critical functions. Use it as a refresh before the exam.`

Contents:
- [Statistical Functions](#statistical-functions)
- [Text Functions](#text-functions)
- [Conversions](#conversions)
- [Filter Functions](#filter-functions)
  - Related & RelatedTable
- [Context](#context)
  - [All](#all)
  - [Filter](#filter)
  - [Calculate](#calculate)
- [Time Functions](#time)
  - [Time Intelligence](https://github.com/user905/PL-300-Personal-Study-Guide/blob/main/Modeling/DAX%20-%20Time%20Intelligence.md)

## Statistical Functions

#### Ending in `A`. 
These do the same thing as their normal counterparts, albeit by including non-numerics, i.e. text, blank, dates, etc.:
<p align="center"><img width="718" alt="image" src="https://user-images.githubusercontent.com/29554021/156592075-1ec32b82-aabf-4f5e-8969-bbf94959f634.png"></p>

#### Ending in `X`.
Similarly, these perform the same function as their normal counterparts, only here they'll perform a calculation per row.  

E.g. Say you have a temperature column that is in celsius and you want the average temperature, but in Farenheit. You could use `= AVERAGEX(MyTable,(MyTable[Temperature] * 9/5)+32)` to return the total average value after converting each row to Farenheit.
<p align="center"><img width="736" alt="image" src="https://user-images.githubusercontent.com/29554021/156593371-c48ddc61-1a80-4550-a14e-350dfec9152e.png"></p>

## Text Functions
#### Searching
<p align="center"><img width="814" alt="image" src="https://user-images.githubusercontent.com/29554021/156603664-3cf76d49-8919-4a0a-8f5a-41e39dc86b4d.png"></p>
<p align="center"><img width="793" alt="image" src="https://user-images.githubusercontent.com/29554021/156605850-b2b6866b-1c8f-4913-afe0-02ce2ec2fee9.png"></p>

- Substitute: `<instance num>` tells the function to look for a specific instance, i.e. 1st, 2nd, 3rd, etc. No value means all.
- Replace (not shown): similar to substitute, but with replace you know where in the text the value is that you want to change.

#### Conversions
<p align="center"><img width="813" alt="image" src="https://user-images.githubusercontent.com/29554021/156606258-e411ddbd-fa1a-4dd3-8797-9332e5795c38.png"></p>

## Information Functions
<p align="center"><img width="788" alt="image" src="https://user-images.githubusercontent.com/29554021/156609876-725dc349-44bc-41ad-b721-7b639c03fae0.png"></p>

- LOOKUPVALUE: Equivalent to VLOOKUP in Excel. Does `not` require relationships between tables, although the lookup values should exist in both tables.
  - Start with the column where your result is. Then define the column where the search result will be found. Finally, add the search result (could be a column name).

## Filter Functions
#### Related
<p align="center"><img width="811" alt="image" src="https://user-images.githubusercontent.com/29554021/156615199-1ee099a0-64d9-4084-bed8-c28b00d9020f.png"></p>

- Uses the existing relationship of two tables, but goes in the opposite direction of the cardinality. (Against the relationship arrows in the Modeling page; from Many:1)
- Returns a single value.

#### RelatedTable
- Allows you to follow the stream of relationships between tables and tie otherwise distantly related tables & columns together. This descends the relationship stream (1:Many), whereas `Related` ascends (Many:1).
- Return is a filtered table. This table can then be manipulated the way you would any other.
- Note that the function is smart enough to understand the columns tying the two tables together.

## Context
What is the difference between these two formulas? (Pulled from [here](https://www.udemy.com/course/70-778-analyzing-and-visualizing-data-with-power-bi/learn/lecture/14030996#overview))
<p align="center"><img width="507" alt="image" src="https://user-images.githubusercontent.com/29554021/156620383-523391d4-f8fc-480e-a4e7-15ba7eb79baf.png"></p>

The second formula takes the entirety of the `FactInternetSales` table and sums across all rows `without referencing the established relationships between these two tables`. The first uses the relationships established through the Modeling of these two tables to connect `ProductCategoryKey` in the top dimension table to `ProductKey` in the fact table:

<p align="center"><img width="712" alt="image" src="https://user-images.githubusercontent.com/29554021/156620951-15b9c7e0-a7de-4909-be7a-094a2fac8f9d.png"></p>

<p align="center"><img width="894" alt="image" src="https://user-images.githubusercontent.com/29554021/156621403-5c37da08-1c0b-42f6-81af-511119b25f35.png"></p>

This difference has its uses. For example, if you want to know the percentage of sales a particular product makes up from the the total sales, you would divide the first formula by the second:
```
PercentTotal = 
    SUMX(
        RELATEDTABLE(FactInternetSales),
        FactInternetSales[ProductStandardCost]
    ) / 
    SUMX(
        FactInternetSales,
        FactInternetSales[ProductStandardCost]
    )
```

As a calculated column, this latter use has its pitfall however.

<p align="center"><img width="229" alt="image" src="https://user-images.githubusercontent.com/29554021/156634621-f140cbb5-d45c-4894-a48d-1898ea4b6271.png"></p>

Note here that the year breakouts don't work. What's the problem? The problem is that the calculated column has already created values, and those values were not calculated with breakouts into years. To fix this, you recreate the calculation as a measure. But even this won't quite work...Here it is recreated as a measure:

<p align="center"><img width="229" alt="image" src="https://user-images.githubusercontent.com/29554021/156634891-18fc3be3-b506-4533-b475-7fe7bb0c4b29.png"></p>

What's the problem now? Well, take Bike: Within the _context_, bikes sell 100% of bikes. Same for apparel. You need to use...

#### All
All removes context from the current equation. So our new formula looks like this:
```
PercentTotal = 
    SUMX(
        RELATEDTABLE(FactInternetSales),
        FactInternetSales[ProductStandardCost]
    ) / 
    SUMX(
        ALL(FactInternetSales),
        FactInternetSales[ProductStandardCost]
    )
```

And voila:
<p align="center"><img width="673" alt="image" src="https://user-images.githubusercontent.com/29554021/156635700-c0ef3513-b91d-466a-a024-0b1f564d9e60.png"></p>

In the case of RelatedTable, the calculated column wasn't taking advantage of the context. The Measure on the other hand does.

#### Filter
Filter does the opposite. It narrows down the context: E.g. 
```
SumOfHelmetSales = 
    SUMX(
        Filter(
          ProductSales,
          ProductSales[ProductName]="Helmet"
        ),
        ProductSales[SaleValue]
    )
```

#### Calculate
Another way to use the `All` & `Filter` functions. Consider the previous function that used `All`:
```
PercentTotal = 
      SUMX(
          RELATEDTABLE(FactInternetSales),
          FactInternetSales[ProductStandardCost]
      ) / 
      SUMX(
          ALL(FactInternetSales),
          FactInternetSales[ProductStandardCost]
      )
```

To do the same with `Calculate`:
```
PercentTotal = 
      SUMX(
          RELATEDTABLE(FactInternetSales),
          FactInternetSales[ProductStandardCost]
      ) / 
      CALCULATE(
            SUMX(
                FactInternetSales,
                FactInternetSales[ProductStandardCost]
            ),
        ALL(FactInternetSales)
      )
```

Here you tell CALCULATE that the table `FactInternetSales` should sum, but with the added stipulation of a filter, which is here `All()`.

Similarly, if you want to filter:
```
PercentTotal = 
      SUMX(
          RELATEDTABLE(FactInternetSales),
          FactInternetSales[ProductStandardCost]
      ) / 
      CALCULATE(
            SUMX(
                FactInternetSales,
                FactInternetSales[ProductStandardCost]
            ),
            Filter(FactInternetSales[PromotionKey]=1
      )
```

Lastly, here's a helpful way to think of context:
<p align="center"><img width="676" alt="image" src="https://user-images.githubusercontent.com/29554021/156639196-218f495a-9a1f-4052-b257-ff8afd6cfc58.png"></p>

#### Additional Functions
ALL-Related functions:
- ALLEXCEPT
- ALLNOBLANKROW
- ALLSELECTED

<p align="center"><img width="639" alt="image" src="https://user-images.githubusercontent.com/29554021/156638490-57d7df7d-70cf-41bb-9f8b-4c3cf4000cd1.png"></p>

ALLSELECTED is the least obvious. It can include additional filter info inside the parentheses or not. Here is an example:
<p align="center"><img width="706" alt="image" src="https://user-images.githubusercontent.com/29554021/156640264-484c40f7-175e-46a6-8b24-bb79b65f5e0c.png"></p>

Here's more with additional filter options:
<p align="center"><img width="874" alt="image" src="https://user-images.githubusercontent.com/29554021/156644817-a43792e9-c8a1-4ed8-a1f1-a0b2b7dbab79.png"></p>

<p align="center"><img width="873" alt="image" src="https://user-images.githubusercontent.com/29554021/156643978-cbbe5614-87f2-40aa-bec8-2efed8301fc0.png"></p>

For a great explanation, go to [this](https://www.udemy.com/course/70-778-analyzing-and-visualizing-data-with-power-bi/learn/lecture/14031006#overview) lesson in the DA-100 Udemy course.

# Time
A sampling (see [here](https://docs.google.com/spreadsheets/d/1OUsL7HiE5-LWipUaVlhm-NqBi4pY7wS3/edit#gid=1585899868) for more (filter for Category: Date and Time Functions)
<p align="center"><img width="633" alt="image" src="https://user-images.githubusercontent.com/29554021/156782575-19ac02ab-ae50-4450-8192-b21913574c0f.png"></p>
