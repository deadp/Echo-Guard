# Echo-Guard
LLM Powered Bot Detection

Our objective is to engineer a software tool designed to evaluate the potential usefulness of Language Learning Models (LLMs) in identifying signs of disinformation or bot activities within Reddit posts. 

The end product of this endeavor should have the capacity to discern and compare the extent of bot activity across different posts or topics. 

Data Processing Procedure:

Input: A URL corresponding to a Reddit post. 

The software will extract data relating to the comments and users engaging with the posts, which will then be presented in a table format including the user's name, their comment(s), the date of the post, and potential responsive comments. 

To further optimize the process, we'll enrich the table to create comprehensive data profiles of each user interacting with the post. This extended data set will include:

- Their last 25 comments.
- The list of subreddits they've interacted with.
- Their last 10 posts.

Below, we present a set of heuristics that our model will consider to flag potential bots:

|Heuristic|Description|
|---|---|
|Account age|Newer accounts are more likely to be bot-related.|
|Karma|Accounts with minimal karma points tend to be bot-operated.|
|Account verification|Unverified accounts present a higher probability of being bots.|
|Reddit employee|Accounts linked to Reddit employees are less likely to be bots.|
|Variance in time interval between posts/comments|Accounts demonstrating high frequency of comments or posts within a short timeframe can be indicative of bot behavior.|
|Variance in content of posts/comments|Accounts that repeatedly post identical comments or posts are suspected of bot activity.|

Leveraging this collected data, we will train a GPT-based model to estimate the probability of user accounts displaying bot-like or disinformation-related behavior. 

The ultimate goal is to equip the LLM with the ability to identify both overtly bot-operated accounts as well as more nuanced activities, such as accounts making jesting comments or spreading disinformation.
