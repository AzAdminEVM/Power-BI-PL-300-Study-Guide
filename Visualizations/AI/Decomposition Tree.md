# [Decomposition Tree](https://docs.microsoft.com/en-us/power-bi/visuals/power-bi-visualization-decomposition-tree)
The decomposition tree visual in Power BI lets you visualize data across multiple dimensions. It automatically aggregates data and enables drilling down into your 
dimensions in any order. 

<p align="center"><img src="https://user-images.githubusercontent.com/29554021/156380655-afe6e43b-d261-4397-87b8-5fca92c0a356.png" width=600></p>

The visualization requires two types of input:
- Analyze: the metric you would like to analyze. This has to be a measure or an aggregate.
- Explain By: one or more dimensions you would like to drill down into.

Once fields have been added to `Explain By`, click the '+' and pick what you want to explain by:
<p align="center"><img src="https://user-images.githubusercontent.com/29554021/156381348-97c1b1e3-c589-417a-81f9-2a3f20164749.png" width=600></p>

### [AI Splits](https://docs.microsoft.com/en-us/power-bi/visuals/power-bi-visualization-decomposition-tree#ai-splits)
You can use “AI Splits” to figure out where you should look next in the data. These splits appear at the top of the list and are marked with a lightbulb. 
The splits are there to help you find high and low values in the data, automatically. 

The analysis can work in two ways depending on your preferences. The default behavior is as follows:
- High Value: Considers all available fields and determines which one to drill into to get the highest value of the measure being analyzed.
- Low Value: Considers all available fields and determines which one to drill into to get the lowest value of the measure being analyzed.

Here's an example. Note the Lightbulb on the far right column header. That means an AI split was requested:
<p align="center"><img src="https://user-images.githubusercontent.com/29554021/156382104-f0cfdee1-2411-450e-9075-d9a27c349595.png" width=600></p>

You can configure the visual to find Relative AI splits as opposed to Absolute ones. Relative mode looks for high values that stand out compared to the rest of 
the data in the column.

<p align="center"><img src="https://user-images.githubusercontent.com/29554021/156382922-ea2ce3ac-b0f7-4132-b3f4-a06e710a9c1b.png" width=600></p>

##### Miscellaneous & Limitations
- Designers can 'lock levels', forcing consumers down certain paths in the decomposition tree
<p align="center"><img src="https://user-images.githubusercontent.com/29554021/156383232-b2276697-235c-4436-9dbd-f03d7ab78473.png" width=600></p>

- The decomposition tree is not supported in On-premises Analysis Services
- AI splits are not supported in the following scenarios: 
  - Azure Analysis Services
  - Power BI Report Server
  - Publish to Web
  - Complex measures and measures from extensions schemas in 'Analyze'



