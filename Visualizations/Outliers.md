`Notice: This is a personal study file. It assumes a certain familiarity with the topic and therefore DOES NOT contain everything about this topic. The author created this to track more technical gotchas that might appear in the PL-300 exam.`

# Outliers
Typically easiest to find in a scatter plot with two measures compared against one another. There is no magic formula to identify these, however. Look at the data at various granularities and identify them manually.

You can also use DAX. E.g.:
```
Outliers =
CALCULATE (
    [Order Qty],
    FILTER (
        VALUES ( Product[Product Name] ),
        COUNTROWS ( FILTER ( Sales, [Order Qty] >= [Min Qty] ) ) > 0
    )
)
```

See [here](https://docs.microsoft.com/en-us/learn/modules/perform-analytics-power-bi/3-visuals) for more details.


