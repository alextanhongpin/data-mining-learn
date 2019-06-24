# data-mining-learn
Knowledge base for data mining


## Affinity Analysis

Compare the different data mining algorithms for affinity analysis, especially apriori and eclat. Repo [here](https://github.com/alextanhongpin/affinity-analysis).

## CRISP-DM

Cross Industry Standard Practice for Data Mining. Try to implement the full steps.


## Frequent Itemsets

Use frequent itemsets for food recommendation, create packages (food, drink and misc.), log the most frequently purchased and perform recommendations.


## Mining high-utility itemsets in transaction database

Take a look into the algorithms and see how to apply it.

https://www.philippe-fournier-viger.com/spmf/mHUIMiner.php

## Frecency

https://developer.mozilla.org/en-US/docs/Mozilla/Tech/Places/Frecency_algorithm

one way is to bucket the counter for each time the request hit, e.g. hourly

hour 24: 10
hour 23: 50
hour 22: 3
…

then, take the last N buckets to determine the ranking of the item. Another way is to add them in buckets with different range of data:

4 days bucket, weight: 100
14 days bucket: weight: 70
31 days bucket: weight 50
90 days bucket: weight 30
rest, 10:

The more frequent and recent ones will have a higher score. How can we do this with redis set?

Another easier way is just to check the usage in the last seven days. 
day 7 * 100
day 6 * 80
day 5 * 60
day 4 * 40
day 3 * 20
day 2 * 10
day 1 * 5
the sum of the scores is the recency score. Create fake data to check the distribution. 

## References

- https://www.janbasktraining.com/blog/what-is-data-mining/
- https://www.mssqltips.com/sqlservertutorial/4002/data-mining-algorithms-overview/
- https://searchdatamanagement.techtarget.com/definition/RFM-analysis
- https://stackoverflow.com/questions/43233300/sql-determine-recency-of-a-value
- https://www.deep-data-mining.com/2012/09/recency-frequency-monetary-rfm-analysis_9313.html
- http://www.silota.com/docs/recipes/sql-z-score.html
