# [Using the Q&A Visual](https://docs.microsoft.com/en-us/learn/modules/ai-visuals-power-bi/2-visual?ns-enrollment-type=LearningPath&ns-enrollment-id=learn-bizapps.data-analysis-power-bi)

`Notice: This is a personal study file. It assumes a certain familiarity with the topic and therefore DOES NOT contain everything about Power BI Q&A. The author created this to track more technical gotchas that might appear in the PL-300 exam.`

The Q&A Visual can be added as both an item on a canvas and as a button. Adding it as a button saves space. Designers can add it to reports. Dashboards have the Q&A box automatically if it is enabled in the settings in the PBI service.

It allows users to query data, create visuals when doing so, and train it to improve via the [Q&A tooling](https://docs.microsoft.com/en-us/power-bi/natural-language/q-and-a-tooling-intro). It works best when the data is normalized and well-modeled.

- The Q&A visualization consists of the following four core components:
  - The question box, where users enter their question and are shown suggestions to help them complete the question.
  - A pre-populated list of suggested questions.
  - An icon that users can select to convert the Q&A visual into a standard visual.
  - An icon that users can select to open Q&A tooling, which allows designers to configure the underlying natural language engine. When entering natural language queries with Power BI Q&A, you can specify the visual type in your query.

Once the visual is created, it supports: Cross Highlighting, Bookmarks, Cross Filtering. Report Page Tooltips are only available once the visual is converted into a standard visual


## [Technical Details](https://docs.microsoft.com/en-us/power-bi/natural-language/q-and-a-data-sources)
Q&A is supported in the following configurations:
- Import mode
- Live connect mode – Using on-premises SQL Server Analysis Services, Azure Analysis Services, or Power BI datasets
- Direct Query – Azure Synapse, Azure SQL, and SQL Server 2019. Although other sources may work in direct query mode, we do not officially support these sources.

By default, Q&A is enabled inside a report if you use the Q&A visual. A prompt will appear if you're using Direct Query or Live connect. 
You can explicitly turn on/off the natural language capabilities for a report by going into options. When enabled, Q&A builds an index to speed querying.

<p align="center"><img width=400 src="https://user-images.githubusercontent.com/29554021/154740600-c9a5c361-f53a-49a0-b8d6-175838839617.png" /></p>

## [Be sure your data is properly modeled](https://docs.microsoft.com/en-us/power-bi/natural-language/q-and-a-best-practices)
Here are the primary suggestions:
1. Add missing relationships
2. Pick sensible column & table names
3. Fix incorrect data types. Date & number types are particularly susceptible to mis-categorization.
4. Power BI tries by default to summarize numeric columns. Therefore be sure `Summarization` is set to `Don't Summarize` for year & identifier columns. (see image below)
5. Choose a Data Category for each date and geography column (see image below)
6. Choose a Sort By Column for relevant columns
7. [Normalize your model](https://docs.microsoft.com/en-us/power-bi/natural-language/q-and-a-best-practices#normalize-your-model)

Data Category & Summarization settings:  
<img width=400 src="https://user-images.githubusercontent.com/29554021/154742223-e3e80907-4b2a-44f4-bc14-fe00b3288a34.png" />


#### Miscellaneous
- Your own Pages can be used as an answer to certain questions. To do so, go to the Page in question > Visualization > Format > Page Information > Toggle Q&A > Then add alternate names.  

<p align="center"><img width="146" alt="image" src="https://user-images.githubusercontent.com/29554021/155398080-4f582bac-7b7b-4e34-a467-c9f40c0faf01.png"></p>


