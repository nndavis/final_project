# final_project
## Authors: Adio Olufemi Peter, Ashlesha Vengareddy, Noah Davis, Ethan Dirksen

Topic:
Take our "Glassdoor Job Reviews" dataset which contains 18 columns: 
1. Firm, 
2. job title, 
3. location, 
4. overall rating, 
5. diversity inclusion, 
6. Culture values, 
7. pros, 
8. cons, 
9. and a few more ratings and things.

Within this dataset we could ask multiple questions: 
- does location affect overall job rating? , 
- are managers bias in their rating?, 
- does location adversely affect diversity inclusion? etc. 

As far as machine learning goes, our "target" would be overall rating and we would "classify"/train our data off whether or not a job is good or bad. Good being ratings 3+ and bad being 2-. We could use the other 17 columns as features, but we would more than likely thin down the long string columns such as "pros" and "cons" as those would be difficult to turn into numerical values which is necessity for machine learning.

Core question:
What are the top 3 factors that impact the overall job rating? or, 
What do future employees look for in a job?

How to train the machine learning model:
Use two datasets. Find things in the sample dataset that indicate a higher overall rating (the rating is 3 or above) and train the model to find what would indicate what makes up a job's overall rating in the test dataset. 

Questions we want answered:
- does location adversely affect diversity inclusion?
- are managers bias in their rating?
- does location affect overall job rating?
