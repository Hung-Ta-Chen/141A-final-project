## 141A-final-project

Briefly project description:

Ultimate Fighting Championship (UFC) is the most prestigious MMA promotion throughout the world. Our goal is to analyze the data about every UFC fight that happened before 2021 and then predict the winners in the future fights by addressing the several questions we listed below. We will use several data analytical methods to address the questions. 

Briefly data description:

The dataset is a list of every fight in UFC from 1993 to 2021. Each row represents one fight, and it contains several pre-fight stats of each fighter, background information about the fight, and the outcome of the fight. The dataset has 6007 rows and 46 columns in total before cleaning. And then we use that data to predict the winning rate of each fighter and the winnerfight.
Source: UFC-Fight historical data from 1993 to 2021 | Kaggle


Questions to be Addressed:		

Is there any relationship between variables?

Weight class vs Win by knockout 

Average takedown attempt vs  Total rounds fought

Height vs Average significant strikes landed

Can we predict the winner of the fight with fighters’ pre-fight stats and other background information?

Can we separate fighters into different groups based on their pre-fight stats?
						 						
					
Methodology:

To discuss the win rate and finding the relationship between the variables, we will first split the data into the tactics/win rate, and then remove NA and transform the data into the data frame for regression. On this step we will apply clustering on the tactics to minimize the number of variables.

We will use ggplot and histogram to visualize the different variables and display our clustering results.

We will apply different modelings such as cluster analysis, logistics analysis, neural network and decision tree to classify fighters and predict the winner.

We will use k-fold cross-validation to find the best model for the prediction. 
