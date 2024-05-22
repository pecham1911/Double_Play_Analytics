## Forecasting and Analyzing Baseball
#### Double Play Analytics

![image](https://github.com/pecham1911/Double_Play_Analytics/assets/159095917/659eea84-0506-47f5-acad-eae626e2b7d7)

#### Overview
This project analyzes the factors associated with forecasting baseball game outcomes and provides key recommendations for success to industry leaders.

#### Business understanding
In the highly competitive and financially driven landscape of professional baseball, accurately predicting game outcomes can significantly impact team performance, fan engagement, and revenue generation. By leveraging historical game data our predictive modeling approach aims to provide teams, broadcasters, and stakeholders with actionable insights into future game outcomes. This predictive analytics tool will empower teams to optimize their strategies, such as player selection, pitching rotations, and in-game tactics, leading to improved win rates and overall performance. Additionally, broadcasters can enhance viewer experience by offering more informed pre-game analysis and real-time predictions during broadcasts. Ultimately, a reliable predictive model for baseball game outcomes has the potential to drive fan excitement, increase ticket sales, and attract valuable sponsorships, thus contributing to the long-term success and profitability of baseball organizations.

#### Data understanding and analysis
The dataset was taken from https://www.retrosheet.org/. They came from the Game logs datset for 2010 through 2023. The data dictionary can be found on the webpage and in the supplemental materials of this repository.

#### Description of data
##### Data shape
After concatenating the thirteen years of data there were 32,484 games (rows of data) and 179 columns/features. 

##### Data manipulation

The target 'win' was created using the (a) score of the visiting team, (b) score of the home team, (c) name of the visiting team, and (d) name of the home team to calcuate the winning and losing team. The rows that represented each game were then divided into two row per game, one for each team and the winning team of the pair was assigned a win=1 and the losing team of the pair was assigned an win=0. Each pair was given the same ID and kept together through the train_test_split. 

X features included: 'at_bats', 'hits', 'double', 'triple', 'home_run', 'sacrifice_hit', 'sacrifice_fly', 'hit_by_pitch', 'walk', 'intent_walk', 'strikeout', 'stolen_base', 'caught_stealing', 'grounded_into_double_plays', 'left_on_base', 'pitchers_used', 'wild_pitches', 'assists', 'errors', 'double_def'. All features used in X were numeric and standard scaled. 

##### Data and analysis limitations
- The COVID-19 pandemic -- 2020 was an incomplete season. The games thate were played should not be notably different from games played in other years. However, it is possible that there were unclear variances impacting games. 

- Baseball provides one of the richest data fields of any sport. The abundance of information provides---challenge.

##### Data modeling, evaluation, and interpretation

These data were completely balanced; 50% of rows won=1 and 50% of rows won=0. A Dummy Classifier---

A grid search looking for the best paramenters was used on both Decision Tree and Random Forest Classifiers to gauge the most important parameters and model features. 

Logistic regression using the full set of X features ----

A Neural Network was conducted with the extensive coding support of ChatGPT. ---c 

This project contains:
Exploratory Data Analysis: 
Training the Model: 
Testing the Model: 

Visualizations

Resources
PRESENTATION: 
TABLEAU: 
