# [Clustering](https://powerbi.microsoft.com/en-us/blog/power-bi-desktop-november-feature-summary/#clustering)

`Notice: This is a personal study file. It assumes a certain familiarity with the topic and therefore DOES NOT contain everything about this topic. The author created this to track more technical gotchas that might appear in the PL-300 exam.`

You can use clustering on your scatter chart by clicking the “…” and then selecting Automatically find clusters:
<p align="center"><img src="https://user-images.githubusercontent.com/29554021/156251242-cfe4d8b0-3e93-45c9-8a5f-fe4e575f9a10.png" width=400 /></p>

When you select this, a dialog opens where you can decide how many clusters you want us to find. If you leave it blank, we will automatically find the number of 
clusters we think makes the most sense with your data.

After the clustering algorithm runs, we will create a new categorical field with the different cluster groups in it. This new field will be adding to your scatter 
chart’s legend field well bucket, which you can now use as a source of cross highlighting like any other legend field. You can also find it in your field list and 
use it in new visuals just like any other field.

These are editable by right-clicking the newly created measure in the fields list and select Edit Cluster.

<p align="center"><img src="https://user-images.githubusercontent.com/29554021/156251560-6b429d12-da68-4680-abde-8da0aac33b47.png" width=400 /></p>

##### Limitations
- Hierarchies cannot be clustered. E.g. If you've got a date hierarchy – Year, Quarter, Month – in the X Axis, the scatter plot cannot be clustered.

# [Binning & Grouping](https://docs.microsoft.com/en-us/power-bi/create-reports/desktop-grouping-and-binning)
Grouping is for categorical data, binning for numberic.  

#### Grouping
Select multiple `categories` from a chart, right-click, Group data:
<p align="center"><img src="https://user-images.githubusercontent.com/29554021/156254632-bc8522e5-7879-4b2a-a549-03e3e4473662.png" width=400 /></p>

This creates a new field in the field panel and places that into the visualization's legend well, separating the selected categories with a new color.

#### Binning
You can set the bin size for numerical and time fields in Power BI Desktop. You can make bins for calculated columns, but not for measures. Use binning to right-size the data that Power BI Desktop displays.

Right-click a field > New Group:
<p align="center"><img src="https://user-images.githubusercontent.com/29554021/156255357-56065fc5-44dc-4898-9969-4475102bb8e4.png" width=400 /></p>
