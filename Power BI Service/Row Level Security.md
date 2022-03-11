# [Row Level Security](https://docs.microsoft.com/en-us/power-bi/enterprise/service-admin-rls)
Row-level security (RLS) with Power BI can be used to restrict data access for given users. Filters restrict data access at the row level, and you can define 
filters within roles. In the Power BI service, members of a workspace have access to datasets in the workspace. RLS doesn't restrict this data access.

So, say you publish and share a report with a dataset for sales of bikes, accessoriees, and clothing, but you only want the colleague in the bike department 
to see data related to bikes. This is the use case for row-level security.

The process is to set it up first in PBI Desktop and then to assign people to the roles you have setup.

<p align="center"><img width="609" alt="image" src="https://user-images.githubusercontent.com/29554021/157730586-5a8568b1-3d93-49b2-a1e0-6b717903f650.png"></p>

Leads to:
<p align="center"><img width="759" alt="image" src="https://user-images.githubusercontent.com/29554021/157730684-4f25d1fe-83bd-492d-9da0-d69dbecfb49f.png"></p>

Leads to:
<p align="center"><img width="319" alt="image" src="https://user-images.githubusercontent.com/29554021/157730747-b7013d53-3a46-46fc-b6c1-0ff82c44339e.png"></p>

You can then "View As Role" to see the effect:
<p align="center"><img width="347" alt="image" src="https://user-images.githubusercontent.com/29554021/157730929-49efcd4c-1dab-4a6e-9b8c-43db0200e282.png"></p>

Then in PBI Service, you need to add people to the rules:
<p align="center"><img width="292" alt="image" src="https://user-images.githubusercontent.com/29554021/157731171-46f53b94-4b84-40b9-a9c8-2d533bf6b1ca.png"></p>

And...
<p align="center"><img width="766" alt="image" src="https://user-images.githubusercontent.com/29554021/157731221-0b34fcea-4df4-46ca-acc2-27092669e50b.png"></p>

## Dynamic RLS
`username()` and `userprincipalname()`. These functions allow dynamic RLS. Here's the difference.

##### PBI Desktop
- username: returns a DOMAIN/user
- userprincipalname: returns an email address (e.g. elias@goaztech.onmicrosoft.com)

##### PBI Service
- username: returns an email address (e.g. elias@goaztech.onmicrosoft.com)
- userprincipalname: returns an email address (e.g. elias@goaztech.onmicrosoft.com)

In conjunction with View As > Other User, apply these via a dynamic role:
<p align="center"><img width="705" alt="image" src="https://user-images.githubusercontent.com/29554021/157733343-f7455488-ebf5-478c-b485-eb252d10fed6.png"></p>

