## Defining a Cohort Based on a Diagnosis

### Problem
You want to define cohort of patients who all have a diagnosis of essential hypertension and generate results showing the number of patients in the cohort.

### Solution
 1. On the *Cohort Definitions* page, click the **New Cohort Definition** button.  
 ![New cohort definition button](images/01-new-cohort-defn.png)

 1. Type 'Essential Hypertension' in the red box. This will name the definition so we can locate it later.  
 ![Name cohort definition](images/01-name-cohort-defn.png)

 1. Click the **Add Primary Event Filters** dropdown and select *Add Condition Filters*. A new filter, a condition occurrence of _Any Condition_, appears. _Any Condition_ is a concept set which represents any condition. We must instead create and reference a concept set that represents essential hypertension.

 1. Click the **+** button beside _Any Condition_.   
 ![Create concept set](images/01-create-concept-set.png)

 1. The *Concept Sets* tab is activated and a new concept set is created. Type 'essential hypertension concept set' to name the concept set we are about to create.

 1. Click the **Add** button and type 'Essential hypertension' to search the vocabulary for concepts containing this phrase. Locate and select the concept with concept id 320128. Click the **Add And Close** button to complete the operation.  
 ![Add concept](images/01-concept-set-add-concept.png)

 1. Click the **Save** button beside the cohort definition name (i.e. 'ID - Essential Hypertension').  
 ![Save cohort definition](images/01-save-cohort-defn.png)

 1. On the *Generation Status* tab, click the **Generate** button.  
 ![Generate cohort definition](images/01-gen-cohort-defn.png)

 1. When the job completes (approximately 20 seconds), the *Generation Status* tab will be updated and will display the count of patient records containing a diagnosis of essential hypertension.

### Discussion
Defining and generating a cohort is the first step toward more advanced analyses within Atlas. You can specify more complex filters depending on your needs. You may also import concept sets and cohort definitions that have been defined by others. Similarly, you may export these assets and share them with colleagues.

### See Also
[Exploring Cohort Summary Statistics](/Cookbook/Exploring_Cohort_Summary_Statistics)
