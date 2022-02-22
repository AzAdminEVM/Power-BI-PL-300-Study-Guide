# Workspaces
[Primary Link](https://docs.microsoft.com/en-us/power-bi/consumer/end-user-workspaces)

`Notice: This is a personal study file. It assumes a certain familiarity with the topic and therefore DOES NOT contain everything about this topic. The author created this to track more technical gotchas that might appear in the PL-300 exam.`

## [Roles](https://docs.microsoft.com/en-us/power-bi/consumer/end-user-workspaces#permissions-in-the-workspaces)
([Primary Doc](https://docs.microsoft.com/en-us/power-bi/collaborate-share/service-roles-new-workspaces))

When granting access to a new workspace, designers add individuals or groups to one of the workspace roles. Everyone in a user group gets the assigned role. 
If someone's in several groups, they get the highest access. 

**Note 1: All of these capabilities, except viewing and interacting, require a Power BI Pro or Premium Per User (PPU) license.**  
**Note 2: If the workspace is backed by a Premium capacity, a non-Pro user can view content within the workspace under the Viewer role.**

- Admin
  - Add/remove other users
  - Publish, update, and/or share an app in a workspace
  - Create, edit, delete, and publish reports and content in a workspace
  - View and interact with reports and dashboards in a workspace
  - Configure data refreshes
  - [How to administer](https://docs.microsoft.com/en-us/power-bi/admin/service-admin-portal?WT.mc_id=DP-MVP-5003635) [REVIEW]
  - Admins can also: enable use of ArcGIS Maps and custom visuals, allow use of only certified custom visuals, allow for interaction and sharing of R/Python visuals 
- Member
  - Can complete all tasks that are associated with admins but can't add or remove users
  - Cannot delete the workspace
  - Cannot update the metadata about the workspace
- Contributor
  - Cannot add or remove users
  - Cannot publish, update, or edit an app in a workspace unless given this ability by admins/members
  - Can create, update, and publish content and reports within a workspace
  - Can schedule data refreshes
- Viewer
  - Cannot add or remove users
  - Can only view a report or dashboard in a workspace
  - Can read data that is stored in workspace dataflows


## [Licensing](https://docs.microsoft.com/en-us/power-bi/consumer/end-user-license)
Each user of the Power BI service has either a `free license`, a `Pro license`, or a `Premium per-user license`. 

Premium is an organizational *subscription* that provides a different way to store content--in a virtual container called a capacity. `With Premium capacity, anyone with permissions, whether they're inside or outside your organization, can view content stored in this Premium capacity, without purchasing individual Power BI Pro or Premium per-user licenses.` Users without a Pro license can still access a workspace that's in Power BI Premium capacity, as long as they're assigned a role in that workspace.

Apps are similar. When a designer creates and publishes an app, they grant access to entire organizations or individuals. The extent to which you can interact with the app's content depends on the specific access permissions given to you. For example, you may be given access to view the app, connect to the underlying datasets, make copies of reports, or share the content.

In short, premium capacity enables widespread distribution of content by Pro users without requiring Pro licenses for the recipients who view the content.

If you want to create and share content (dashboards, reports, apps), or open content that someone else shared with you, then you need to have a Pro user license or a Premium per user license. 

#### Putting it together
There are many different ways organizations organize their Power BI subscriptions and licenses. From a business users perspective, one of the most common scenarios is when an organization buys a Premium subscription, the admin assigns Pro licenses to a small group of users, and all the other users work with free licenses. Typically, the admin assigns the Pro licenses to the employees who will be creating and sharing content. The Pro users create workspaces and add content (dashboards, reports, datasets, apps) to those workspaces. To allow free users to collaborate in those workspaces, the admin or Pro user then assigns the workspaces to a Premium capacity.

![image](https://docs.microsoft.com/en-us/power-bi/consumer/media/end-user-license/power-bi-dedicated.jpg)
