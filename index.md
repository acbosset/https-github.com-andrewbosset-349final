# Predicting the Over/Under for NBA Games 
## Andrew Bosset 
## andrewbosset2019@u.northwestern.edu

SUMMARY: 
	My task was to predict whether two teams would cover the over or under provided by Vegas for each NBA basketball game. This task carries obvious importance due to the betting significance.  Vegas oddsmakers get payed a ton to set perfect odds such as the over/under so it would be quite a feat to have an advantage over their odds. 
	To investigate this, I collected data from various NBA online databases through either developing web scrapers designed for that data or by shear manpower. I focused my data collection on the 2017-2018 season and used weka to try to model learning algorithms to predict whether two teams will pass a overunder. Ultimately my models failed to successfully pick the over or under with any statistical significance. Randomforest topped out as the most successful at 52%. This was after a lot of parameter tweaking which leads me to believe that with more refined attributes and with optimal parameters there is room for improvement.


(Threshold curve for Over classification on best case Random Forest)
![Naming it](/pic1.png)


Screen Shot 2018-06-12 at 9.24.48 PM.png
```
Data: The data was a set of 1230 examples or exactly one complete NBA season. 
The data set included the basic stats for both the home and away team
(ft fg,2pt and 3pt stats for attempted made, and percentage. Rebounding rates, turnover rates, 
assists, steals, and blocks). I also created the fields of whether or not a team was playing 
back to back nights and how many wins the team had at the time of their game. 
The O/U was what was to be classified. When testing the data I used 10-fold-cv
```


```
Implementation: I uploaded the file to Weka to test out different classification models. First I 
tested the model on zeroR which returned an astonishingly close to even model of 50.6504% accuracy. 
I knew that this would make my task hard as it might be difficult to derive which attributes would be 
involved in a skewed data.. The main classifier I was interested in going in was a Random Forest. 
During experimentation I tested decision tree, RandomForest, Bayes Net, Naïve Bayes, multilayer perceptron, 
logistic regression and Random Committee.  I tested the decision tree and random forest first with the DT 
coming in around 52% accuracy while the random forest failed to achieve half. The benefit I saw in using the 
random forest was the ability to rate the importance of each attribute. Utilizing this random forest was 
able to achieve near 53% as well. I then trimmed almost half of variable and attempted again 
but received less accuracy.
```

![Naming it](/pic3.png)

```
	There were many variables I did not account for such as All-star level talent, injuries, and
the streakiness of teams. Injuries can have a large effect when you consider that I was using
whole season averages so a late season injury or an early season injury to a star can really 
throw that off and the rhythm. One thing I noticed for spreads was that teams that were covering 
tended to continue to cover which didn’t seem to be as prevalent of a trend in O/U. After a certain amount 
of testing it seemed pretty futile to try any more classifiers with as poor as they were all performing.
```
1. ZeroR  -  50.6504%
2. Decision Tree (J48)  -  51.8293 %
3. RandomForest  -     49.187  %
4. Random Committee   -  49.5935 %
5. Bayes Net  -     50.5691 %
6. Naive Bayes   -   51.1382 %
7. Random Forest  -  51.9106 %
8.  Random Forest  - 52.8862 %
9. Multilayer-Perceptron  49.7561 %



```
Discussion: My original intention was to build a model to attempt to predict which team would cover the spread in 
an NBA game. Through the whole beginning of the project that is where my data collection and such was going. 
However a later blunder while updating my csv file resulted in a loss of data that among other issues, 
made the question of the spread more difficult. After attempting to recover the lost data in as many ways 
as I could I decided that maybe the data could lead to a prediction on over/under scores. Obviously sadly, 
this did not go as well as I would have hoped either.
```
```
Futures: Now knowing that I am attempting to answer the question of the total Over/Under for games 
I would focus heavily on certain attributes. One attribute I could immediately add in is the pace of each team. 
This is a well tracked advanced metric in the NBA. However after this project I have realized how accurate 
the oddsmakers are when they set lines. It is clear that any attribute I would gage as important is readily at 
the hands of the odds makers and much easier to obtain. I’m under the impression that for odds such as the 
spread or the over/under there is little if anything I could do to completely overmatch the oddsmakers.
```
Member Contributions:  I was the sole member.
