# [The Analyze Feature](https://docs.microsoft.com/en-us/power-bi/consumer/end-user-analyze-visuals)
Often in report visuals, you see a large increase and then a sharp drop in values, and wonder about the cause of such fluctuations. With Analyze in the Power BI service, you can learn the cause with just a few clicks.

The details returned by insights are intended to highlight what was different between the two time periods, to help you understand the change between them.

On a graph, right-click a point > Analyze > Explain the [increase/decrease]. 
Available for 1) Power BI service for business users, and 2) Power BI service for designers & developers.

<p align="center"><img src="https://user-images.githubusercontent.com/29554021/156377533-fdf5b05a-7c28-4838-8a6a-c155776adff0.png" width=400></p>

Here are the results:
<p align="center"><img src="https://user-images.githubusercontent.com/29554021/156377635-f77416a2-a46f-439c-ad63-0b0ec7264ea2.png" width=400></p>

There are four visuals that can be displayed:
- Scatter Plot: shows the value of the measure in the first period (on the x-axis) against the value of the measure in the second period (on the y-axis)
- 100% Stacked Column: shows the value of the contribution to the total
- Ribbon: shows the value of the measure before and after
- Waterfall: show actual increases or decreases between the periods

### Add to Page
<p align="center"><img src="https://user-images.githubusercontent.com/29554021/156377780-a67b2903-b6d1-4a80-8efe-1d65051be0a1.png" width=400></p>

##### Limitations
The following list is the collection of currently unsupported scenarios for Analyze - explain the increase/decrease/difference:
- TopN filters
- Include/exclude filters
- Measure filters
- Non-numeric measures
- Use of "Show value as"
- Filtered measures - filtered measures are visual level calculations with a specific filter applied (for example, Total Sales for France), and are used on some of the visuals created by the insights feature
- Categorical columns on X-axis unless it defines a sort by column that is scalar. If using a hierarchy, then every column in the active hierarchy has to match this condition
- RLS or OLS enabled data models


