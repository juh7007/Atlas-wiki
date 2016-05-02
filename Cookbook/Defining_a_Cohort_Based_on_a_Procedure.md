## Defining a Cohort Based on a Procedure

### Problem

You would like to define cohort of patients who have all undergone a prostatectomy and generate results showing the number of patients in the cohort.

### Solution

1. Click New Cohort Definition (upper right, blue button)

1. Fill in new Cohort Definition name (red input field). Type ‘prostatectomy’.

1. Fill in description (input field labeled description, underneath name). Type ‘prostatectomy study’

1. In the Expression tab, in the drop down menu 'Add primary event filters...', choose 'Add Procedure Filters'

1. Click plus sign (+) next to dropdown to create a new concept set

1. In Concept Sets tab, Type 'prostatectomy concept set' in input field right of name: (it should currently contain 'Unnamed Concept Set')

1. Click Add (blue button bottom left). A dialog box should appear entitled "Select Concept...".

1. Choose Procedure from drop down menu to the right of the search box.

1. In the search box, type 'prostatectomy' and then press Enter.

1. In the table, click on the column label 'DRC' (this stands for Descendant Record Count) twice or until largest number appears as top record.

1. Click on check boxes in leftmost column of first [nine] records.

1. Click on the 'Add And Close' button in the bottom right of the dialog box.

1. Click the 'Save' button to save the cohort definition

1. Click the drop down menu 'Please select code set to modify' to check that the new concept set has been added.  You should see the new concept set listed.

1. Click on the 'Generation Status' tab

1. Click the 'Generate' button in the Action column (it will not respond after clicking, please click only once)

1. Click on 'Jobs' in left menu to check on the status of the new job. A line for the new job should show at top of table. Check for [generating cohort prostatectomy: Source Name (Source Key)]

1. Click Cohort Definitions in left menu

1. Click on ‘Prostatectomy’ at top of list of cohorts definitions. If the cohort definition is not at top, click on the 'Created' column header in the table until it appears at the top.  Otherwise, if you prepended your title with your ID, you can filter for the new cohort based on your ID.

1. Click ‘Prostatectomy’ Cohort Definition

1. Choose Generation Status tab. Confirm that status is complete, generated is green

1. Choose Analysis Status tab

1. Click multiple Analysis Types [PERSON, VISITS, CONDITION, PROCEDURE, DRUG] and then click on 'Generate'

1. Go to jobs in left menu to check status of the new job. Should be the top job. [Check for HERACLES_COHORT_xxx_Source Key]

1. Click Cohort definitions in left menu

1. Click on ‘Prostatectomy’ at top of list of cohorts definitions. If cohort definition is not at top, toggle create menu header in table until it appear its top.

1. Click ‘Prostatectomy’ Cohort Definition

1. Choose Generation Status tab. Confirm that selected Analysis Types [PERSON, VISITS, CONDITION, PROCEDURE, DRUG] are checked green

1. Click Cohort reporting in left menu (See the tutorial on [Exploring Cohort Summary Statistics](/Cookbook/Exploring_Cohort_Summary_Statistics.md) to learn about how to explore this cohort's characteristics)

### Discussion
Defining and generating a cohort is the first step toward more advanced analyses within Atlas. You can specify more complex filters depending on your needs. You may also import concept sets and cohort definitions that have been defined by others. Similarly, you may export these assets and share them with colleagues.

### See Also
[Exploring Cohort Summary Statistics](/Cookbook/Exploring_Cohort_Summary_Statistics.md)
