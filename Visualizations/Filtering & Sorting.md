# Filtering
`Notice: This is a personal study file. It assumes a certain familiarity with the topic and therefore DOES NOT contain everything about this topic. The author created this to track high-level notes and technical gotchas that might appear in the PL-300 exam.`

#### Miscellaneous
- Wildcard filtering. 
  - Use '\*' to filter for any character across any number of spaces. E.g. W\*e would return a word like Whatever.
  - Use '?' to filter for any single character. E.g. W?e would return a word like Wednesday.
  - These can be combined.
- TopN
  - Apply this to a visual so that it shows only the top (or bottom) x number of results.
  - This will adjust as filters are applied from other visuals.

<img width="814" alt="image" src="https://user-images.githubusercontent.com/29554021/155385432-f82bf0bf-c48d-47f0-b115-e08cc336d0a4.png">

<img width="1000" alt="image" src="https://user-images.githubusercontent.com/29554021/155385912-ff9c13d2-eda3-45cc-8996-ee1fe4c762ad.png">

# Sorting
- Don't forget `Sort by Column` (Modeling page)
- Tables can be sorted by clicking on column headers or the three dots > sort ascending/descending/sort by; Matrices must be sorted using the three dots, otherwise PBI simply spotlights when a column is clicked.
- To sort the x axis of a chart that has continuous values like years you will first need to go to the formatting section in the Visualizations pane > X Axis > Type = Categorical.
  - Continuous cannot be sorted.

# Bookmarks
<img width="164" alt="image" src="https://user-images.githubusercontent.com/29554021/155390990-4743545e-3fc6-4cae-88dd-8d6e1f96c8da.png">
  
Bookmarks can be used to filter several things:
- Data: Filters, Slicers, & Sort States
- Display: Spotlighting & Visibility of objects
- Current Page: Which page is visible
- All Visuals or Selected?  
  
Use the selection page to show/hide certain things:
<img width="866" alt="image" src="https://user-images.githubusercontent.com/29554021/155391625-88ebab74-f0a6-4fc2-b229-79ac71185687.png">

Don't forget to update the bookmark!
<img width="879" alt="image" src="https://user-images.githubusercontent.com/29554021/155391592-f6112171-c002-4080-86e5-98e8afdfe1ec.png">

Recall that bookmarks can be triggered by buttons & images using the `Action` feature:
<img width="422" alt="image" src="https://user-images.githubusercontent.com/29554021/155396021-a4e6c1d9-a91f-4c8f-b92f-03fa32926447.png">

Other actions include:
- Web URL
- Back
- Bookmark
- Q&A
- Page Navigation
- Drill through (Buttons only)

# Selection Pane
<img width="214" alt="image" src="https://user-images.githubusercontent.com/29554021/155392218-22b1cea9-3d58-46d5-9bd7-40d55bddb501.png">

Several things:
- Change the tab order
- Change the layer order
- Group visuals to select several at once. Allows you to adjust shared formatting


