# Module 1 Challenge

## Overview

This project provides Louise with information about how different campaigns fared in relation to their launch dates and their funding goals. Using the Kickstarter dataset that Louise and others provided, this project helps Louise visualize Kickstarter campaign outcomes based on their launch dates and their funding goals. This report can be provided to Louise to help her decide when to lauch a funding campaign for her new play and what an appropriate fundraising goal should be. 

## Analysis and Challenges
Using the data provided, the fundraising campaign outcomes for plays were analyzed based on both launch dates and funding goals. 

### Analysis of Outcomes Based on Launch Date
To understand the interaction between the outcomes of theater kickstarter fundraising campaigns based on their launch dates required filtering the data to select only the theatre category and then reinterpreting the creation date column that had earlier been changed to a user friendly format, and extracting the year. Now results for theatre kickstarter fundraising campaigns can be grouped and then broken down by outcome (successful, failed, cancelled). The resulting Pivot Table looks like this:

[Kickstarter campaign outcomes based on months_PivotTable](resources/Outcomes_by_launch_month2.PNG)

### Outcomes Based on Launch Date Visualization
For the analysis of kickstarter campaign outcomes based on the launch date's month, the following image shows the number of successful, failed and cancelled theatre events. It appears that overall more campaigns were launched during the summer months; although if you launch a campaign in May you have the best chance of success. In this visualization it appears that there are always more successful theatre campaigns than failed ones and a few cancelled campaigns appear as well. March, January and Decomeber are the three months that I would not advise Louise to start her kickstarter campaign becuase those months appear 

[Kickstarter campaign outcomes based on month lanched](resources/Theater_Outcomes_vs_Launch2.png)

### Challenges related to Outcomes Based on Launch Date
The challenges for this analysis were: 
* converting the date of camapaign creation (launch) from its original format in the data into a human readable short date 
* extracting the year from that date
* creating the pivot table to correctly show the months instead of the years while breaking out the columns for the campaign outcomes of success, failure, cancelled.
* sorting the months! they started out with Dec first and I had to resort them to correctly show Jan - Dec. 

### Analysis of Outcomes Based on Goals
To understand the interaction between the fundraising goals and the success or failure of the fundraising campaigns, the number of successful, failed and cancelled outcomes of each campaign for plays were counted. Then using this information, the percentage of each type (success, failure, cancelled) was computed for selected ranges of fundraising goals in intevals of $5,000, starting with less than $1,000 for small campaigns, and going up fundraising goals to $50,000 or more. This breakdown of goals was designed to help Louise determine a reasonable goal amount for her play's kickstarter campaign. 

### Outcomes Based on Goals Visualization
For the analysis of kickstarter campaign outcomes, the following image shows the percentages of successful, failed and cancelled plays based on the fundraising goals. 
[Kickstarter campaign outcomes based on goal ranges](resources/Outcomes_vs_Goals.png)

There are several things to notice in this image:

* None of the theatre campaigns were cancelled in the given data.
* Live plays were not including in this analysis.
* When the fundraising goals were between $1,000 - $4,999 there weren't any failed campaigns
* When the fundraising goals was less than $20,000 there were always more successes than failed campaigns. 
* Then when the fundraising goals were just under $35,000 up to $45,000 more campaigns failed than succeeded. 
* Next, the fundraising goals from $35,000 to just under $45,000 gave more successes than failures but both success and failure were present.
* Finally, fundraising goals of $45,000 or greater failed more often than succeeded, with the goal range of $45,000 to just under $50,000 showing no successes.
* It is not clear from this image why these fundraising goal ranges show such a pattern. There must be some other variable lurking that casued these results. 

### Challenges related to Outcomes Based on Goals
One challenge in doing this analysis were that my computer is a little older and therefore working with an Excel file with so many worksheets plus so many forumlas embedded in it meant I needed to manually save the file pretty frequently. 

Another challenge was figuring out which columns held the outcomes, goals and the subcategory plays and then applying these columns with specific values for the breakdown of the goals to each cell. For example, here are the formulas for the 'Number of Successful Plays) based on the specified fundraising goals. 
Number Successful
=COUNTIFS(KickStarter!$D:$D,"<1000",KickStarter!$F:$F,"successful", KickStarter!$R:$R,"plays")
=COUNTIFS(KickStarter!$D:$D,">=1000",  KickStarter!$D:$D,"<5000",KickStarter!$F:$F,"successful", KickStarter!$R:$R,"plays")
=COUNTIFS(KickStarter!$D:$D,">=5000",  KickStarter!$D:$D,"<10000",KickStarter!$F:$F,"successful", KickStarter!$R:$R,"plays")
=COUNTIFS(KickStarter!$D:$D,">=10000",  KickStarter!$D:$D,"<15000",KickStarter!$F:$F,"successful", KickStarter!$R:$R,"plays")
=COUNTIFS(KickStarter!$D:$D,">=15000",  KickStarter!$D:$D,"<20000",KickStarter!$F:$F,"successful", KickStarter!$R:$R,"plays")
=COUNTIFS(KickStarter!$D:$D,">=20000",  KickStarter!$D:$D,"<25000",KickStarter!$F:$F,"successful", KickStarter!$R:$R,"plays")
=COUNTIFS(KickStarter!$D:$D,">=25000",  KickStarter!$D:$D,"<30000",KickStarter!$F:$F,"successful", KickStarter!$R:$R,"plays")
=COUNTIFS(KickStarter!$D:$D,">=30000",  KickStarter!$D:$D,"<35000",KickStarter!$F:$F,"successful", KickStarter!$R:$R,"plays")
=COUNTIFS(KickStarter!$D:$D,">=35000",  KickStarter!$D:$D,"<40000",KickStarter!$F:$F,"successful", KickStarter!$R:$R,"plays")
=COUNTIFS(KickStarter!$D:$D,">=40000",  KickStarter!$D:$D,"<45000",KickStarter!$F:$F,"successful", KickStarter!$R:$R,"plays")
=COUNTIFS(KickStarter!$D:$D,">=45000",  KickStarter!$D:$D,"<50000",KickStarter!$F:$F,"successful", KickStarter!$R:$R,"plays")
=COUNTIFS(KickStarter!$D:$D,">=50000",KickStarter!$F:$F,"successful", KickStarter!$R:$R,"plays")


## Results
In Conclusion, the image showing theater outcomes by launch date suggests that kickstarter fundraising campaigns launched in May are the most likely to be successful plus the summer months are the next best to time launch. December appears to be the least likely month to be successful so don't expect to start your fundraising campaign in December or in March.  

Looking at the succcess of fundraising campaigns based on the fundraising goals set, the data shows that very small campaigns such as those raising less than $1,000 appear to second most likely to succeed. Raising $1,000  to just under $5,000 dollars are most likely to succeed overall. For some reason, campaigns raising from $15,000 to about $33,000 and from $44,000 or so and above appear fail more than succeed. 

It would be good to find out more about the reasons for failure or success, and know how close to the goal the failing campaigns were. That might help Louise determine when to launch and what goals to set. 


