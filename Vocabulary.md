Atlas provides the ability to search and explore the OMOP standardized vocabulary. This functionality was originally built as part of the Hermes working group and now Hermes has been fully incorporated into Atlas. 

Select "Vocabulary" in the Atlas left hand menu to bring up the search screen. You will see 4 tabs: search, advanced, results and import. Each section will be described in more detail.

## Search

Type in a search term and Atlas will search the entire standardized vocabulary for concepts that match that term. It will do a wildcard search so if you search for a term like "dementia" it will look for concepts that contain the term dementia. Once the search is complete, the results will show in the results tab.

## Advanced

This will allow you to perform a search query and specifically filter the results down to a specific set of vocabularies and domains. 

## Results

The results area will show you the results from either your basic search or advanced search. This screen will allow you to further refine your search results using the filters that appear to the left of the grid. Here are the list of filters and how they work:

1. Vocabulary: This will allow for filtering down to a specific vocabulary.
2. Class: This will allow for filtering down to a specific class of concepts.
3. Domain: This will allow for filtering down to a specific domain.
4. Standard Concept: Allows for filtering down to standard concepts.
5. Invalid Reason: This will enable for filtering out invalid concepts.
6. Has Records: If you have configured a source daimon for your CDM, this filter will enable you to determine which concepts contain data in your CDM.
7. Has Descendant Records: Similar to "Has Records", it enables you to filter on concepts where descendant concepts contain data in your CDM.

The concepts in the results will contain the following information:
- Concept ID: Unique concept ID in the vocabulary
- Code: The original code that is used in the source vocabulary
- Name: The name of the concept. This field is color coded by: 
    - Green: Categorization Concept
    - Blue: Standard Concept
    - Red: Non-standard concept
- Class: The class of concept from the source vocabulary
- RC: The record count. This will show the number of records that are coded with this concept in the CDM.
- DRC: The descendant record count. The DRC column will show the sum of all descendant concepts that are coded in the CDM. 
- Domain: The domain of the concept.
- Vocabulary: The vocabulary associated to this concept.

The table of results also has the following features:

- Paging: the default page size if 15 and this can be modified using the drop down appearing just above the results table. You can also page through the data using the paging functionality on the right side of the results table.
- Filtering: There is a filter text box that appears in the upper right hand corner of the results table. Typing a term in this box will dynamically filter the results.
- Sorting: The table allows for sorting on each column
- Shopping Cart: Clicking on the shopping cart will allow you to select the concept for use in new Concept Set (see below).  If you do not have a concept set open, this will automatically start a new concept set for you.
	
## Import

The import tab provides a means for importing concepts into a new concept set. Concept sets are described in more detail in the section below. This section allows you to import concepts in the following ways:

1. Concept Identifiers: use a list of comma delimited concept_ids to import concepts into a concept set
2. Source Codes: use a list of comma delimited source code values to import these concept into a concept set
3. Concept Set: enables you to import a JSON object that represents a concept set
