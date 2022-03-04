# Power-BI-PL-300-Study-Guide
A study guide for the PL-300: Microsoft Power BI Data Analyst Certification Exam

# Introduction
The below is a study guide for the [PL-300: Microsoft Power BI Data Analyst certification exam](https://docs.microsoft.com/en-us/learn/certifications/exams/da-100), the exam to certify the recipient as a [Microsoft Certified: Power BI Data Analyst Associate](https://docs.microsoft.com/en-us/learn/certifications/data-analyst-associate/).

`The study guide and outline are current as of February 2022.`

# What this Document Contains
This document provides a checklist recreation of the Microsoft's current Skills Measured outline found [here](https://query.prod.cms.rt.microsoft.com/cms/api/am/binary/RE4qbu6). It is structured as follows:

## Section Header
#### Section Sub-Header
- Sub-section

Headers and sub-headers always link to the official Microsoft Learn path documentation (where it exists), while sub-sections link mostly to other Microsoft Documentation. In instances where MS Documentation is lacking, outside resources are used or the MS Learn page specific to the topic is linked. Additional resources are then added at the bottom of each section linking out to MS Learn labs and third-party resources. 

The document also contains references to [further reading and resources](#additional-resources--links), including tutorial videos, paid training (not ours), and the Dashboard in a Day project offered by Microsoft (free).

Lastly, the repo contains additional pages with more granular information on specific topics. These largely represent gaps the creator found in his own knowledge following one go-through of the MS Learn material. Use these as supplement, but do not treat them as comprehensive for their specific topic.

# How to Use this Document
Clone the repo. Then, begin with the Microsoft Learn track found [here](https://docs.microsoft.com/en-us/learn/certifications/data-analyst-associate/). It is the go-to source for all material covered by the exam. Use the outline's checkboxes to track progress and the links to return to sections in the future. 

To check off the sub-sections and headers, add an `x` between the brackets like so `[x]`. Example:
- [ ] Incomplete
- [x] Complete

We then recommend working with the supplemental material to solidify content. 

**NOTICE: Following the Microsoft Learn path is not enough. There is too much material to memorize in one go and content will not sink in without further practice and review. You *will* have to practice, and you will be revisiting content.**

# Additional Notes & Caveats
Unfortunately, Microsoft's Learn path and its outline are not a 1:1. This can manifest in several ways.

First, a sub-section in the outline may not have its own explicit page in the MS Learn path and may exist across several pages of content. E.g. `identify and connect to a data source` does not exist as a specific page in the MS Learn section for `Prepare the Data`, but rather as several pages tied to various data sources.  

Second, content for certain sub-sections in the outline may not be found within the indicated MS Learn section. We have tried to note this where possible.

Lastly, a section titled `Develop a data model` exists in the Outline, but has no corollary in the MS Learn track. In this case, informative content has been provided to the best of our ability. Several gaps surely remain, however, so please feel free to contribute.

# Resources for Colleagues (AzTech International)
See [this](https://drive.google.com/drive/u/1/folders/14mQNdzJjq_DcMgXNRPRdD8PjviCCVeqQ) folder for additional documentation. Contained are further details about the exam, a thorough list of DAX functions with descriptions, and a list of M functions with descriptions and examples.

# About the DA-100 / PL-300
- Duration: 180 Minutes.
- Question Types: Multiple choice and multi-response questions.
- Number of Questions: 45-50 multiple choice questions in section 1; ~4-5 questions each in 2-3 case studies.
- Score to Pass: 700/1000.

# The Skills Measured Outline
## [Prepare the Data (15-20%)](https://docs.microsoft.com/en-us/learn/paths/prepare-data-power-bi/)
### [Get data from different data sources](https://docs.microsoft.com/en-us/learn/modules/get-data/)
- [ ] [identify and connect to a data source](https://docs.microsoft.com/en-us/power-bi/connect-data/desktop-connect-to-data)
- [ ] [change data source settings](https://www.c-sharpcorner.com/article/how-to-change-data-source-of-existing-report-in-power-bi/)
- [ ] select a shared dataset or create a local dataset (See first bullet. Documentation contains various sections on connecting to different sets of data.)
- [ ] [select a storage mode](https://docs.microsoft.com/en-us/power-bi/transform-model/desktop-storage-mode)
- [ ] [use Microsoft Dataverse](https://docs.microsoft.com/en-us/learn/modules/dataverse-teams-power-bi/)
- [ ] [change the value in a parameter](https://docs.microsoft.com/en-us/power-query/power-query-query-parameters)
- [ ] [connect to a data flow](https://docs.microsoft.com/en-us/power-bi/transform-model/dataflows/dataflows-develop-solutions)

##### Additional Resources:
- [Lab: Prepare data in Power BI Desktop](https://docs.microsoft.com/en-us/learn/modules/get-data/lab-prepare)  
- [MS Documentation: Data sources in Power BI](https://docs.microsoft.com/en-us/power-bi/connect-data/desktop-data-sources)  
- [How To Change Data Source Of Existing Report In Power BI](https://www.c-sharpcorner.com/article/how-to-change-data-source-of-existing-report-in-power-bi/)

### [Clean, transform, and load the data](https://docs.microsoft.com/en-us/learn/modules/clean-data-power-bi/)
- [ ] [profile the data](https://docs.microsoft.com/en-us/power-query/data-profiling-tools)
- [ ] resolve inconsistencies, unexpected or null values, and data quality issues ([errors](https://docs.microsoft.com/en-us/power-query/dealing-with-errors#cell-level-error), [duplicates](https://docs.microsoft.com/en-us/power-query/working-with-duplicates))
- [ ] [identify and create appropriate keys for joins](https://docs.microsoft.com/en-us/power-query/merge-queries-overview)
- [ ] [evaluate and transform column data types](https://docs.microsoft.com/en-us/power-query/data-types), [also](https://docs.microsoft.com/en-us/power-query/best-practices#use-the-correct-data-types)
- [ ] [shape and transform tables (link provides first document in a series)](https://docs.microsoft.com/en-us/power-query/table-promote-demote-headers)
- [ ] combine queries: [append](https://docs.microsoft.com/en-us/power-query/append-queries), [merge (series)](https://docs.microsoft.com/en-us/power-query/merge-queries-overview)
- [ ] [apply user-friendly naming conventions to columns and queries](https://docs.microsoft.com/en-us/learn/modules/clean-data-power-bi/3-data-structure) (see bottom of article)
- [ ] [configure data loading](https://docs.microsoft.com/en-us/power-bi/connect-data/desktop-connect-to-data) (Recommend reading entire track starting here)
- [ ] [resolve data import errors](https://docs.microsoft.com/en-us/learn/modules/get-data/9-import-errors?ns-enrollment-type=LearningPath&ns-enrollment-id=learn-bizapps.data-preparation-in-power-bi)

##### Additional Resources:
- [Lab: Load data in Power BI Desktop](https://docs.microsoft.com/en-us/learn/modules/clean-data-power-bi/8-lab/?ns-enrollment-type=LearningPath&ns-enrollment-id=learn-bizapps.data-preparation-in-power-bi)

## [Model the Data (30—35%)](https://docs.microsoft.com/en-us/learn/paths/model-power-bi/)
### [Design a data model](https://docs.microsoft.com/en-us/learn/modules/design-model-power-bi/)
- [ ] [define the tables](https://docs.microsoft.com/en-us/power-bi/visuals/power-bi-visualization-tables)
- [ ] [configure table and column properties](https://docs.microsoft.com/en-us/power-bi/connect-data/desktop-shape-and-combine-data)
- [ ] [design and implement role-playing dimensions](https://towardsdatascience.com/role-playing-dimensions-in-power-bi-185dc58f90f1)
- [ ] [define a relationship's cardinality and cross-filter direction](https://docs.microsoft.com/en-us/power-bi/transform-model/desktop-relationships-understand)
- [ ] [design a data model that uses a star schema](https://docs.microsoft.com/en-us/power-bi/guidance/star-schema)
- [ ] [create a common date table](https://docs.microsoft.com/en-us/power-bi/guidance/model-date-tables)

##### Additional Resources:
- [Lab: Model data in Power BI Desktop, pt.1](https://docs.microsoft.com/en-us/learn/modules/design-model-power-bi/8-lab/?ns-enrollment-type=LearningPath&ns-enrollment-id=learn-bizapps.model-power-bi)  
- [Lab: Model data in Power BI Desktop, pt.2](https://docs.microsoft.com/en-us/learn/modules/design-model-power-bi/9-lab/?ns-enrollment-type=LearningPath&ns-enrollment-id=learn-bizapps.model-power-bi)

### Develop a data model 
Unfortunately this section does not appear in the MS Learn track, though its items are addressed elsewhere. Links have nevertheless been provided below to cover the topics.
- [ ] [create calculated tables](https://docs.microsoft.com/en-us/power-bi/transform-model/desktop-calculated-tables)
- [ ] [create hierarchies](https://spreadsheeto.com/power-bi-hierarchy/)
- [ ] [create calculated columns](https://docs.microsoft.com/en-us/power-bi/transform-model/desktop-tutorial-create-calculated-columns)
- [ ] [implement row-level security roles](https://docs.microsoft.com/en-us/learn/modules/row-level-security-power-bi/)
- [ ] [use the Q&A feature](https://docs.microsoft.com/en-us/power-bi/create-reports/power-bi-tutorial-q-and-a)

##### Additional resources:
- [Row-level security (RLS) with Power BI](https://docs.microsoft.com/en-us/power-bi/admin/service-admin-rls)
- [Use the Q&A visual](https://docs.microsoft.com/en-us/learn/modules/ai-visuals-power-bi/2-visual?ns-enrollment-type=LearningPath&ns-enrollment-id=learn-bizapps.data-analysis-power-bi)

### [Create model calculations by using DAX](https://docs.microsoft.com/en-us/learn/modules/create-measures-dax-power-bi/)
- [ ] [create basic measures by using DAX](https://www.red-gate.com/simple-talk/databases/sql-server/bi-sql-server/creating-measures-using-dax/)
- [ ] [use CALCULATE to manipulate filters](https://docs.microsoft.com/en-us/dax/best-practices/dax-avoid-avoid-filter-as-filter-argument)
- [ ] implement Time Intelligence using DAX: [List of functions](https://docs.microsoft.com/en-us/dax/time-intelligence-functions-dax), [Helpful Guide](https://www.red-gate.com/simple-talk/homepage/creating-time-intelligence-functions-in-dax/)
- [ ] [replace implicit measures with explicit measures](https://radacad.com/explicit-vs-implicit-dax-measures-in-power-bi)
- [ ] [use basic statistical functions](https://docs.microsoft.com/en-us/dax/statistical-functions-dax)
- [ ] [create semi-additive measures](https://www.sqlbi.com/articles/semi-additive-measures-in-dax/)
- [ ] [use quick measures](https://docs.microsoft.com/en-us/power-bi/transform-model/desktop-quick-measures)

##### Additional Resources:
- [Lab: Introduction to DAX in Power BI Desktop](https://docs.microsoft.com/en-us/learn/modules/create-measures-dax-power-bi/6-lab/?ns-enrollment-type=LearningPath&ns-enrollment-id=learn-bizapps.model-power-bi)
- [Lab: Time Intelligence and Measures in DAX](https://docs.microsoft.com/en-us/learn/modules/create-measures-dax-power-bi/8-lab/?ns-enrollment-type=LearningPath&ns-enrollment-id=learn-bizapps.model-power-bi)

### [Optimize model performance](https://docs.microsoft.com/en-us/learn/modules/optimize-model-power-bi/)
- [ ] [remove unnecessary rows and columns](https://docs.microsoft.com/en-us/power-bi/guidance/import-modeling-data-reduction)
- [ ] [identify poorly performing measures, relationships, and visuals](https://docs.microsoft.com/en-us/power-bi/guidance/power-bi-optimization)
- [ ] [reduce cardinality levels to improve performance](https://www.testpreptraining.com/tutorial/improve-cardinality-levels-by-changing-data-types-and-through-summarization/)

## [Visualize and Analyze the Data (25—30%)](https://docs.microsoft.com/en-us/learn/paths/visualize-data-power-bi/)
### [Create reports](https://docs.microsoft.com/en-us/learn/modules/visuals-power-bi/)
- [ ] [add visualization items to reports](https://docs.microsoft.com/en-us/power-bi/visuals/power-bi-report-add-visualizations-i)
- [ ] [choose an appropriate visualization type](https://docs.microsoft.com/en-us/power-bi/visuals/power-bi-visualization-types-for-reports-and-q-and-a)
- [ ] [format and configure visualizations](https://docs.microsoft.com/en-us/power-bi/visuals/service-getting-started-with-color-formatting-and-axis-properties)
- [ ] [use a custom visual](https://docs.microsoft.com/en-us/power-bi/developer/visuals/import-visual)
- [ ] [apply and customize a theme](https://docs.microsoft.com/en-us/power-bi/create-reports/desktop-report-themes)
- [ ] [configure conditional formatting](https://docs.microsoft.com/en-us/power-bi/create-reports/desktop-conditional-table-formatting)
- [ ] apply [slicing](https://docs.microsoft.com/en-us/power-bi/visuals/power-bi-visualization-slicers) and [filtering](https://docs.microsoft.com/en-us/power-bi/create-reports/power-bi-report-add-filter)
- [ ] [configure the report page](https://docs.microsoft.com/en-us/power-bi/create-reports/power-bi-report-display-settings)
- [ ] [use the Analyze in Excel feature](https://docs.microsoft.com/en-us/power-bi/collaborate-share/service-analyze-in-excel)  
- [ ] [choose when to use a paginated report](https://docs.microsoft.com/en-us/learn/modules/create-paginated-reports-power-bi/)

##### Additional Resources:
- [Lab: Design a report in Power BI Desktop](https://docs.microsoft.com/en-us/learn/modules/visuals-power-bi/8-lab/?ns-enrollment-type=LearningPath&ns-enrollment-id=learn-bizapps.visual-data-power-bi)
- [Lab: Create a paginated report](https://docs.microsoft.com/en-us/learn/modules/create-paginated-reports-power-bi/6-lab)

### [Create dashboards](https://docs.microsoft.com/en-us/learn/modules/create-dashboards-power-bi/)
- [ ] [manage tiles on a dashboard](https://docs.microsoft.com/en-us/power-bi/create-reports/service-dashboard-tiles)
- [ ] [configure mobile view](https://docs.microsoft.com/en-us/power-bi/create-reports/power-bi-create-mobile-optimized-report-about)
- [ ] [use the Q&A feature](https://docs.microsoft.com/en-us/power-bi/consumer/end-user-q-and-a)
- [ ] [add a Quick Insights result to a dashboard](https://docs.microsoft.com/en-us/power-bi/consumer/end-user-insights)
- [ ] [apply a dashboard theme](https://docs.microsoft.com/en-us/power-bi/create-reports/service-dashboard-themes)
- [ ] [pin a live report page to a dashboard](https://www.youtube.com/watch?v=QIVromazBw4)

##### Additional Resources:
- [Lab: Create a Power BI dashboard](https://docs.microsoft.com/en-us/learn/modules/create-dashboards-power-bi/9-lab/?ns-enrollment-type=LearningPath&ns-enrollment-id=learn-bizapps.visual-data-power-bi)
- [Use the Q&A visual](https://docs.microsoft.com/en-us/learn/modules/ai-visuals-power-bi/2-visual?ns-enrollment-type=LearningPath&ns-enrollment-id=learn-bizapps.data-analysis-power-bi)

### [Enhance reports for usability and storytelling](https://docs.microsoft.com/en-us/learn/modules/data-driven-story-power-bi/)
- [ ] [configure bookmarks](https://docs.microsoft.com/en-us/power-bi/create-reports/desktop-bookmarks?tabs=powerbi-desktop)
- [ ] [create custom tooltips](https://docs.microsoft.com/en-us/power-bi/create-reports/desktop-tooltips)
- [ ] [edit and configure interactions between visuals](https://docs.microsoft.com/en-us/power-bi/create-reports/service-reports-visual-interactions)
- [ ] [configure navigation for a report](https://docs.microsoft.com/en-us/power-bi/create-reports/button-navigators?tabs=powerbi-desktop)
- [ ] [apply sorting](https://docs.microsoft.com/en-us/power-bi/consumer/end-user-change-sort)
- [ ] [configure Sync Slicers](https://docs.microsoft.com/en-us/power-bi/visuals/power-bi-visualization-slicers#sync-and-use-slicers-on-other-pages)
- [ ] [group and layer visuals by using the selection pane](https://docs.microsoft.com/en-us/power-bi/create-reports/desktop-grouping-visuals#:~:text=To%20create%20a%20group%20of,displayed%20in%20the%20Selection%20pane.)
- [ ] [drilldown into data using interactive visuals](https://docs.microsoft.com/en-us/power-bi/consumer/end-user-drill)
- [ ] [export report data](https://docs.microsoft.com/en-us/power-bi/visuals/power-bi-visualization-export-data?tabs=dashboard)
- [ ] [design reports for mobile devices](https://docs.microsoft.com/en-us/power-bi/create-reports/power-bi-create-mobile-optimized-report-mobile-layout-view?tabs=powerbi-desktop)

##### Additional Resources:
- [Lab: Enhance Power BI reports with slicers, interaction, and formatting](https://docs.microsoft.com/en-us/learn/modules/data-driven-story-power-bi/13-lab/?ns-enrollment-type=LearningPath&ns-enrollment-id=learn-bizapps.visual-data-power-bi)

### [Identify patterns and trends](https://docs.microsoft.com/en-us/learn/modules/perform-analytics-power-bi/)
- [ ] [use the Analyze feature in Power BI](https://docs.microsoft.com/en-us/power-bi/consumer/end-user-analyze-visuals)
- [ ] [identify outliers](https://community.powerbi.com/t5/Community-Blog/How-To-Detect-Anomalies-And-Outliers-In-Your-Data/ba-p/470789)
- [ ] [choose between continuous and categorical axes](https://community.powerbi.com/t5/Desktop/what-do-the-continuous-and-categorical-type-options-on-the-x/m-p/67223/highlight/true#M27855)
- [ ] use [groupings, binnings](https://docs.microsoft.com/en-us/power-bi/create-reports/desktop-grouping-and-binning), and [clustering](https://powerbi.microsoft.com/en-us/blog/power-bi-desktop-november-feature-summary/#clustering)
- [ ] [use AI visuals (this is its own section in the MS Learn track)](https://docs.microsoft.com/en-us/learn/modules/ai-visuals-power-bi/)
- [ ] [use the Forecast feature](https://docs.microsoft.com/en-us/power-bi/transform-model/desktop-analytics-pane#apply-forecasting)
- [ ] [create reference lines by using the Analytics pane](https://docs.microsoft.com/en-us/power-bi/transform-model/desktop-analytics-pane)

##### Additional Resources:
- [Lab: Perform data analysis in Power BI Desktop](https://docs.microsoft.com/en-us/learn/modules/ai-visuals-power-bi/5-lab?ns-enrollment-type=LearningPath&ns-enrollment-id=learn-bizapps.data-analysis-power-bi)

## [Deploy and Maintain Assets (20—25%)](https://docs.microsoft.com/en-us/learn/paths/manage-workspaces-datasets-power-bi/)
### [Manage files and datasets](https://docs.microsoft.com/en-us/learn/modules/manage-datasets-power-bi/)
- [ ] [identify when a gateway is required](https://docs.microsoft.com/en-us/power-bi/connect-data/service-gateway-deployment-guidance)
- [ ] [configure a dataset scheduled refresh](https://docs.microsoft.com/en-us/power-bi/connect-data/refresh-scheduled-refresh)
- [ ] [configure row-level security group membership](https://docs.microsoft.com/en-us/power-bi/admin/service-admin-rls)
- [ ] [provide access to datasets](https://docs.microsoft.com/en-us/power-bi/connect-data/service-datasets-build-permissions)
- [ ] [manage global options for files](https://www.oreilly.com/library/view/microsoft-power-bi/9781788290142/3268569d-441d-41b7-9594-d0776568b703.xhtml)
### [Manage workspaces](https://docs.microsoft.com/en-us/learn/modules/create-manage-workspaces-power-bi/)
- [ ] [create and configure a workspace](https://docs.microsoft.com/en-us/power-bi/collaborate-share/service-create-the-new-workspaces)
- [ ] [assign workspace roles](https://docs.microsoft.com/en-us/power-bi/collaborate-share/service-give-access-new-workspaces)
- [ ] [configure and update a workspace app](https://docs.microsoft.com/en-us/power-bi/collaborate-share/service-create-distribute-apps)
- [ ] publish, import, or update assets in a workspace
- [ ] [apply sensitivity labels to workspace content](https://docs.microsoft.com/en-us/power-bi/admin/service-security-apply-data-sensitivity-labels)
- [ ] configure [subscriptions](https://docs.microsoft.com/en-us/power-bi/consumer/end-user-subscribe) and [data alerts](https://docs.microsoft.com/en-us/power-bi/consumer/end-user-alerts)
- [ ] [promote or certify Power BI content](https://docs.microsoft.com/en-us/power-bi/collaborate-share/service-endorsement-overview)

##### Additional Resources:
- [A quick summary on Workspaces, Roles, and Licensing](https://github.com/user905/PL-300-Personal-Study-Guide/blob/main/Understanding%20Workspaces%2C%20Roles%2C%20and%20Licensing.md)  

# Additional Resources & Links
- [Udemy Course](https://www.udemy.com/course/70-778-analyzing-and-visualizing-data-with-power-bi/)
  - Price: ~$20 (price may vary over time)
  - Offering: A complete course of all PBI content.
- [Official Practice Test (Current test exam is for the DA-100)](https://www.mindhub.com/da-100-analyzing-data-with-microsoft-power-bi-microsoft-official-practice-test/p/MU-DA-100?utm_source=microsoft&utm_medium=certpage&utm_campaign=AZLearnerJourney)
  - Price: $99-109 (for 30 & 60 day availability, respectively)
  - Offering: Practice test meant to mimic the exam format.
- [Learn Data Insights](https://learndatainsights.com/data-analyst/analysing-data-with-microsoft-power-bi-da-100%e2%80%8b/)  
  - Price: Free
  - Offering: Questions w/ explanations & links to resources when answers are incorrect.
- [Microsoft's Dashboard in a Day Project](https://powerbi.microsoft.com/en-us/diad/)
  - Price: Free
  - Offering: Materials for constructing dashboards like a professional, including tutorials and sample data
- [Guy In a Cube (YouTube)](https://www.youtube.com/channel/UCFp1vaKzpfvoGai0vE5VJ0w)
- [Curbal (YouTube)](https://www.youtube.com/channel/UCJ7UhloHSA4wAqPzyi6TOkw)

##### Other Resources (Unvetted)
- [Magna Data Solutions](https://magnadatasolutions.com/practice-da100-exam/)
  - Price: Free
  - Offering: Exam tips video & questions
- [Sky Point CSG](https://www.csgpro.com/diad-instructional-videos/?submissionGuid=9a532666-5e9f-4b88-bc58-eac52f89db4e)
  - Price: Free
  - Offering: Video walkthrough of Microsoft's Dashboard in a Day project
- [BI Elite Training DA-100 Exam Prep – Power BI Certification](https://training.bielite.com/courses/da-100-exam-prep-power-bi-certification/)  
  - Price: $29USD
  - Offering: Live Azure database, 30+ DA-100 Practice Exam Questions, Many hours of premium video tutorials from a Microsoft MVP
  – Free Trial? Yes. 7 day.
