# [Data Profiling](https://docs.microsoft.com/en-us/power-query/data-profiling-tools)
`Notice: This is a personal study file. It assumes a certain familiarity with the topic and therefore DOES NOT contain everything about this topic. The author created this to track more technical gotchas that might appear in the PL-300 exam.`

Available in the Power Query Editor.

### Three Types
#### [Column quality](https://docs.microsoft.com/en-us/power-query/data-profiling-tools#column-quality)
The column *quality* (key word) feature labels values in rows in five categories:
- Valid, shown in green.
- Error, shown in red.
- Empty, shown in dark grey.
- Unknown, shown in dashed green. Indicates when there are errors in a column, the quality of the remaining data is unknown.
- Unexpected error, shown in dashed red.

This appears at the top. Data loses utility the more errors and blanks there are, making this a top priority.

<p align="center"><img width=800 src="https://user-images.githubusercontent.com/29554021/154745667-73abe0a6-4035-4938-a0e2-2539a7e19013.png" /></p>


#### [Column distribution](https://docs.microsoft.com/en-us/power-query/data-profiling-tools#column-distribution)
This feature provides a set of visuals underneath the names of the columns that `showcase the frequency and distribution of the values` in each of the columns. The data in these visualizations is sorted in descending order from the value with the highest frequency.

Think *how are values distributed*...

<p align="center"><img width=800 src="https://user-images.githubusercontent.com/29554021/154745808-58e25dd1-6f5c-4f7d-98c2-252c8fa236f5.png" /></p>

#### [Column profile](https://docs.microsoft.com/en-us/power-query/data-profiling-tools#column-profile)
This feature provides a more in-depth look at the data in a column. Apart from the column distribution chart, it contains a column statistics chart. This information is displayed underneath the data preview section, as shown in the following image.

Think *what is the overall `profile`*

<p align="center"><img width=800 src="https://user-images.githubusercontent.com/29554021/154745898-4c0e79ab-8f18-47bc-ae5c-5b2f3fee512c.png" /></p>
