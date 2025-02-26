# Data-driven understanding on soccer team tactics and ranking trends: Elo rating-based trends on European soccer leagues

## Abstract
In modern soccer, strategy and tactics significantly impact team success. In this study, the application of these methodologies within the domain of association soccer is examined, with a particular focus on predicting team strategies via team trend analysis. Using a dataset comprising matches from the top five European soccer leagues, we analyzed team performance trends over time using the Elo rating system and rolling regression. Predicting strategies from soccer match datasets is a challenging. In our study, we propose methods based on count and rank to address these challenges.For the count-based method, the number of forwards, midfielders, and defenders is used to calculate respective defense and attack scores. For the rank-based method, teams are classified into various levels based on their rankings, and strategies are evaluated accordingly. This approach provides a more detailed perspective on strategic tendencies by considering team composition and performance at each level. Experimental results demonstrate the potential of our proposed methods to accurately identify and predict team strategies, offering significant implications for tactical decision-making in professional soccer. The findings indicate that the accuracy of predicting defensive strategies using count-based predictions was approximately 85\%, while the performance of predicting aggressive strategies through rank-based predictions was 89\%. Our methodology can be extended to the development of a predictive model aimed at forecasting team strategies, thereby assisting coaches with more effective preparation for upcoming matches.

## Identifying upswings and downswings

Fig illustrates these trends by using a rolling regression based on the Elo rating system. The figure depicts the Elo ratings and rolling regression trends for the four representative Serie A teams, highlighting the upswings (green dots) and downswings (red dots). 

<figure>
  <p align="center">
    <img src="Soccer Team Trend.png" alt="Trulli" style="width:80%">
    <figcaption align = "center"><b>Soccer Team Trend : For example, the Elo ratings of Milan, Hellas Verona, Udinese, and Spezia are plotted against matchdays, with trend lines from the rolling regression superimposed.</b></figcaption>
  </p>
</figure>

## Model evaluation

Fig(a) presents the confusion matrix based on count-based data, which reveals better accuracy in predicting defensive strategies than offensive strategies. Conversely, Fig(b) presents the confusion matrix based on ranking-based data, indicating superior accuracy in forecasting offensive strategies compared with defensive strategies. Both methodologies exhibit distinctive advantages: one excels at predicting offensive strategies, whereas the other is proficient in forecasting defensive strategies, each with its inherent strengths and weaknesses.

<figure>
  <p align="center">
    <img src="Confusion Matrix.png" alt="Trulli" style="width:80%">
    <figcaption align = "center"></figcaption>
  </p>
</figure>


## Soccer Data.xlsx
We collected data from various websites, including sports-reference(https://www.sports-reference.com/) covering 3652 games played by 98 teams throughout the season. The data that we focused on included aspects such as matchday, team name, opposing team, team formation, opponent formation, match result, home/away status, GF, GA, and team rank. Furthermore, to add depth to our analysis, we also used worldfootball(https://www.worldfootball.net/)to obtain real-time team rankings after each matchday.

## Model parameters
All analyses and model computations were performed using Python. The parameters set during training for each proximity are as follows: batch size = 128 and epochs = 10. We used the Adam optimizer with a dropout rate of P drop = 0.1 and a learning rate of 0.01. Dropout was applied to the output of each sub-layer, and L2 regularization (weight decay) of 0.001 was applied in the fully connected layers.

https://journals.plos.org/plosone/article?id=10.1371/journal.pone.0318485
<!---
--->
