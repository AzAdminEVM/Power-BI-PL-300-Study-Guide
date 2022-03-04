# Time Intelligence

Content:
- [FirstDate & Last Date](#firstdate--lastdate)
- [StartOf & EndOf](#startof--endof)
- [Next & Previous](#next--previous)
- [DatesInPeriod](#datesinperiod)
- [DatesMTD/QTD/YTD & TotalMTD/QTD/YTD](#datesmtdqtdytd--totalmtdqtdytd)
- [Opening & Closing](#opening--closing)
- [SamePeriodLastYear & ParallelPeriod](#sameperiodlastyear--parallelperiod)
- [Time Intelligence & Semi-Additive Measures](#time-intelligence--semi-additive-measures)

### FirstDate & LastDate
<p align="center"><img width="641" alt="image" src="https://user-images.githubusercontent.com/29554021/156783171-97256f95-ffe2-45d2-b6fe-b78a893d8765.png"></p>

Simple. Note however that as a standalone function the same results can be accomplished by dropping a date field into a well and applying basic filters like First/Last. Standalone, what makes these useful is that they force the consumer to look at one value without being able to change it. Otherwise, they are used in conjunction with other formulas as a more versatile option that returns a table that can be treated as a value. More on this later.

Return type: _table_

### StartOf & EndOf
<p align="center"><img width="641" alt="image" src="https://user-images.githubusercontent.com/29554021/156784258-e9ce72f5-134d-46d1-b827-55637b6a63e4.png"></p>

Note that these functions expect a _column_ for their input. Functions like MIN/MAX return _values_ and cannot be used. This is why you use FirstDate/LastDate.

Return type: _table_

### Next & Previous
<p align="center"><img width="635" alt="image" src="https://user-images.githubusercontent.com/29554021/156788223-6819341f-ea59-4a37-81f5-65fdeab1c5c4.png"></p>

Return type: _table_

Example: `SalesAmountNext = CALCULATE(SUM(FactInternetSales[SalesAmount]),NEXTDAY(FactInternetSales[DueDate]))`. Note how this changes the context for the CALCULATE function.

Results:
<p align="center"><img width="296" alt="image" src="https://user-images.githubusercontent.com/29554021/156788883-5a72c2a3-7004-4b00-bd9d-15187d6b30e8.png"></p>

Caveat: You can't use this with a date hierarchy because that forces the context down into one day per row. You have to use a single field because that forces the context to represent the whole table, even if each row is focused on a single day.

Results w/ Date Hierarchy:
<p align="center"><img width="688" alt="image" src="https://user-images.githubusercontent.com/29554021/156789201-3114bcb0-45fb-44f8-b1eb-c943fbbd116f.png"></p>

### DatesInPeriod
<p align="center"><img width="636" alt="image" src="https://user-images.githubusercontent.com/29554021/156789928-04211467-697b-42a2-bb5e-66e8de79772c.png"></p>

Return a table of dates from within a range defined by the inputs.
```
SalesAmountPrev = 
          CALCULATE(
                  SUM(
                      FactInternetSales[SalesAmount]
                  ),
                  DATESINPERIOD(
                      FactInternetSales[DueDate],
                      FIRSTDATE(FactInternetSales[DueDate]),7,DAY
                  )
          )
```

Note the use of `FIRSTDATE` here. While `DATESINPERIOD` expects values in its date range period, here `FIRSTDATE` is able to provide a single value, as it is wrapped in another function.

Return type: _table_

### DatesMTD/QTD/YTD & TotalMTD/QTD/YTD
<p align="center"><img width="471" alt="image" src="https://user-images.githubusercontent.com/29554021/156795748-05624963-2fe2-46a9-b7a4-6882542262c9.png"></p>

Dates: These provide cumulative totals. See below for a `DATESMTD`:

<p align="center"><img width="476" alt="image" src="https://user-images.githubusercontent.com/29554021/156796422-58f5526b-7f05-40e8-89fa-e83abfb395ee.png">"></p>

Total: These allow you to substitute out calculate and just sum the running total:

<p align="center"><img width="546" alt="image" src="https://user-images.githubusercontent.com/29554021/156797252-d41c9603-d789-412c-9f7f-b101e4785bad.png"></p>

Return type: _table_

### Opening & Closing
<p align="center"><img width="642" alt="image" src="https://user-images.githubusercontent.com/29554021/156797752-24a6cc82-363b-43dd-a3f7-54c7e0dd2a23.png"></p>

`Caveat: Cannot be used with CALCULATE.` Syntax is similar to the TOTAL functions above.

<p align="center"><img width="645" alt="image" src="https://user-images.githubusercontent.com/29554021/156798029-d84b67d1-b4f6-4659-a776-1463cb585cdd.png"></p>

### SamePeriodLastYear & ParallelPeriod
<p align="center"><img width="644" alt="image" src="https://user-images.githubusercontent.com/29554021/156801047-459786a1-3c58-4a60-9689-371d53d70ffd.png"></p>

SamePeriodLastYear is more obvious. ParallelPeriod simply allows you to pick a period of dates to compare.

Use these with CALCULATE.

<p align="center"><img width="639" alt="image" src="https://user-images.githubusercontent.com/29554021/156801579-8556c7e7-e9fd-4ae6-aedf-20d4cb7aed54.png"></p>

The same result can be achieved by replacing PARALLELPERIOD with NEXTMONTH.


Return type: _table_

## Time Intelligence & Semi-Additive Measures
Summary pulled from [here](https://www.sqlbi.com/articles/semi-additive-measures-in-dax/).
First things first: what is a semi-additive calculation? Any calculation can be either additive, non-additive or semi-additive. An additive measure uses SUM to aggregate over any attribute. The sales amount is a perfect example of an additive measure. Indeed, the sales amount for all customers is the sum of the individual sales for each customer; at the same time, the amount over a year is the sum of the amounts for each month.

A non-additive measure does not use SUM over any dimension. Distinct count is the simplest example: the distinct count of products sold over a month is not the sum of the distinct counts of individual days. The same happens with any other dimension: a distinct count of products sold in a country is not the sum of the distinct counts of the products sold in each city in the country.

Semi-additive calculations are the hardest ones: `a semi-additive measure uses SUM to aggregate over some dimensions and a different aggregation over other dimensions – a typical example being time.` 

Consider the balance in a bank account at the end of a quarter. The balance is not the sum of values across the previous three months, it is the last month shown for that quarter.

So this:
```
LastBalance LD =
CALCULATE (
    SUM ( Balances[Balance] ),
    LASTDATE ( 'Date'[Date] )
)
```
Resulting in this:
<p align="center"><img width="642" alt="image" src="https://user-images.githubusercontent.com/29554021/156800316-335a34a4-fc91-4618-915a-0253c3b4728f.png"></p>

As opposed to:
<p align="center"><img width="642" alt="image" src="https://user-images.githubusercontent.com/29554021/156800424-f87a18d8-849d-405c-b744-c7fa83d4a416.png"></p>

Another example would be how you compound discounts on an item. 30% off an item that is already 50% off != 80% off.
