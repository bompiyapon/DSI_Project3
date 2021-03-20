# DSI_Project3 Subreddit Classifier

## Problem Statement
----------------------------
In this project, we will try to classify by the text input (from post) which subreddit should the post be the reddit and auto classify to that subreddit. For instance, player on reddit no longer need to look for game subreddit themself anymore just post and model will predict which game subreddit this post should be in!

This is the proof of concept of the project the classify subreddit game. Which will create model to classify League of Legends (LoL) and DotA2 by gathering posts from subreddit /r/leagueoflegends and /r/DotA2. For, furthermore we hope model can classify all game post in the subreddit


## Executive Summary
----------------------------
A subreddit is a specific online community, and the posts associated with it, on the social media website Reddit. Subreddits are dedicated to a particular topic that people write about, and they're denoted by /r/, followed by the subreddit's name, e.g., /r/gaming. You can subscribe if you like that topic or you can unsubscribe if you dont.

With the problem statement we will try to increase accuracy of subreddit classification utmost to make the correctness of subreddit the post should be in

### Key Takeaways
----------------------------
- With NLP the unique word which help model to identify subreddit such  as name of players, shoutcaster and etc.
- The differentiate of the name also have high impact on it. For example, character in DotA called 'hero' while in LoL called 'champion'.
- Due to DotA2 and LoL are MOBA game, If we remove some general word which occur in 2 game post will help model classify more efficiency


### Data Dictionary
----------------------------
1. Firstly, I have called API of reddit which is /r/DotA2 and /r/leagueoflegends and save as .csv file name 14March_dota2_post.csv and 14March_league_post.csv
2. Base on these post to implementing model to  classify

| Feature | Type   |Description |
|----|----|----|
|title    | object | Title of the post in subreddit |
|text     | object | Text in the post |
|subreddit| object | Subreddit label which use as a target variable to classify |
|all_text | object | Feature engineering which concatenate text from title and text together |


### Conclusion
----------------------------
Our model correctly predicts 89.3% of the observations
- Among posts that our model predicted to be in /r/DotA2, we have 94.44% of them correctly classified.
- Among posts that our model predicted to be in /r/leagueoflegends, we have 82.63% of them correctly classified.
- Removing the general word (which occur in both subreddit) can help improve the model accuracy.

Scope for future improvements:
- Try other ensemble models, such as using boosting , SVM
- Ability for model to classify more than two subreddits
- Improve the false positive value (predicted LoL as DotA)
