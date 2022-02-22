# DirectQuery

- Ideal for large data sets, where users need access to the latest data.
- Pitfalls are that it limits Power Query & DAX, including calculated tables
- Q&A is available for on-prem data, but a gateway must be established
- Slow because:
  - Each interaction with report (e.g. slicing/cross-filtering) requires a query back to the source to be calculated
  - Complex DAX has to be translated into source query languages (e.g. SQL)
  - Data Aggregations have to be performed at source rather than being done by DAX
