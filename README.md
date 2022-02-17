# Power-BI-PL-300-Study-Guide
A study guide for the PL-300: Microsoft Power BI Data Analyst Certification Exam

# Introduction
This repo contains a study guide for the [PL-300: Microsoft Power BI Data Analyst certification exam](https://docs.microsoft.com/en-us/learn/certifications/exams/da-100), the exam to certify the recipient as a [Microsoft Certified: Power BI Data Analyst Associate](https://docs.microsoft.com/en-us/learn/certifications/data-analyst-associate/).

`Document is current as of February 2022.`

# What this Document Contains

First and foremost is the current Skills Measured outline found [here](https://query.prod.cms.rt.microsoft.com/cms/api/am/binary/RE4qbu6). This has been recreated below as a checklist first, and then as an [outline](#the-skills-measured-outline). The structure for the is as follows:

### Section Header
##### Section Sub-Header
- Sub-section

Headers and sub-headers always link to the official Microsoft Learn path documentation (where it exists), while sub-sections link mostly to other Microsoft Documentation. In instances where MS Documentation is lacking, outside resources are used. Additional resources are then added at the bottom of each seaction linking out to MS Learn labs and third-party resources. 

The document also contains references to [further reading and resources](#additional-resources--links), including tutorial videos, paid training (not ours), and the Dashboard in a Day project offered by Microsoft (free).

# How to Use this Document
Clone the repo. Then, begin with the Microsoft Learn track found [here](https://docs.microsoft.com/en-us/learn/certifications/data-analyst-associate/). It is the go-to source for all material covered by the exam. Use the below Checkboxes to track progress and the links in the Outline to return to sections in the future. 

To check off the sub-sections and headers, add an `x` between the brackets like so `[x]`. Example:
- [ ] Incomplete
- [x] Complete

We then recommend working with the supplemental material to solidify content. 

**NOTICE: Following the Microsoft Learn path is not enough. There is too much material to memorize in one go-through and content will not sink in with further practice and review. You *will* have to practice, and you will be revisiting content.**

# Additional Notes & Caveats
Unfortunately, Microsoft's Learn path and its outline are not a 1:1. This can manifest in several ways.

First, a sub-section in the outline may not have its own explicit page in the MS Learn path and may exist across several pages of content. E.g. `identify and connect to a data source` does not exist as a specific page in the MS Learn section for `Prepare the Data`, but rather as several pages tied to various data sources.  

Second, content for certain sub-sections in the outline may not be found within the indicated MS Learn section. We have tried to note this where possible.

Lastly, a section titled `Develop a data model` exists in the Outline, but has no corollary in the MS Learn track. In this case, informative content has been provided to the best of our ability. Several gaps surely remain, however, so please feel free to contribute.

# About the DA-100 / PL-300
- Duration: 180 Minutes.
- Question Types: Multiple choice and multi-response questions.
- # of Questions: s 40-60 questions.
- Score to Pass: 700/1000


# The Skills Measured Checklist
### [Prepare the Data (15-20%)](#prepare-the-data)
- [ ] **Get data from different data sources**
  - [ ] identify and connect to a data source
  - [ ] change data source settings
  - [ ] select a shared dataset or create a local dataset
  - [ ] select a storage mode
  - [ ] use Microsoft Dataverse
  - [ ] change the value in a parameter
  - [ ] connect to a data flow
- [ ] **Clean, transform, and load the data**
  - [ ] profile the data
  - [ ] resolve inconsistencies, unexpected or null values, and data quality issues
  - [ ] identify and create appropriate keys for joins
  - [ ] evaluate and transform column data types
  - [ ] shape and transform tables
  - [ ] combine queries
  - [ ] apply user-friendly naming conventions to columns and queries
  - [ ] configure data loading
  - [ ] resolve data import errors
### [Model the Data (30—35%)](#model-the-data)
- [ ] **Design a data model**
  - [ ] define the tables
  - [ ] configure table and column properties
  - [ ] design and implement role-playing dimensions
  - [ ] define a relationship's cardinality and cross-filter direction
  - [ ] design a data model that uses a star schema
  - [ ] create a common date table
- [ ] **Develop a data model**
  - [ ] create calculated tables
  - [ ] create hierarchies
  - [ ] create calculated columns
  - [ ] implement row-level security roles
  - [ ] use the Q&A feature
- [ ] **Create model calculations by using DAX**
  - [ ] create basic measures by using DAX
  - [ ] use CALCULATE to manipulate filters
  - [ ] implement Time Intelligence using DAX
  - [ ] replace implicit measures with explicit measures
  - [ ] use basic statistical functions
  - [ ] create semi-additive measures
  - [ ] use quick measures
- [ ] **Optimize model performance**
  - [ ] remove unnecessary rows and columns
  - [ ] identify poorly performing measures, relationships, and visuals
  - [ ] reduce cardinality levels to improve performance
### [Visualize and Analyze the Data (25—30%)](#visualize-and-analyze-the-data)
- [ ] **Create reports**
  - [ ] add visualization items to reports
  - [ ] choose an appropriate visualization type
  - [ ] format and configure visualizations
  - [ ] use a custom visual
  - [ ] apply and customize a theme
  - [ ] configure conditional formatting
  - [ ] apply slicing and filtering
  - [ ] configure the report page
  - [ ] use the Analyze in Excel feature
  - [ ] choose when to use a paginated report
- [ ] **Create dashboards**
  - [ ] manage tiles on a dashboard
  - [ ] configure mobile view
  - [ ] use the Q&A feature
  - [ ] add a Quick Insights result to a dashboard
  - [ ] apply a dashboard theme
  - [ ] pin a live report page to a dashboard
- [ ] **Enhance reports for usability and storytelling**
  - [ ] configure bookmarks
  - [ ] create custom tooltips
  - [ ] edit and configure interactions between visuals
  - [ ] configure navigation for a report
  - [ ] apply sorting
  - [ ] configure Sync Slicers
  - [ ] group and layer visuals by using the selection pane
  - [ ] drilldown into data using interactive visuals
  - [ ] export report data
  - [ ] design reports for mobile devices
- [ ] **Identify patterns and trends**
  - [ ] use the Analyze feature in Power BI
  - [ ] identify outliers
  - [ ] choose between continuous and categorical axes
  - [ ] use groupings, binnings, and clustering
  - [ ] use AI visuals
  - [ ] use the Forecast feature
  - [ ] create reference lines by using the Analytics pane
### [Deploy and Maintain Assets (20—25%)](#deploy-and-maintain-assets)
- [ ] **Manage files and datasets**
  - [ ] identify when a gateway is required
  - [ ] configure a dataset scheduled refresh
  - [ ] configure row-level security group membership
  - [ ] provide access to datasets
  - [ ] manage global options for files
- [ ] **Manage workspaces**
  - [ ] create and configure a workspace
  - [ ] assign workspace roles
  - [ ] configure and update a workspace app
  - [ ] publish, import, or update assets in a workspace
  - [ ] apply sensitivity labels to workspace content
  - [ ] configure subscriptions and data alerts
  - [ ] promote or certify Power BI content

# The Skills Measured Outline
### [Prepare the Data](https://docs.microsoft.com/en-us/learn/paths/prepare-data-power-bi/)
#### [Get data from different data sources](https://docs.microsoft.com/en-us/learn/modules/get-data/)
- [identify and connect to a data source](https://docs.microsoft.com/en-us/power-bi/connect-data/desktop-connect-to-data)
- [change data source settings](https://www.c-sharpcorner.com/article/how-to-change-data-source-of-existing-report-in-power-bi/)
- select a shared dataset or create a local dataset (See first bullet. Documentation contains various sections on connecting to different sets of data.)
- [select a storage mode](https://docs.microsoft.com/en-us/power-bi/transform-model/desktop-storage-mode)
- [use Microsoft Dataverse](https://docs.microsoft.com/en-us/learn/modules/dataverse-teams-power-bi/)
- [change the value in a parameter](https://docs.microsoft.com/en-us/power-query/power-query-query-parameters)
- [connect to a data flow](https://docs.microsoft.com/en-us/power-bi/transform-model/dataflows/dataflows-develop-solutions)

##### Additional Resources:
- [Lab: Prepare data in Power BI Desktop](https://docs.microsoft.com/en-us/learn/modules/get-data/lab-prepare)  
- [MS Documentation: Data sources in Power BI](https://docs.microsoft.com/en-us/power-bi/connect-data/desktop-data-sources)  
- [How To Change Data Source Of Existing Report In Power BI](https://www.c-sharpcorner.com/article/how-to-change-data-source-of-existing-report-in-power-bi/)

#### [Clean, transform, and load the data](https://docs.microsoft.com/en-us/learn/modules/clean-data-power-bi/)
- profile the data
- resolve inconsistencies, unexpected or null values, and data quality issues
- identify and create appropriate keys for joins
- evaluate and transform column data types
- shape and transform tables
- combine queries
- apply user-friendly naming conventions to columns and queries
- configure data loading
- resolve data import errors

##### Additional Resources:
- [Lab: Load data in Power BI Desktop](https://docs.microsoft.com/en-us/learn/modules/clean-data-power-bi/8-lab/?ns-enrollment-type=LearningPath&ns-enrollment-id=learn-bizapps.data-preparation-in-power-bi)

### [Model the Data](https://docs.microsoft.com/en-us/learn/paths/model-power-bi/)
#### [Design a data model](https://docs.microsoft.com/en-us/learn/modules/design-model-power-bi/)
- define the tables
- configure table and column properties
- design and implement role-playing dimensions
- define a relationship's cardinality and cross-filter direction
- design a data model that uses a star schema
- create a common date table

##### Additional Resources:
- [Lab: Model data in Power BI Desktop, pt.1](https://docs.microsoft.com/en-us/learn/modules/design-model-power-bi/8-lab/?ns-enrollment-type=LearningPath&ns-enrollment-id=learn-bizapps.model-power-bi)  
- [Lab: Model data in Power BI Desktop, pt.2](https://docs.microsoft.com/en-us/learn/modules/design-model-power-bi/9-lab/?ns-enrollment-type=LearningPath&ns-enrollment-id=learn-bizapps.model-power-bi)

#### Develop a data model 
Unfortunately this section does not appear in the MS Learn track, though its items are addressed elsewhere. Links have nevertheless been provided below to cover the topics.
- [create calculated tables](https://docs.microsoft.com/en-us/power-bi/transform-model/desktop-calculated-tables)
- [create hierarchies](https://spreadsheeto.com/power-bi-hierarchy/)
- [create calculated columns](https://docs.microsoft.com/en-us/power-bi/transform-model/desktop-tutorial-create-calculated-columns)
- [implement row-level security roles](https://docs.microsoft.com/en-us/learn/modules/row-level-security-power-bi/)
- [use the Q&A feature](https://docs.microsoft.com/en-us/power-bi/create-reports/power-bi-tutorial-q-and-a)

##### Additional resources:
- [Row-level security (RLS) with Power BI](https://docs.microsoft.com/en-us/power-bi/admin/service-admin-rls)
- [Use the Q&A visual](https://docs.microsoft.com/en-us/learn/modules/ai-visuals-power-bi/2-visual?ns-enrollment-type=LearningPath&ns-enrollment-id=learn-bizapps.data-analysis-power-bi)

#### [Create model calculations by using DAX](https://docs.microsoft.com/en-us/learn/modules/create-measures-dax-power-bi/)
- create basic measures by using DAX
- use CALCULATE to manipulate filters
- implement Time Intelligence using DAX
- replace implicit measures with explicit measures
- use basic statistical functions
- create semi-additive measures
- use quick measures

##### Additional Resources:
- [Lab: Introduction to DAX in Power BI Desktop](https://docs.microsoft.com/en-us/learn/modules/create-measures-dax-power-bi/6-lab/?ns-enrollment-type=LearningPath&ns-enrollment-id=learn-bizapps.model-power-bi)
- [Lab: Time Intelligence and Measures in DAX](https://docs.microsoft.com/en-us/learn/modules/create-measures-dax-power-bi/8-lab/?ns-enrollment-type=LearningPath&ns-enrollment-id=learn-bizapps.model-power-bi)

#### [Optimize model performance](https://docs.microsoft.com/en-us/learn/modules/optimize-model-power-bi/)
- remove unnecessary rows and columns
- identify poorly performing measures, relationships, and visuals
- reduce cardinality levels to improve performance

### [Visualize and Analyze the Data](https://docs.microsoft.com/en-us/learn/paths/visualize-data-power-bi/)
#### [Create reports](https://docs.microsoft.com/en-us/learn/modules/visuals-power-bi/)
- add visualization items to reports
- choose an appropriate visualization type
- format and configure visualizations
- use a custom visual
- apply and customize a theme
- configure conditional formatting
- apply slicing and filtering
- configure the report page
- [use the Analyze in Excel]feature(https://docs.microsoft.com/en-us/power-bi/collaborate-share/service-analyze-in-excel)  
- [choose when to use a paginated report](https://docs.microsoft.com/en-us/learn/modules/create-paginated-reports-power-bi/)

##### Additional Resources:
- [Lab: Design a report in Power BI Desktop](https://docs.microsoft.com/en-us/learn/modules/visuals-power-bi/8-lab/?ns-enrollment-type=LearningPath&ns-enrollment-id=learn-bizapps.visual-data-power-bi)
- [Lab: Create a paginated report](https://docs.microsoft.com/en-us/learn/modules/create-paginated-reports-power-bi/6-lab)

#### [Create dashboards](https://docs.microsoft.com/en-us/learn/modules/create-dashboards-power-bi/)
- manage tiles on a dashboard
- configure mobile view
- use the Q&A feature
- add a Quick Insights result to a dashboard
- apply a dashboard theme
- pin a live report page to a dashboard

##### Additional Resources:
- [Lab: Create a Power BI dashboard](https://docs.microsoft.com/en-us/learn/modules/create-dashboards-power-bi/9-lab/?ns-enrollment-type=LearningPath&ns-enrollment-id=learn-bizapps.visual-data-power-bi)
- [Use the Q&A visual](https://docs.microsoft.com/en-us/learn/modules/ai-visuals-power-bi/2-visual?ns-enrollment-type=LearningPath&ns-enrollment-id=learn-bizapps.data-analysis-power-bi)

#### [Enhance reports for usability and storytelling](https://docs.microsoft.com/en-us/learn/modules/data-driven-story-power-bi/)
- configure bookmarks
- create custom tooltips
- edit and configure interactions between visuals
- configure navigation for a report
- apply sorting
- configure Sync Slicers
- group and layer visuals by using the selection pane
- drilldown into data using interactive visuals
- export report data
- design reports for mobile devices

##### Additional Resources:
- [Lab: Enhance Power BI reports with slicers, interaction, and formatting](https://docs.microsoft.com/en-us/learn/modules/data-driven-story-power-bi/13-lab/?ns-enrollment-type=LearningPath&ns-enrollment-id=learn-bizapps.visual-data-power-bi)

#### [Identify patterns and trends](https://docs.microsoft.com/en-us/learn/modules/perform-analytics-power-bi/)
- use the Analyze feature in Power BI
- identify outliers
- choose between continuous and categorical axes
- use groupings, binnings, and clustering
- [use AI visuals (this is its own section in the MS Learn track)](https://docs.microsoft.com/en-us/learn/modules/ai-visuals-power-bi/)
- use the Forecast feature
- create reference lines by using the Analytics pane

##### Additional Resources:
- [Lab: Perform data analysis in Power BI Desktop](https://docs.microsoft.com/en-us/learn/modules/ai-visuals-power-bi/5-lab?ns-enrollment-type=LearningPath&ns-enrollment-id=learn-bizapps.data-analysis-power-bi)

### [Deploy and Maintain Assets](https://docs.microsoft.com/en-us/learn/paths/manage-workspaces-datasets-power-bi/)
#### [Manage files and datasets](https://docs.microsoft.com/en-us/learn/modules/manage-datasets-power-bi/)
- identify when a gateway is required
- configure a dataset scheduled refresh
- configure row-level security group membership
- provide access to datasets
- manage global options for files
#### [Manage workspaces](https://docs.microsoft.com/en-us/learn/modules/create-manage-workspaces-power-bi/)
- create and configure a workspace
- assign workspace roles
- configure and update a workspace app
- publish, import, or update assets in a workspace
- apply sensitivity labels to workspace content
- configure subscriptions and data alerts
- promote or certify Power BI content

# Additional Resources & Links
- [BI Elite Training DA-100 Exam Prep – Power BI Certification](https://training.bielite.com/courses/da-100-exam-prep-power-bi-certification/)  
  - Price: $29USD
  - Offering: Live Azure database, 30+ DA-100 Practice Exam Questions, Many hours of premium video tutorials from a Microsoft MVP
  – Free Trial? Yes. 7 day.
- [Learn Data Insights](https://learndatainsights.com/data-analyst/analysing-data-with-microsoft-power-bi-da-100%e2%80%8b/)  
  - Price: Free
  - Offering: Questions w/ explanations & links to resources when answers are incorrect.
- [Magna Data Solutions](https://magnadatasolutions.com/practice-da100-exam/)
  - Price: Free
  - Offering: Exam tips video & questions
- [Sky Point CSG](https://www.csgpro.com/diad-instructional-videos/?submissionGuid=9a532666-5e9f-4b88-bc58-eac52f89db4e)
  - Price: Free
  - Offering: Video walkthrough of Microsoft's Dashboard in a Day project
- [Microsoft's Dashboard in a Day Project](https://powerbi.microsoft.com/en-us/diad/)
  - Price: Free
  - Offering: Materials for constructing dashboards like a professional, including tutorials and sample data
- [Official Practice Test (Current test exam is for the DA-100)](https://www.mindhub.com/da-100-analyzing-data-with-microsoft-power-bi-microsoft-official-practice-test/p/MU-DA-100?utm_source=microsoft&utm_medium=certpage&utm_campaign=AZLearnerJourney)
  - Price: $99-109 (for 30 & 60 day availability, respectively)
  - Offering: Practice test meant to mimic the exam format.
- [Udemy Practice Tests](https://www.udemy.com/course/pl-300-practice-tests-microsoft-power-bi-data-analyst/?couponCode=66B6F0AF85D1A0E729C6)
  - Price: ~$20 (price may vary over time)
