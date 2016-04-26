## Identifying Patients Dignosed With _Afib_ and Taking Anti-arrhythmia Medication

### Problem

To identify the set of patients that have atrial fibrillation (_Afib_) and started taking an anti-arrhythmia medication after diagnosis.

### Solution

Use the vocabulary search feature to search for the concept codes associated with the proposed __Afib__ cohort via one of two options.

1. To find the set of patients that have Atrial Fibrillation (Afib) and are on an Anti-Arrhythmia medicine, search for the concept codes to create Afib cohort via one of two options: a) __by searching by name__ or b) __searching by icd-9 code__.   

1. __Search by name__:    

  1. Use the vocabulary search by clicking on 'Vocabulary Search' on the left navigation.   

  1. Type Atrial Fibrillation and hit 'Enter'   
![Search Atrial Fibrillation by Name Part 1](images/afib/atlas-search-afib-1.png)

  1. Click on 'Standard' under 'Standard Concepts' on the left side.   

  1. Sort the records based on record count (RC). This give you a sense of how the data is populated in the database.   
![Search Atrial Fibrillation by Name Part 2](images/afib/atlas-search-afib-2.png)

1. __Search for the ICD-9 Code__

  1. Alternatively in the vocabulary search bar, type 427.31 for Afib. This will return ID 44821957. You'll notice that 'Atrial Fibrillation' is in red, which means that it is a non-standard vocabulary based on OHDSI.   
![Search Atrial Fibrillation by ICD Part 1](images/afib/atlas-search-afib-icd9-1.png)
![Search Atrial Fibrillation by ICD Part 2](images/afib/atlas-search-afib-icd9-2.png)

1. Our OHDSI instance only uses standard vocabularies, so click on 'Atrial Fibrillation'   
![Search Atrial Fibrillation by ICD Part 3](images/afib/atlas-search-afib-icd9-3.png)

1. click on 'Related Concepts' to find the concept to select.   
![Search Atrial Fibrillation by ICD Part 4](images/afib/atlas-search-afib-icd9-4.png)

1. After the concept(s) are found, click on the shopping cart icon next to each concept. As each concept is selected, it will be added to the 'Concept Set' on the left navigation.   
![Search Atrial Fibrillation Add to Shopping Cart](images/afib/atlas-search-afib-icd9-5.png)

1. After all the relevant concepts are added to the shopping cart, click on the 'Concept Set' link on the left-navigation.   
![Search Atrial Fibrillation Concept Set](images/afib/atlas-search-afib-icd9-6.png)

1. Click on the 'Export' tab on the top of the right-pane.   

1. Copy the contents of the field 'Concept Set Expression JSON' and paste it to a scratch notepad: this is a JSON representation of the concept set. You will use it later when creating your cohort.   
![Search Atrial Fibrillation Export Concept Set](images/afib/atlas-search-afib-icd9-7.png)

1. Follow the above steps for finding antiarrythmic drugs. (Try this on your own)   
![Search Anti-Arrythmic Drug](images/afib/atlas-search-antiarrhythmic-1.png)
![Search Anti-Arrythmic Drug Add to Shopping Cart](images/afib/atlas-search-antiarrhythmic-2.png)
![Search Anti-Arrythmic Drug Export Concept Set](images/afib/atlas-search-antiarrhythmic-3.png)

1. Click on 'New Cohort Definition' to create cohort definition and name it 'AFib Test'.

1. Select 'Condition Filter' in the 'Add Primary Even Filters' drop-down.   

1. Select '+' icon to add a concept set.   

1. Under the 'Concept Sets' tab, click 'Import'   

1. Paste the JSON that was copied earlier.   
![Import Atrial Fibrillation Concept Set](images/afib/atlas-cohort-definition-afib-condition-import-1.png)

1. Click Save.   

1. Name the concept 'AFib Conditions'.   
![Save Atrial Fibrillation Concept Set](images/afib/atlas-cohort-definition-afib-condition-import-2.png)

1. Do the same for the anti-arrhythmia drugs, and name the concept set 'ArrhythmiaMeds'.   
![Import Anti-Arrythmic Drug Concept Set](images/afib/atlas-cohort-definition-afib-antiarrhythmic-import.png)

1. Click the 'Expression' tab again.   

1. Click on 'Add Additional Filters' in order to add the drug filter.   
![Additional Filter for Anti-Arrythmic Drugs](images/afib/atlas-cohort-definition-antiarrhythmic-filter-1.png)

1. Select at least 1 occurrence of drug exposure 'ArrhythmiaMeds' occurring 0 days before and all days after the index, which is the time an Afib diagnosis was observed.   
![Final Cohort Definition](images/afib/atlas-afib-cohort-definition-final.png)

NOTE: Make sure that 'Descendants' are selected for both 'Atrial fibrillation' and 'Antiarrhythmic' concepts. You can check this by clicking on the 'Print Friendly' tab.   
![Print Friendly of Concept Sets in Cohort](images/afib/atlas-afib-cohort-definition-print-friendly.png)

NOTE: If not, you need to click on the check under 'Descendants' to have the descendants displayed.   
![Selecting Descendants](images/afib/atlas-afib-concept-descendants.png)

1. The final cohort counts can be viewed after clicking 'Generate' under the 'Generation Status' Tab.   
![Final AFib Cohort Counts](images/afib/atlas-afib-cohort-definition-results.png)


### Discussion
you can define and generate more advanced cohort within Atlas use complex filters that match needs. You may also import concept sets and cohort definitions that have been defined by others. Similarly, you may export these assets and share them with colleagues.

### See Also
[Exploring Cohort Summary Statistics](/cumc-dbmi/Atlas-wiki/Cookbook/Exploring_Cohort_Summary_Statistics)
