# Queries

`Notice: This is a personal study file. It assumes a certain familiarity with the topic and therefore DOES NOT contain everything about this topic. 
The author created this to track more technical gotchas that might appear in the PL-300 exam.`

The below assumes a certain knowledge about the M Language. It does not attempt to teach M, but to explain the processes involved in querying data.

## [Query Evaluation](https://docs.microsoft.com/en-us/power-query/query-folding-basics)
A brief overview of how M queries are processed.

<p align="center"><img src="https://user-images.githubusercontent.com/29554021/154755849-4f2fe892-932f-4c21-8714-b1a1225bb0ce.png" width=600 /></p>
(Source does not need to be SQL...)

When Power Query reads your M script, it runs the script through an optimization process to more efficiently evaluate your query. In this process, it determines 
which steps (transforms) from your query can be offloaded to your data source. It also determines which other steps need to be evaluated using the Power Query 
engine. This optimization process is called `query folding`, where Power Query tries to push as much of the possible execution to the data source to optimize your 
query's execution.

Furthermore, when multiple sources are involved, the data privacy level of each data source is taken into consideration when evaluating the query.

## [Query Folding](https://docs.microsoft.com/en-us/power-query/query-folding-basics#query-folding-overview)
`Note: Queries that rely solely on unstructured data sources or that don't have a compute engine, such as CSV or Excel files, don't have query folding capabilities. This means that Power Query evaluates all the required data transformations using the Power Query engine.`

The goal of query folding is to offload or push as much of the evaluation of a query to a data source that can compute the transformations of your query.

The query folding mechanism accomplishes this goal by translating your M script to a language that can be interpreted and executed by your data source. 
It then pushes the evaluation to your data source and sends the result of that evaluation to Power Query.

This operation often provides a much faster query execution than extracting all the required data from your data source and running all transforms required in 
the Power Query engine.

Depending on how the query is structured, there could be three possible outcomes to the query folding mechanism:
- Full query folding: When all of your query transformations get pushed back to the data source and minimal processing occurs at the Power Query engine.
- Partial query folding: When only a few transformations in your query, and not all, can be pushed back to the data source. In this case, only a subset of your transformations is done at your data source and the rest of your query transformations occur in the Power Query engine.
- No query folding: When the query contains transformations that can't be translated to the native query language of your data source, either because the transformations aren't supported or the connector doesn't support query folding. For this case, Power Query gets the raw data from your data source and uses the Power Query engine to achieve the output you want by processing the required transforms at the Power Query engine level.

[Here](https://docs.microsoft.com/en-us/power-query/query-folding-examples) are examples of each.
