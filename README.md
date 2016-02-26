This is a python tool to calculate WOE (Weight Of Evidence) and Information Value of binary classification dataset. WOE is an approach to encode a categorical feature to a continuous value stands for the events frequency odds.

WOE = ln(percent of events / percent of non-events) e.g. events means y=1 rows and non-events means y=0 rows

Information Value (IV) is a measure of the predictive capability of a categorical feature to accurately predict the events.

IV(i) = (percent of events - percent of events) * WOE (for each category label) The total IV of a variable is the sum of IV's of its categories. 

Following is what the values of IV mean according to Siddiqi (2006): 
•Information Value Predictive Power 
• < 0.02 useless for prediction 
•0.02 to 0.1 Weak predictor 
•0.1 to 0.3 Medium predictor 
•0.3 to 0.5 Strong predictor 
• > 0.5 Suspicious or too good to be true 

Methods:
•woe -- Calculate woe of each feature category and information value. Returns numpy array of woe dictionaries, and numpy array of information value of each feature.
•woe_single_x -- Calculate woe and information for a single feature. Returns woe dictionary, and information value of this feature.
•woe_replace -- Replace the explanatory feature categories with its woe value. Returns the new numpy array in which woe values filled.
•combined_iv -- Calcute the information vlaue of combination features. Returns woe dictionary and information value of combined features. This method is in order by work with evolutionary algorithms like PSO or GA to select optimized features combination.

Details please refer to comments in the code.
