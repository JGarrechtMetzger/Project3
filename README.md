# Project3: Predicting Winners and Losers for NBA Games at Halftime

- The goal of this project to is use a large dataset covering 20 regular seasons of NBA games and predict the winner better than 50% of the time.

  - No data was taken from the 2020 season  to avoid COVID irregularities in gameplay and season structure.

- An applicable use case for this model could be simple betting at halftime.  If the model accuracy is higher than chance (50%) than the model would be helpful for making predictions of winners and losers.  Accuracy is chosen here because it does not make what direction the predcition is made (win or loss), only that it is correct.

- I used the NBA API and to combine over 45,000 matchup observations (2 observations per unique game at 1 per team).

- 21 features were investigated where numerical gameplay featuers were all taken from only the first half of a each game.  No cummulative stats (e.g., Season W-L %) were used in this project.

- The point difference at halftime was the single most important predictor of winners and losers.

  - This feature is labeled as "PLUS_MINUS"

-  Logistic Regression models were found to be >70% accurate and were preffered over the kNN and Random Forest models that yeilded similar results due the increased interpretability of the Logistic Regression Models.  A logistic regression model using only 2 features was >98% as accurate as one that incorporated 21 features suggesting a strong driving force behind the chosen 2 features: Score ("PTS") and score difference ("PLUS_MINUS").

- Suggestions for further work:

  - Incorporate cumulative features such as those that includes team-wide statistics in the season prior to the game being predicted.
  - Look at smaller windows of time such a single season where the lineup for a given team is consistent.
  - Look at differences in Home and Away performance.
  - Look at how second half performance for games lost and games won may help predict the winner at halftime.

  