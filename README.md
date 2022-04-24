# An Analysis of Kickstarter Campaigns

## Overview of Project:
Analyzation of a dataset of 4,000 crowdfunding projects to identify trends, specifically looking at how launch dates and funding goals impact the success rates of a fundraising campaign. The materials contained here provide a visualization of the data examined as well as an analysis of what this data tells us. The goal of the project is to provide methods for the client to easily interpret the data and apply it to her current goals and make decisions for her own campaign. 

## Analysis & Challenges
### Analysis

#### First 
I determined the outcomes of theater projects by launch date to determine the times in which those projects were best received historically. I did this by creating a [pivot chart](https://github.com/mlostritto/kickstarter-analysis/blob/ef8a4c7297991b0244d64e7b1e717c0863b39594/Kickstarter_Challenge.zip) using the initial Kickstarter data set that I was given. Within that chart, I used Parent Category and Years as the Filters, Outcomes in the Columns, Data Created Conversion in the Rows, and Outcomes again in the Values. I sorted the Parent Category by “theater” and arranged the column labels in descending order to show “successful,” “failed,” and “canceled” in that order. To provide better visualization, I added a Line with Markers chart. 
![Line with Markers Chart](https://github.com/mlostritto/kickstarter-analysis/blob/2490f0debe21057169f9b427c3a5fc5d531faa98/Theater_Outcomes_vs_Launch.png)
#### Second 
I determined the number of successful, failed, and cancelled campaigns for the subcategory of “plays” based on if the campaigns met their goals. For better visualization, I created a [new sheet](https://github.com/mlostritto/kickstarter-analysis/blob/ef8a4c7297991b0244d64e7b1e717c0863b39594/Kickstarter_Challenge.zip) and arranged the goals in subsets of 5000, starting the goals of less than 1000 and then increasing in 5000 increments to 50,000 or more as the final subset. These were arranged as the rows in the spreadsheet and the columns were arranged as number of campaigns that were successful, failed, and canceled, then the total sum of those projects, followed by the percentages of the successful, failed, and cancelled campaigns. For additional visualization, I created a line chart that showed the percentage of successful, failed, and cancelled campaigns across the level of the goals each campaign was attempting to reach.
![Line Chart](https://github.com/mlostritto/kickstarter-analysis/blob/2490f0debe21057169f9b427c3a5fc5d531faa98/Outcomes_vs_Goals.png)

### Challenges

#### The First Challenge
uilding the pivot table for the determination of the outcomes of the theater projects by launch dates. When I first put the Data Created Conversion label into the Rows section, it loaded a large amount of data under the label (blank). This meant that my numbers were no where near accurate. The first thing I discovered when troubleshooting this problem, was that there was a flaw in my original Kickstarter data. In the Data Created Conversion column there were many blank cells. When I had originally input the conversion formula, I input it in the first cell and then double clicked the bottom right corner to auto apply the formula to the rest of the cells. An error occurred in this process and many cells were left blank. To rectify this, I applied the original formula in the first and second cell and then auto applied the formula to the rest of the cells. This fixed the issues, and every cell was then filled with the correct data. 

#### The Second Challenge
This came when I attempted to create a new pivot chart with the new data. The (blank) label was still there even though none of the cells in the data set I was pulling from were blank. After some trial-and-error, I finally thought to go into the PivotTable Analyze tab and click the Refresh button in the data section. This updated the data in the pivot table based on the corrections I had made previously and removed the (blank) label, leaving me with all the correct data in the table. 

#### The Third Challenge 
Came during the second phase of the analysis when I was determining the outcomes based on goals and needed to use the COUNTIFS function. This was the first time I had used this function and so I did not have the necessary knowledge to immediately implement it. Through a series of trial-and-error experimentation, though, it did not take me long to figure out the proper functions and apply them to the entire sheet. After that, creating a line chart to provide better visualization was relatively easy. 

## Results

### Theater Outcomes by Launch Date Conclusions

#### First Conclusion
This one jumps from this data immediately at first glance. May and June both have 100 or more successful campaigns, which is 10-20 more successes than the next highest month. This could potentially indicate that May and June are the best months to plan a theater production, which is useful information for my client. We also see heightened success rates in April, July, and August, so even the timeframes around May and June are still more likely to aid in success. 

#### Second Conclusion 
Can be draw from the data shown in the line chart. The line for the failed campaigns stays relatively steady over time. This can potentially indicate that while the time of the year may play into the success of a campaign, it does not have as much impact into whether a campaign will fail. Another interpretation of this data is that because the failed rates stay the same across time, the spike in successes that we see in May and June may be attributed to another factor that is not show in this data set and therefore simply be a correlation without necessarily any causation involved. 

### Outcomes Based on Goals Conclusions
As with the theater outcomes, here there is one easily read message, and that is that the higher a campaigns goals, the less likely it is to succeed. The lowest goals produced the highest percent chance of success, this is clearly shown by the Less Than 1000 subset of goals having a 76% chance of success and that chance gradually decreases as the goals increase. The exception to this is the goals 35,000 – 44,999, which have a success percentage of 67 each. However, there were only 9 total campaigns within that subset, out of over 1,000 total campaigns, so these can be classified as outliers that are not numerically significant. 
Another conclusion can be draw from the significant drop in the success rate after the 1,000 – 4,999 subset, where it goes from 73% success to 55% success. This would indicate that having a campaign goal of less than 5,000 offers the greatest opportunity for success. 

## Limitations of the Dataset
### The main limitation
Is simply the amount of data at hand. We only have the number of projects within this category and whether they succeeded or not, plus the months in which we see the most successes. This leaves out a bevy of information about why these campaigns succeeded or not and is drawing conclusions purely on the amount of money being requested and the time of year it is requested. These are certainly large factors, but they are not the only factors. Within the overarching Kickstarter data provided, we also have access to the countries these campaigns are based in, the number of backers involved, a wide variety of categories for the projects, and how much was pledged in comparison to the goals of the campaigns. All of that information can be used in a variety of ways to add context into the data analyzed in this project. With it, we have the potential to see which countries tended to have the most success in which categories, which could tell the client where her particular category of campaign could see the most success. We could see which campaigns received a large amount more pledges than their goals, which could indicate which types of campaigns have a higher demand. This is also simply what we could look at with the current data at hand. If we pulled data from other fundraising applications beyond Kickstarter, it could provide a lot more helpful information. 

### Another limitation 
Is that everything that has been discussed so far is quantitative data. There is no information on the qualitative elements that may have contributed to the success or failure of campaigns. Some campaigns could have had famous individuals attached to them which aided in the marketing of the project and increased the number of pledged. Even without that, the level of marketing and its success would have a significant impact regardless because if no one knows about a campaign, of course it won’t reach its goals. The number of hours that each project team put into making it work could also have a significant impact. There are many factors that go into a successful fundraising campaign and the base quantitative data that I had to work with here is only one part of it. 

## Other Table and/or Graph Potentials
For greater understand of the Outcomes Based on Goals section, a bar chart could have been quite helpful with visualization. It would have made the disparity between the goals up to 5,000 versus the higher goals much clearer than the line chart did. 
A clustered column or bar chart could have also been useful for the Theater Outcomes by Launch Date section. It would achieve approximately the same outcome as the line chart, however the slight alteration in visual presentation could potentially help the client more, or at least help her to spot different patterns. 
