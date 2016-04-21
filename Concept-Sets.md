Atlas provides the ability to create concept sets: these are lists of concepts from the standardized vocabulary that taken together describe a topic of interest for a study. 

## Browsing concept sets

Selecting the Concept Sets menu option in Atlas will show you all of the concept sets available in the system. This table has filtering and sorting capabilities similar to the [vocabulary results table](https://github.com/OHDSI/Atlas/wiki/Vocabulary#results). From this screen, you can click on an existing concept set to explore its definition or you can click the "Add Concept Set" button to start developing a new one.

## Creating concept sets

There are a few ways to create a concept set. One way is to browse and open existing concept sets or add a new concept set (described above). Another way is to explore the vocabulary and if you find a concept that you'd like to use to start a new concept set, click on the "shopping cart" icon which will create a new concept set and add that concept to it. Your new concept set will now appear at the top of the left hand menu. This allows you to quickly navigate back to the concept set and to indicate that it is your current working concept set. 

To add new concepts to a concept set, use the vocabulary search to find and explore concepts. When you find a concept that you'd like to add, click on the "shopping cart" icon which will add it to the current concept set.  You may also use the "shopping cart" icon to remove items from your current concept set.

## Concept set expression

Once you have one or more concepts in your concept set, you can use the concept set expression tab to further define what concepts should be included in the set. On the concept set expression tab, you will see the list of concepts that you have selected in a tabular format. The table has 3 checkboxes that are used to further select/deselect concepts:

1. Exclude: Selecting this checkbox will prevent that concept from being used in the concept set.
2. Descendants: Selecting this check box will use the vocabulary relationships to automatically select all descendants. If this option is used in conjunction with the exclude option, it will exclude the current concept and all descendants.
3. Mapped: Selecting this check box will use the vocabulary relationships to automatically select all concepts mapped to the selected concept.
	
As you define the concept set expression, you can use the other tabs to explore how the expression is evaluated against the vocabulary to select concepts.

## Included concepts

The included concept tab is used to show all of the standard concepts that are included when the concept set is evaluated. You can use this tab to review the standard concepts that are included as part of the concept set and use the filters on the left hand side to further explore the different properties of these concepts.

## Included source codes

The included source codes tab is used to show all of the non-standard concepts that are included when the concept set is evaluated. You can use this tab to review which source codes are included when the concept set is evaluated. This is useful when attempting to translate from a set of source codes (i.e. ICD9) to standard concepts to ensure that your definition is complete. It is also useful when attempting to ensure that the concept set will translate to other data sources that may have different source codes.

## Export

The export tab is used to export the concept set expression and/or the concept id list. This is useful if we need to share a concept set definition with others outside of our organization. They can then use this information to import this definition using the [import functionality under the vocabulary area](https://github.com/OHDSI/Atlas/wiki/Vocabulary#import). 

## Saving

Concept sets must be named and saved in order to persist them between Atlas sessions. There is a save button in the top-right of the page that is used to save this work to the database.

## Closing

When you are done using the concept set, you can use the close button in the top-right of the page to close it out. This will also remove the reference in your left-hand menu.