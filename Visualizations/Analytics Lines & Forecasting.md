# [Analytics Pane](https://docs.microsoft.com/en-us/power-bi/transform-model/desktop-analytics-pane)

`Notice: This is a personal study file. It assumes a certain familiarity with the topic and therefore DOES NOT contain everything about this topic. The author created this to track more technical gotchas that might appear in the PL-300 exam.`

With the Analytics pane in Power BI Desktop, you can add dynamic reference lines to visuals, and provide focus for important trends or insights. 
If you have time data in your data source, you can use the forecasting feature. Just select a visual, then expand the Forecast section of the Analytics pane.
The Analytics icon and pane is found in the Visualizations area of Power BI Desktop.

<p align="center"><img src="https://user-images.githubusercontent.com/29554021/156247250-f8cd0703-32c8-48b0-8e58-c8bd7a8393dd.png" width=600/></p>

Types of lines:
- X-Axis constant line
- Y-Axis constant line
- Min line
- Max line
- Average line
- Median line
- Percentile line
- Symmetry shading
- Forecast (if data contains time and using a line chart)

Symmetry Shading creates a line with two shades on either side. The line represents where the X & Y value are the same:
<p align="center"><img src="https://user-images.githubusercontent.com/29554021/156248607-8bf34c8c-db3d-40a5-bcbb-ce22368d216b.png" width=400/></p>


### Miscellaneous & Limitations
- Not all charts have all lines available. E.g. Stacked charts only allow constant lines. See [here](https://docs.microsoft.com/en-us/power-bi/transform-model/desktop-analytics-pane#considerations-and-limitations) for details.



