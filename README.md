# AN ANALYSIS OF KICKSTARTER CAMPAIGNS
## Overview of Project
This analysis is done on Kickstarter dataset to visualize campaign outcomes based on their launch dates and their funding goals, and also to uncover any underlying trends between the outcomes and the launch date, and the outcomes and the funding goals.

## Analysis and Challenges
### Outcome Based on Launch Date
The first step in the analysis was to convert Unix tmestamps for launch date to readable date format.The year from the date was extracted in a separate column and then used to create a pivot table to reflect the outcomes of theatre campaigns during each month of the year. Using this information a pivot chart was created to show the count of successful, failed and canceled campaigns.
![Theater_Outcomes_vs_Launch](https://user-images.githubusercontent.com/86074187/123528916-93173e80-d6b9-11eb-8928-bc25b2415922.png)
### Outcome Based on Goals
In order to complete this analysis, different ranges with a difference of $5000 from less than $1000 to greater than $50000 were considered. For each range, COUNTIFS() function was used to count the total number of plays with different outcomes i.e. successful, failed or canceled. By adding the number of successful, the number of failed and the number of canceled plays, total number of project was calculated for each range. Using total number of project and number of successful and number of failed campaigns we calculated percentage of succesful campaigns vs percentage of failed campaigns.
A pivot chart was also created depicting the relationship between percentages and the funding goal ranges.
![Outcomes_vs_goals](https://user-images.githubusercontent.com/86074187/123529409-e4293180-d6bd-11eb-8aca-9780e2f5a534.png)
### Challenges in Analysis
The biggest challenge while analyzing Outcomes based on goals is that the failed campaigns on average had a much higher goal but their pledged amount is much lesser than the successful campaigns. Had goal been the issue, the pledged amount for both successful and failed campaigns would roughly be equal. Therefore, due to limitation of information it is difficult to derive a direct relationship between goal and success rate.

## Result
### Conclusion on Outcomes Based on Launch Date
* Based on the pivot chart, the highest number of succesful campaigns are launched in May.
* The lowest number of succesful campaigns are launched in December.
### Conclusion on Outcome Based on Goals
* The highest success rate is for campaigns whose goal range less than $1000. The higher the range, the lower the success rate.
### Limitations
By looking at pivot charts, we can say that there are other factors also that affect the success rate of the show which are not taken into account during our analysis. For example, you see an increase in success rate between the goal range of $30000 and $40000, denying the general trend of lower goal--->higher success rate. 
### Recommendations
We could have possibly looked at the sum of pledged funds during different months to see if there is a relationship between the month and the amount of pledged funds. That would give us insight into which month to launch a campaign based on goal.
