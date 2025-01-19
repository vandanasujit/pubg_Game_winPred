## Problem Statement

Task 1:-Prepare a complete data analysis report on the given data.
Task 2:-Create a predictive model which is an attempt to predict the win probability
of the Pubg match and to look at the important factors affecting the win probability of
the pubg game.

#### Dataset Link:
###### Link: https://d3ilbtxij3aepc.cloudfront.net/projects/CDS-Capstone-Projects/PRCP-1012-GameWinnerPred.zip
###### Attribute Information
1. Id
2. groupId
3. matchId
4. assists
5. boosts
6. damageDealt
7. DBNOs
8. headshotKills
9. heals
10. killPlace
11. killPoints
12. kills
13. killStreaks
14. longestKill
15. matchDuration
16. matchType
17. maxPlace
18. maxPlace
19. rankPoints
20. revives

21. rideDistance
22. roadKills
23. swimDistance
24. teamKills
25. vehicleDestroys
26. walkDistance
27. weaponsAcquired
28. winPoints
29. winPlacePerc

## Project Workflow
* ##### Data Exploration and Cleaning:

Loaded and inspected the dataset for any missing or erroneous values.
Removed rows that seemed to be not valid.
Performed exploratory data analysis (EDA) to understand the relationships between player statistics and their final placement.
* ##### Feature Engineering:
Selected columns for Prediction with the help of heatmap and correlation matrix.
Dropped irrelevant features for predicting winperc.
Scaled all numerical data and did labelencoding on categorical column MatchType.

* ##### Model Building:

Experimented with various machine learning models, including:
* ###### Linear Regression
* ###### SVR
* ###### Knn
* ###### Decision Tree
* ###### Random Forest
* ###### Gradient Boosting
* ###### XGBoost
Used cross-validation and hyperparameter tuning to optimize model performance.
* ##### Model Evaluation:
Evaluated model performance using metrics such as Mean Absolute Error (MAE) and Root Mean Squared Error (RMSE). Got XGboost as good model in predicting the target.

## Challenges faced in this project
1. ##### Understanding the Features:

Initially, understanding the features in the PUBG dataset was a challenge. The dataset included several columns related to the game, and it was essential to interpret each feature correctly. I researched the PUBG game rules and looked up relevant information online to understand how these features were defined and how they related to player performance. This helped me gain a clearer understanding of the dataset, which was crucial for proper analysis.

2. ##### Dealing with Invalid Data:

Another challenge was identifying and removing invalid data. Some data entries were irrelevant or corrupted, which required me to clean the dataset. By applying the PUBG game rules and context, I was able to filter out invalid entries and improve the quality of the dataset for further analysis.

3. ##### Handling the Large Dataset:

The dataset initially had over 4.4 million entries (4,446,966), which made processing and analysis slow, especially during visualization tasks. Running the code was time-consuming, and visualizing the data using traditional methods was inefficient.
To overcome this, I avoided using inefficient operations like for loops for iterating through large datasets. Instead, I visualized a smaller subset of features at a time (focusing on one to three features) to improve performance.

4. ##### Reducing the Dataset Size:

After cleaning and removing the invalid data, I was able to reduce the dataset size to 105,556 entries. This reduction made the analysis more manageable and improved the efficiency of running code, especially when visualizing data and performing computations.
