# [Apps in Power BI](https://docs.microsoft.com/en-us/power-bi/consumer/end-user-apps)

`Notice: This is a personal study file. It assumes a certain familiarity with the topic and therefore DOES NOT contain everything about this topic. The author created this to track more technical gotchas that might appear in the PL-300 exam.`

## [A Primer](https://docs.microsoft.com/en-us/power-bi/consumer/end-user-apps)
Power BI designers can create official packaged content, then distribute it to a broad audience as an app. Apps are created in workspaces, 
where members can collaborate on Power BI content with their colleagues before publishing the finished app to individuals, large groups of people in an 
organization, or an entire organization. 

`By using an app, it's easier for designers to manage permissions on these collections since the app can have permissions that are different than those 
set on the workspace.`

#### Advantages of Apps
Apps are an easy way for designers to share different types of content at one time. App designers create the dashboards and reports and bundle them together into an app that users can interact with but not modify. The designers then share or publish the app to a location where the business user can access it. Because related dashboards and reports are bundled together, it's easier for the business user to find and install in both the Power BI service (https://powerbi.com) and on their mobile device. 

After installing an app, the business user doesn't have to remember the names of a lot of different dashboards or reports because they're all together in one app, in browser or on a mobile device.

You can make your own or install Apps in the App Marketplace. All you have to do is install them and then find them in the 'Apps' portion of powerbi.com.

## [Publishing an App](https://docs.microsoft.com/en-us/power-bi/collaborate-share/service-create-distribute-apps)
This is one of the fastest ways to release content to an entire organization. Collaborate inside a workspace, developing content, and then, when it's ready for distribution, create an app. Do this by navigating to the workspace and selecting create app. Then navigate to 'Permissions' where you select ‘Publish to entire organization’.

One of the benfits is that apps make it easier to manage permissions on the collections of dashboards and reports they contain. Users can interact with it either in the Power BI service, or one of the mobile apps -– filtering, highlighting, and sorting the data. They get updates automatically and `you can control how frequently the data refreshes`. 

`Build Permissions:` App creators can also give users [Build permission](https://docs.microsoft.com/en-us/power-bi/connect-data/service-datasets-build-permissions) to connect to the underlying datasets, and to create copies of the reports in the app.

You give Build permission for a dataset in a few different ways ([source](https://docs.microsoft.com/en-us/power-bi/connect-data/service-datasets-build-permissions)):
- Members of a workspace with at least a Contributor role automatically have Build permission for datasets in that workspace, and permission to copy a report.
- Dataset owners can assign Build permission to specific users or security groups on the Manage permissions page.
- Say you have Reshare and Build permission on a dataset. When you share a report or dashboard built on that dataset, you can specify that the recipients also get Build permission for the underlying dataset. See Share Power BI reports and dashboards for detail.
- An admin or member of the workspace where the dataset resides can decide during app publishing that users with permission for the app also get Build permission for the underlying datasets. This is the `Allow users to connect to datasets` setting. This allows other users to:
  1. Use the app datasets as the basis for their reports.
  2. Search for these datasets in Power BI Desktop and in the get-data experience in the Power BI service.
  3. Create reports and dashboards based on these datasets.

<p align="center"><img width="400" alt="image" src="https://user-images.githubusercontent.com/29554021/154581950-6f6f8ffa-2eff-4af8-8210-4e6d2c46bbc0.png"></p>

To create or update an app, you need a Power BI Pro or Premium Per User (PPU) license. For app consumers, there are two options.
- Option 1. The workspace for this app is not in a Power BI Premium capacity: All business users need Power BI Pro or Premium Per User (PPU) licenses to view your app.
- Option 2 The workspace for this app is in a Power BI Premium capacity: Business users without Power BI Pro or Premium Per User (PPU) licenses in your organization can view app content. However, they can't copy the reports, or create reports based on the underlying datasets. Read What is Power BI Premium? for details.


### A question to better understand Apps vs Workspaces
<p align="center"><img width="400" alt="image" src="https://user-images.githubusercontent.com/29554021/154580841-713422c6-6e57-487b-b0fb-e8ef39746dfe.jpg"></p>


