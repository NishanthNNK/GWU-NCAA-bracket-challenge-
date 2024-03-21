# GWU-NCAA-bracket-challenge-

Team Name: JKNN GWU

**Group Members**
1) JongKyu Lee, jongkyu.lee1@gwu.edu, SEAS, MSc Data Analytics
2) Nishanth Nandakumar, nishanth.nandakumar@gwu.edu, SEAS, MSc Data Analytics


**Model Definition**

Our model employs statistical features derived from historical match data to predict the outcomes of NCAA basketball games. Unlike traditional embedding-based approaches, this model leverages a combination of team performance metrics such as field goal percentage (FGP), 3-point field goal percentage (FGP3), and free throw percentage (FTP) to understand and predict game results.

The model operates by processing these key features for each team involved in a matchup:

Team ID (to uniquely identify each team)
Team FGP (Field Goal Percentage)
Team FGP3 (3-Point Field Goal Percentage)
Team FTP (Free Throw Percentage)
Team Score (to incorporate the scoring capabilities of the team)
The model predicts a binary outcome indicating whether team A wins (is_team_a_win = 1) or not (is_team_a_win = 0) based on these features. The features for both teams participating in a matchup are first independently processed and then combined to serve as input to a predictive model that outputs the likelihood of team A winning against team B.

The core model utilizes gradient boosting techniques, specifically XGBoost, to analyze the historical performance and scoring data of the teams. The model was trained and validated on a dataset comprising matches from previous seasons, with a particular focus on accurately predicting the binary outcome of matchups in the NCAA tournament context.

The effectiveness of the model was evaluated using accuracy as the primary metric, in addition to other performance measures such as precision and recall where applicable. Our model tuning process involved experimenting with various hyperparameters, including the number of estimators, max depth, learning rate, and regularization parameters, to optimize performance.
