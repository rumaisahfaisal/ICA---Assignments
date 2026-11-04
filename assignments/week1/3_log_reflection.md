## step 3: check evaluation
### ai proposed questions
1. how do the mean variations compare across the four different items over the tracked observation days?
2. is there a statistically significant difference between the pricing distributions of 'staple A' versus 'oil B' across the recorded cities?
3. what is the maximum absolute price range observed for each individual item throughout the entire timeline?
4. Do all items exhibit synchronized price movements on the same calendar dates, or do specific items lag behind market shifts?
5. What proportion of the total price variance in the dataset can be attributed to differences between item categories versus differences across cities?
 ### Rejected questions and reasons
* **Rejected question 1 (alternative q2):** *"Is there a statistically significant difference between the pricing distributions of Staple A versus Oil B across the recorded cities?"*
* **Reason: comparing pricing distributions directly between staple a and oil b doesnt make sense because they are completely different commodities with different baseline costs. Additionally, our dataset is focused on simple descriptive stats across 96 rows and doesnt contain explicit city level categories to group them area wise.
* **Rejected Question 2 (Alternative Q5):** *"What proportion of the total price variance in the dataset can be attributed to differences between item categories versus differences across cities?"*
* **Reason: this question assumes the data set contains hogh level groupings like item categroies, and distinct city feels. while originally, our clean data set only tracks four specific items overtime, so we cannot perform a breakdown across non existent categories.

## reflect : step 4
this data set showed how easy it is to jump to conclusions when you donot look at the limits first. We only have 96 rows covering 4 basic items across 12 dates. because of this small sample, we cannot claim these prices reflect real world inflation or big market trends across the country.there are no city names, shop tyres, or extra cost factors included. the dataset only lets us calculate basic averages and ranges for these specific 4 items. so we have to keep our conclusions strcitly focused on what the simple numbers show.

## critique of ai suggestion
AI suggested analyzing whether price differences between staple a and oil b were statistically significant across cities. it sounds really smart statistically at first, but if we look closely at the data, comparing completely different items with totally different baseline costs didnt make any sense, plus we didnt even have city category columns. Accepting that tempting ai suggestion would have led me to run fancy stats on unsupported assumptions, so catching it taught me to verify ai questions against the actual data variables before using them.