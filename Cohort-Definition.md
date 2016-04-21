When performing an analysis, usually the first step is to define the population of interest (also known as a cohort). This functionality was originally built as part of the [Circe working group](http://www.ohdsi.org/web/wiki/doku.php?id=documentation:software:circe) and now Circe has been fully incorporated into Atlas. 

## Browsing cohorts

Select the "cohorts" menu option to browse existing cohorts. Click on an existing cohort to dive into the cohort definition and other functions that will be described in the subsequent sections. Alternatively, you can select the "New Cohort" button in the top-right of the screen to create a new one.

You can use the table to browse through existing cohort definitions. The filter functionality above the table can be used to filter the list based on a search string. Furthermore, the columns in the table can be used to sort the information in the table to find the cohort(s) of interest.

## Cohort Definition

Coming soon!

## Concept Sets

The concept sets tab will list the concept sets that are defined within the cohort. To review the definition of the concept set you can select it from the table and the definition will show up below it. The concept set definition will be shown and takes the same form as described in the Concept Set section. Furthermore, the cohort concept set that has been opened will now appear in the left hand menu as the current concept set. 

## Generation

When you feel that your cohort definition is complete, you can use the Generate tab to generate a list of people in your cohort. This tab will show a table of CDM data sources that are available with the following properties:

- Generate button: clicking this button will execute SQL code against your CDM to select people that will define your cohort.
- Source Name: the source name of your CDM
- Generation Status: This will show the status of the cohort generation activity
- Distinct People: If the cohort has been generated, this will show the distinct number of people in the cohort
- Generated: The date and time the cohort was generated
- Generation Duration: How long it took to generate the cohort

Once this cohort is generated, you can use the reporting section to obtain further descriptive analytics around this cohort.

## Reporting

The reporting tab provides cohort summarization and visualization tools. This functionality was originally built as part of the [Heracles working group](http://www.ohdsi.org/web/wiki/doku.php?id=documentation:software:heracles) and now Heracles has been fully incorporated into Atlas.

From the reporting tab, you will see a column with the reports that are defined in the Heracles Analysis List section of this [article](http://www.ohdsi.org/web/wiki/doku.php?id=documentation:software:heracles).  Then you will see a column for each CDM source that has been defined. From here you can select each report by placing a check mark in the column and select the Generate button to generate the reports. This will start an analysis job that you can monitor by selecting the "Jobs" menu item.

Once the analysis is complete, each report will have a "view" button that you can use to view the results. 

### Drilldown reports

Some reports contain a top level set of statistics with the ability to drill into the details. More specifically, these reports are: Condition, Condition Eras, Drug Eras, Drug Exposure, Drugs by Index, Procedure and Procedures by Index. 

These reports contain an initial visualization with two tabs: treemap and table. The treemap provides a visualization of the data that appears on the table tab. The table tab provides a tabular view of each report. Clicking on a row in the tabular format OR on a cell in the treemap will reveal further details for the selected concept.

## Print Friendly

This tab provides a human-readable description of the cohort definition. This is useful when describing the logic used to define the cohort along with the concept sets/source codes that make up the definition. 

## JSON

The JSON tab provides JavaScript Object Notation (JSON) representation of the cohort definition and supporting concept sets. This enables you to copy & paste the full cohort definition to provide as part of your study write up or to another member of the OHDSI network to generate the same cohort in their environment.

If you have a cohort definition in JSON format, you can copy & paste it into the text box in this area and click the "Reload" button found at the bottom right of the page. This will then load the full cohort definition and concept sets into the editor.

## Saving

Provide a name for your cohort and use the "save" button to save the cohort to the database.

## Show SQL

The "Show SQL" button will provide a dialog that will show you the SQL statement that is executed based on the cohort definition. This window will allow you to copy/paste SQL from Atlas into a SQL editor for further refinement. This window will also provide the SQL for the different SQL dialects currently supported.

## Close

This will close the current cohort definition. If there are unsaved changes, you will be prompted to save them or abandon your changes.

## Copy

This will create a copy of the current cohort definition.

## Delete Cohort

This will delete the current cohort.