# [Common Date Tables](https://docs.microsoft.com/en-us/power-bi/guidance/model-date-tables)
Use these when years don't necessarily start and end on standard calendar days. This means disabling Date hierarchies first.

<p align="center"><img width="509" alt="image" src="https://user-images.githubusercontent.com/29554021/156818192-e47dff77-a534-4ebe-8fd0-52139e6116aa.png"></p>

Then, create your date table. Use `CALENDAR()`:
```
DateTable = CALENDAR(DATE(2000,1,1),DATE(2030,12,31))
```

Then, mark it as your date table. Table Tools > Mark as date table (right-click works too):

<p align="center"><img width="948" alt="image" src="https://user-images.githubusercontent.com/29554021/156818422-1bd21739-ed47-42b8-8a31-a8b0baf7800b.png"></p>

From there you'll need to add year, month, day columns as needed, with adjustments for what is considered the first business day of the year. 
This example shows April as the first:

<p align="center"><img width="494" alt="image" src="https://user-images.githubusercontent.com/29554021/156818840-648e3cc8-ba69-4d97-8ed6-0bf858117d90.png"></p>
