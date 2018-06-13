# Predicting the Over/Under for NBA Games 
## Andrew Bosset 
## andrewbosset2019@u.northwestern.edu

SUMMARY: My task was to predict whether two teams would cover the over or under provided by Vegas for each NBA basketball game. This task carries obvious importance due to the betting significance.  Vegas oddsmakers get payed a ton to set perfect odds such as the over/under so it would be quite a feat to have an advantage over their odds. 
	To investigate this, I collected data from various NBA online databases through either developing web scrapers designed for that data or by shear manpower. I focused my data collection on the 2017-2018 season and used weka to try to model learning algorithms to predict whether two teams will pass a overunder. Ultimately my models failed to successfully pick the over or under with any statistical significance. Randomforest topped out as the most successful at 52%. This was after a lot of parameter tweaking which leads me to believe that with more refined attributes and with optimal parameters there is room for improvement.

[Link](url) and ![Image](src)

Markdown is a lightweight and easy-to-use syntax for styling your writing. It includes conventions for

```
Data: The data was a set of 1230 examples or exactly one complete NBA season. 
The data set included the basic stats for both the home and away team
(ft fg,2pt and 3pt stats for attempted made, and percentage. Rebounding rates, turnover rates, assists, steals, and blocks).
I also created the fields of whether or not a team was playing 
back to back nights and how many wins the team had at the time of their game. 
The O/U was what was to be classified. When testing the data I used 10-fold-cv
[Link](url) and ![Image](src)
```

