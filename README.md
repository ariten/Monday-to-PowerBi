# Monday-to-PowerBi
This repo is documenting the queries i have used and made to bring in a monolithic board with several thousand records

The GetFirst and GetNext queries are originally developed by [@hmbouk](https://gist.github.com/hmbouk) on their [Gist Post](https://gist.github.com/hmbouk/b5712f8d4639eb85328bf4828b402284) and have been adapted for the specific use case i have. 

SourceTable is a designed to accept 1 single large board and is specifically written to handle the returns from these queries, if you amend the queries you will need to amend the steps following List.Generate. 

1 further note, For all of this to work, GetFirst and GetNext must return the exact same format of data, The first api call returns the object boards where as the cursor api calls retursn the object next_items_page, in the GetFirst and GetNext queries i normalise the returns to be Cursor and Items and nothing else. 

Update: 
- A [issue](https://github.com/ariten/Monday-to-PowerBi/issues/1) was raised on the repo that outlined the solution was missing the last page of a board, when the board holds over 1500 items this bug presents. The solution was developed by [@tomiapo](https://github.com/tomiapo) and can found on their [repository](https://github.com/tomiapo/monday-to-powerbi), i have updated this repo to reflect their solution and have verified this solution does fix the bug.
