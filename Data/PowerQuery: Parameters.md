# [Using Parameters](https://docs.microsoft.com/en-us/power-query/power-query-query-parameters)
A way to easily store and manage a value that can be reused, parameters offer the flexibility to dynamically change the output of queries depending on their value.
They can be used for:
- Changing the argument values for particular transforms and data source functions
- Inputs in custom functions

<p align="center"><img src="https://user-images.githubusercontent.com/29554021/154758892-928ddb4f-4511-439a-b788-2ab9b33e610b.png" width=600/></p>

Two ways:
1. From an existing query: right-click a query whose value is a simple non-structured constant such as, but not limited to, a date, text, or number, and select Convert to Parameter.
2. Using the Manage Parameters window: select the New Parameter option from the dropdown menu of Manage Parameters in the Home tab (see above image)

### Param Properties
- Name
- Description—Displayed next to the parameter name when parameter information is displayed
- Required
- Type—We recommended that you always set up the data type of your parameter. 
- Suggested Values—Provides the user with suggestions to select a value for the Current Value from the available options:
  - Any value—The current value can be any manually entered value.
  - List of values—Provides a simple table-like experience 
- Query—Uses a list query (a query whose output is a list) to provide the list of suggested values that you can later select for the Current Value.
- Current Value—The value that will be stored in this parameter.

[Examples](https://docs.microsoft.com/en-us/power-query/power-query-query-parameters#where-to-use-parameters)

[Relevant Lab](https://docs.microsoft.com/en-us/learn/modules/create-paginated-reports-power-bi/6-lab?ns-enrollment-type=LearningPath&ns-enrollment-id=learn-bizapps.visual-data-power-bi)
