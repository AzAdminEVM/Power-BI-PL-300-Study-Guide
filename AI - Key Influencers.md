# AI - Key Influencers Visualization

`Notice: This is a personal study file. It assumes a certain familiarity with the topic and therefore DOES NOT contain everything about this topic. 
The author created this to track high-level notes and technical gotchas that might appear in the PL-300 exam.`

[Source](https://docs.microsoft.com/en-us/power-bi/visuals/power-bi-visualization-influencers#interpret-the-results-key-influencers)

Quick Summary: The key influencers visual helps you understand the factors that drive a metric you're interested in. It analyzes your data, ranks the factors that matter, and displays them as key influencers. For example, suppose you want to figure out what influences employee turnover, which is also known as churn. One factor might be employment contract length, and another factor might be commute time.


### The Visual
<p align="center"><img src="https://user-images.githubusercontent.com/29554021/155154342-982cf1cd-1b40-4a96-99f9-6db1251266a6.png" width=400/></p>

It has two primary views:
- `Key Influencers`: assess each factor individually
- `Top Segments`: see how a combination of factors affects the metric that you're analyzing

Both are used to show how `influencers` (fields placed in the `Explain by` bin) affect a factor. Influencers can be of several types:
- categorical (eg. red, yellow, green)
- continuous (eg. age)
- measures & aggregates (eg. count of customer support tickets)

The analyzed factor can be either categorical or numeric.

<p align="center"><img width="400" alt="image" src="https://user-images.githubusercontent.com/29554021/155156552-ccd612bb-cb01-480f-b39e-ef9971528afc.png"/></p>

The `Explain By` fields need not be in the same Table as the analyzed field, but relationships to that field must exist, and influencer fields must be defined at the same level of granularity. `Aggregations are required for one-to-many relationships.` See [here](https://docs.microsoft.com/en-us/power-bi/visuals/power-bi-visualization-influencers#analyze-a-metric-that-is-categorical) and [here](https://docs.microsoft.com/en-us/power-bi/visuals/power-bi-visualization-influencers#interpret-measures-and-aggregates-as-key-influencers)

##### Continuous Influencers > Scatter Plots
The visual on the right need not be a bar graph. See the example of how a continuous influencer changes things. The visualization shows that every time tenure goes up by a standard amount, eg. 13.44 months (the standard deviation of the Tenure field), on average the likelihood of a low rating increases by 1.23 times:
<p align="center"><img width="400" alt="image" src="https://user-images.githubusercontent.com/29554021/155161610-ccd5feb0-cb69-4071-a226-c33d780a98b5.png"/></p>

#### [Top Segments](https://docs.microsoft.com/en-us/power-bi/visuals/power-bi-visualization-influencers#interpret-the-results-top-segments)
<p align="center"><img width="400" alt="image" src="https://user-images.githubusercontent.com/29554021/155163903-fec8f73a-a72a-401a-a572-46d4a6dc758e.png"/></p>

These segments are ranked by the percentage of low ratings within the segment. Segment 1, for example, has 74.3% customer ratings that are low. 
- The higher the bubble, the higher the proportion of low ratings. 
- The size of the bubble represents how many customers are within the segment.
  
Selecting a bubble displays the details of that segment. 

<p align="center"><img width="400" alt="image" src="https://user-images.githubusercontent.com/29554021/155164219-5079c2cc-9192-4b55-b7e4-7e66bc63b9dc.png"/></p>

In this group:
- 74.3% of the customers gave a low rating. 
- The average customer gave a low rating 11.7% of the time, so this segment has a larger proportion of low ratings. It's 63 percentage points higher. 
- Segment 1 also contains approximately 2.2% of the data, so it represents an addressable portion of the population.

#### [Analyzing Numeric Metrics](https://docs.microsoft.com/en-us/power-bi/visuals/power-bi-visualization-influencers#interpret-the-results-key-influencers)
If you move an unsummarized numerical field into the Analyze field, you have a choice how to handle that scenario:
- Categorical Analysis Type (Eg. ‘What influences Survey Scores to be 1?’)
- Continuous Analysis Type (Eg. ‘What influences Survey Scores to increase/decrease?’)

Continuous is helpful when lots of unique values exist in the table, like, eg. housing prices. Here we can see the increase:
<p align="center"><img width="1200" alt="image" src="https://user-images.githubusercontent.com/29554021/155170196-3e826b5f-11e6-43c5-9a5e-35be363c0db3.png"/></p>


Results are similar, with two key differences (note: changes apply to the scatter plot as well, i.e. when influencers are continuous):
- The column chart on the right is looking at the averages rather than percentages.
- The number in the bubble is still the difference between the red dotted line and green bar but it’s expressed as a number ($158.49K) rather than a likelihood (1.93x).

Note this example is for the key influencers part of the visual. There are further changes with the top segments component as well.

#### [Analyzing Metric that are Measures or Summarized Columns](https://docs.microsoft.com/en-us/power-bi/visuals/power-bi-visualization-influencers#analyze-a-metric-that-is-a-measure-or-a-summarized-column)
These default to continuous and cannot be changed. The biggest difference between analyzing a measure/summarized column and an unsummarized numeric column is the level at which the analysis runs. For summarized data the level of analysis is defined in the `Explain By` well.

Imagine we have three fields in Explain By we are interested in: Kitchen Quality, Building Type and Air Conditioning. Average House Price (the measure to analyze) would be calculated for each unique combination of those three fields. It is often helpful to switch to a table view to take a look at what the data being evaluated looks like.

<p align="center"><img width="400" alt="image" src="https://user-images.githubusercontent.com/29554021/155173293-da3a86b5-9113-466a-ad2b-f6ae6b465057.png"/></p>

This analysis is very summarized and so it will be hard for the regression model to find any patterns in the data it can learn from. The solution is to run the analysis at a more detailed level.

To analyze the house price at the house level, you must explicitly add the ID field to the analysis. Nevertheless, we don't want the house ID to be considered an influencer. It is not helpful to learn that as house ID increases, the price of a house increase. This is where the Expand By field well option comes in handy. `Use Expand By to add fields you want to use for setting the level of the analysis *without looking for new influencers*.`

Final Note: Measures and aggregates are by default analyzed at the table level. If there were a measure for average monthly spending (for a customer table), it would be analyzed at the customer table level. If the customer table doesn't have a unique identifier, you can't evaluate the measure and it's ignored by the analysis.


### Miscellaneous
- Select the `Only show values that are influencers` check box to filter by using only the influential values. 
<p align="center"><img width="400" alt="image" src="https://user-images.githubusercontent.com/29554021/155160817-7f6a9544-1da9-4bc1-92be-6052609103a3.png"/></p>
  
- Sometimes continuous influencers have a non-linear effect. In this case, the visual may apply binning (max 5 bins), turning the influencer categorical.  
  
- Enable Counts: Certain influencers may have a high effect, but might represent a small proportion of the data. Enable counts to display rings around the influencer circles. The size of the rings represents the approximate percentage of data that influencer contains. The more of the bubble the ring circles, the more data it contains.
  - Sort by: allows you to sort by count first instead of impact.
  - Having a full ring around the circle means the influencer contains 100% of the data. `You can change the count type to be relative to the maximum influencer using the Count type dropdown in the Analysis card of the formatting pane.` Now the influencer with the most amount of data will be represented by a full ring and all other counts will be relative to it.

<p align="center"><img width="400" alt="image" src="https://user-images.githubusercontent.com/29554021/155178504-0a9c4f19-38ce-458a-a186-93994e9e5281.png"/></p>

- When analyzing a numeric or categorical column, the analysis always runs at the table level. For example, if you are analyzing house prices and your table contains an ID column, the analysis will automatically run at the house ID level. When you are analyzing a measure or summarized column, you need to explicitly state at which level you would like the analysis to run at.

### Limitations
- `Does not support DirectQuery`
- Live Connection to Azure Analysis Services and SQL Server Analysis Services is not supported
- Publish to web is not supported
- .NET Framework 4.6 or higher is required
- SharePoint Online embedding isn't supported
- We recommend that you have at least 100 observations for the selected state (eg. the state is customers who churn). You also need at least 10 observations for the states you use for comparison (eg. customers who don't churn)

