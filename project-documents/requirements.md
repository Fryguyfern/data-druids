# Requirements Workup
## Requirements
1. Users need to be able to log in with a username and passcode
2. Users need to be able to create a login
3. Users need to be able to access the site and interact with notes/entries without logging in, but may not save their notes/entries without a login
4. Users need to be able to post entrties to their journal once logged in, adding it to the database
5. Users need to be able to see, search, and edit their entries into their journal, and consequentially, the database
6. Users need to be able to 'star' some of their entries
7. Users need to be able to view their 'starred' entries
8. Users must not have access to other users entries in any way
9. Users need to be able to access a 'splash screen' detailing their recent journaling history
10. Users need to be able to categorize their entries when making them
11. Users need to be able to adjust an entries categories after posting them to their journal
12. Users need to be able to 'wipe' their journal
13. A journal wipe must come with at least 2 steps of confirmation
14. The google API must be able to pull a logged in user's recent (last 7 days) journal entries and provide a text summary based on the text content and categories of those entries
15. The Google API must be able to pull a logged in user's 'starred' journal entries and provide a text summary based on the text content and categories
16. Users should be able to quickly and freely sqitch between a view of the 'recent' and 'starred' summaries
17. Users should be able to edit any entry they can see from any page that displays it
18. Users should be able to have their login remembered on a specific device
19. Users should be able to make a short note and save it in less than 5 minutes
20. Users should be able to update or change their Username and Passcode
21. Users should not have the same username as another user
22. Users should be able to request prompts for their notes within the create note page
23. Users should be able to edit, or predetermine prompts for their notes

## Design & Modeling
### entities
#### Notes:
ID (PK)
date (date)
userID (int)(FK>User.ID)
categories (List(INT(FK>Category.ID)))
Star (Bool)
TextContent (String)

#### Users:
ID (PK)
Name (unique, String)
Pass (String)

#### Prompts:
ID (PK)
TextContnt (String)
UserID (FK>User.ID)

#### Categories:
ID (PK)
Name (String)
## Elicitation

1. Is the goal or outcome well defined?  Does it make sense?
2. What is not clear from the given description?
3. How about scope?  Is it clear what is included and what isn't?
4. What do you not understand?
    * Technical domain knowledge
    * Business domain knowledge
5. Is there something missing?
6. Get answers to these questions.

## Analysis

Go through all the information gathered during the previous round of elicitation.  

1. For each attribute, term, entity, relationship, activity ... precisely determine its bounds, limitations, types and constraints in both form and function.  Write them down.
2. Do they work together or are there some conflicting requirements, specifications or behaviors?
3. Have you discovered if something is missing?  
4. Return to Elicitation activities if unanswered questions remain.


## Design and Modeling
Our first goal is to create a **data model** that will support the initial requirements.

1. Identify all entities;  for each entity, label its attributes; include concrete types
2. Identify relationships between entities.  Write them out in English descriptions.
3. Draw these entities and relationships in an _informal_ Entity-Relation Diagram.
4. If you have questions about something, return to elicitation and analysis before returning here.

## Analysis of the Design
The next step is to determine how well this design meets the requirements _and_ fits into the existing system.

1. Does it support all requirements/features/behaviors?
    * For each requirement, go through the steps to fulfill it.  Can it be done?  Correctly?  Easily?
2. Does it meet all non-functional requirements?
    * May need to look up specifications of systems, components, etc. to evaluate this.

