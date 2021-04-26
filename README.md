# Analysis of Kickstarter Campaigns
## Overview of Project
This analysis uses excel to identify trends for starting a successful kickstarter campaign using data from over 4000 multi-industry campaigns in various countries. Throughout the analysis, I use pivot tables and the ```COUNTIFS()``` formula to extract data based on launch date and fundraising goals

## Purpose
The purpose of this analysis is to find the best time of year to launch a campaign and an ideal fundraising goal for a theatre campaign.

## Analysis and Challenges

### Analysis of Outcomes Based on Launch Date
To find the optimal time of year to launch a theatre campaign, I used a pivot table to extract the number of successful, failed and canceled outcomes sorted by the month they were launched. 

### Analysis of Outcomes Based on Goals
To determine a fundraising goal, I looked at the number of successful, failed and cancelled play outcomes based on fundraising goal, breaking up the fundraising goals into increments of $5,000. Using the ```COUNTIFS()``` formula, I filtered for the data for the specific goal increments, outcome type and category. 

### Challenges and Difficulties 
To avoid typo’s in the code, I automated the process by adding the outcome types and goal increments to rows and columns outside the table and anchored those values. Instead of typing ```COUNTIFS(Kickstarter!$D:$D, "<=4999", Kickstarter$D:$D, ">= 1000", Kickstarter!$H:$H, "successful", Kickstarter!$T:$T, "plays")``` into cell ```D4```, I used the below formla and was able to easily copy and past into the cells without having to manually update the outcome type and ragnes manually for each cell. 


![Code](https://user-images.githubusercontent.com/80648379/116000870-f43e6b00-a5bf-11eb-96f8-62221a38eb23.png)



## Results

* The graph Outcomes Based on Launch Date illustrates that the best time of year to start a theatre campaign is May. 
![Theater Outcomes vs Launch](https://user-images.githubusercontent.com/80648379/116017656-3b534d00-a60e-11eb-8c01-018cd3dc3ef9.png)
  From the graph it also looks like the most campaigns were started in May, so I looked at the percentage of successful outcomes to see if May was indeed the best time of year to start a campaign.  
![Percents](https://user-images.githubusercontent.com/80648379/116000590-ee945580-a5be-11eb-8a86-075c33baed42.png)
  
  From the above chart it appears that the May is in fact the best time of year to start a theatre campaign,  with 67% of camapigns that started in May being sucessful. It also looks like the worst time of year to start a campaign is December, only 49% of campaigns that started in December were sucessful. 

* Looking at the Play Outcomes Based on Goals chart, it looks like the most successful campaigns had a fundraising goal of $1,000 or less. For the most part, the percentage of sucessful campaigns declines as the goal increases, with the exception of fundraising goals from $35,000 to $45,000. 
![Outcomes vs Goals](https://user-images.githubusercontent.com/80648379/116018418-fdefbf00-a60f-11eb-963c-86203b903218.png)

* One limitation I found with this dataset is that it did not encompass method of funding raising. I would think the method of fundraising would be an important aspect to look at when starting a campaign and knowing what fundraising strategies worked the best. 

* For a more complete and through analysis, we could have looked at the duration of the campaigns to see if there was a correlation with the length of the campaign and outcomes. We could have also taken outliers into consideration, to make the data more accurate. 


