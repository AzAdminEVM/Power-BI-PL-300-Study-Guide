# [Visual Tooltips](https://docs.microsoft.com/en-us/power-bi/create-reports/desktop-tooltips?WT.mc_id=DP-MVP-5003635)
`Notice: This is a personal study file. It assumes a certain familiarity with the topic and therefore DOES NOT contain everything about this topic. The author created this to track high-level notes and technical gotchas that might appear in the PL-300 exam.`

You can create visually rich report tooltips that appear when you hover over visuals, based on report pages you create in Power BI Desktop. By creating a report page that serves as your tooltip, your custom tooltips can include visuals, images, and any other collection of items you create in the report page.

<p align="center"><img src="https://user-images.githubusercontent.com/29554021/154760916-530caec2-95a8-48f7-a7a5-425214103319.png" width=400 /></p>

Each tooltip page can be associated with one or more fields in your report, so that when you hover over a visual that includes the selected field, the tooltip you created on your tooltip page appears, filtered by the datapoint over which your mouse is hovering.

## Steps
### To make a tooltip automatically appear:
1. Create a new page and adjust the Page size to `tooltip` (Visualizations pane).

<p align="center"><img src="https://user-images.githubusercontent.com/29554021/154761384-a98f10d0-a582-4786-9252-d6e0e322baf5.png" width=400 /></p>

2. To see its size, go to View > Page View > Actual Size

<p align="center"><img src="https://user-images.githubusercontent.com/29554021/154761533-f74a4d77-8868-46f8-8aab-2775d0c9c2c8.png" width=400 /></p>

3. Configure the page as a tooltip page: Visualization Pane > Formatting > Page information > Tooltip > on

<p align="center"><img src="https://user-images.githubusercontent.com/29554021/154761628-d3ff8d27-494d-49a0-ae3e-94d91adc0c61.png" width=400 /></p>

4. Specify the fields for which the tooltip should appear: Drap/Drop fields into Visualization Pane > Tooltip bucket

<p align="center"><img src="https://user-images.githubusercontent.com/29554021/154761748-d2705db6-35fd-41a5-99d7-2195269c7fa1.png" width=400 /></p>

### To make a tooltip manually appear:
To set a tooltip manually, select the visual for which you want to specify the manual tooltip, then in the Visualizations pane, select the Format section and expand the Tooltip card. Then, select the page to use as a tooltip:

<p align="center"><img src="https://user-images.githubusercontent.com/29554021/154761897-bd10d20f-3a19-48a6-8940-6ed088b29417.png" width=400 /></p>

Uses:
- Set a blank page for a tooltip to override the default Power BI tooltip selection. 
- Use when you don't want the tooltip that is automatically selected by Power BI to be the tooltip. For example, if you have a visual that includes two fields, and both of those fields have an associated tooltip, Power BI selects only one to show. You might not want that to be the case, so you could manually select which tooltip should be displayed.

### Additional Considerations
- When a report tooltip is displayed for a line chart, only one tooltip for all lines in the chart is displayed. This is similar to the default tooltip behavior for line charts, which also displays only one tooltip.
- When a visual is being cross-highlighted in a report, report tooltips always show the cross-highlighted data, even if you're hovering over the faded section of the data point.
- Button visuals also support tooltips.





