# An Analysis of Kickstarter Campaigns
This file contains an analysis of various Kickstarter campaigns which I analyzed to provide my client, Louise, insight to, that she may best determine how to structure and launch her own Kickstarter campaign to secure financing for a theater production (play) she hopes to bring to market.
# Module 1 Challenge: Kickstarter Data Analysis – Outcomes Based on Launch Date & Goal
## Overview of Project
The purpose of this project is to provide intelligence to my client, Louise, regarding how different Kickstarter campaigns fared (successful, failed, canceled), in relation to/based upon their respective launch dates and funding goals.  The client deliverable includes the data-work of my analysis to produce information, as well as visuals that highlight trends and important nuances of the dataset, from which intelligence can be gleaned.
## Analysis & Challenges
### Analysis Part I
I performed my analysis using Microsoft Excel, a spreadsheet which presents data in tabular (rows and columns) format.  Starting with the raw dataset, I created several additional columns for Parent and Subcategory, to categorize the data more easily.  I used formulas to make Date Created and Date Ended columns for each campaign, based on Unix timestamps in the raw dataset.  Finally, a “Years” column was created formulaically, referencing the “Date Created Conversion” column.
I then used a Pivot Table with key fields (Parent Category, Years, outcomes, and Date Created Conversion) to narrow my focus on the data to find answers to Louise’s question about campaign outcomes based on Launch Date.  I added a PivotChart to the same Workbook Sheet to readily display the data.  Insights can be gleaned from this visual in a matter of seconds, versus trying to make sense of the data-cut contained in the Pivot Table.  
![Outcomes_vs_Goals](path/to/Outcomes_vs_Goals.png)
### Analysis Part II
For the second part of the analysis—Outcomes Based on Goals, I used a series of formulas referencing the raw dataset to create a table of information, which I then presented graphically.  This table grouped the different campaigns into various cohorts (data buckets) based upon the size of the funding Goal in USD. There were 12 different Goal cohorts, so Louise can understand how different size-levels impacted overall campaign performance.  A series of CountIfs formulas with multiple criteria were used to pull in the number of Successful, Failed, and Canceled campaigns, respectively, from the raw data.  A total Projects column was added using a simple sum formula on these three campaign outcomes, by respective Goal cohort.  Finally, simple division was used to create three columns showing the percentages of campaign outcomes, again grouped by Goal cohort.  As in the Launch Date analysis, a graph was created to display the data, which Louise can refer to for quick understanding of how Goal amount affected campaign Outcome.
 https://github.com/deltaLyd/Completed-Kickstarter-Analysis-/blob/main/Resources/Theater_Outcomes_vs_Launch.png
## Challenges
The most challenging part of this analysis for me was writing the CountIfs formulas, as it is a statement that I do not use regularly, and I had to confirm that the information the formulas were returning was correct.  To address this challenge, I referred to online resources on use of the formula to understand the basic syntax and how it functions, and used simple Filters on the raw dataset to determine what the proper value should be for a given Goal cohort and Outcome column, and then confirmed the output with the formula-driven table I created, IE simple spot-checking of the values.
## Results
### Theater Outcomes by Launch Date
Based on my analysis of the dataset with respect to Launch Date, the best time to kick off a Kickstarter campaign for Theater is in the month of May.  This is the single most successful starting month for this Parent Category.  June, July, and August are the three next-best months, in that order.  As the data progressed from May through August, there is a notable decline in Successful outcomes, though the number of Failed campaigns is largely flat over this same time frame.  Analyzing the year as a whole, the “warm months” provide a greater chance of success than the “cold months” (assuming North-American seasons).  February mildly bucks this trend, as it performs on par with April, and only one success shy of August, while having fewer overall Failures.
### Theater Outcomes based on Goal
Turning to Outcomes based on Goals, the most important insights are that the lower the overall Goal size, the greater the chance of a successful Outcome.  While there is a greater number of Successful campaigns in the “1,000 to 4,999” cohort than the “Less than 1,000” cohort, the overall Percentage Successful level of the “Less than 1,000” cohort is the best at 75.8%, vs. 72.7% for the“1,000 to 4,999” cohort.  Therefore, I would recommend to Louise (and anyone else attempting to create a successful Theater Kickstarter) that she should target a relatively modest budget for the project, as likelihood of success drops off meaningfully (both in number and percentage terms) beyond the 4,999 level.
### Dataset Limitations
Some of the (possible) limitations to this dataset are that the dataset could be incomplete.  This dataset was provided to me and did not include an explanation of how the data was collected. While it seems fairly complete, there may have been errors in some of the responses that could skew the data (or at least individual line items) that are not identifiable without knowing the collection methods, be it survey-based or a cross-section of data pulled from Kickstarter’s database.  Another limitation of this dataset (which could be controlled for in the analysis of the data, though it was not explicitly requested for this analysis) is that the information is presented in multiple currencies, based upon the country in which the Kickstarted campaign took place.  While this is useful information to have broken out, without proper analysis, it muddies the overall results of simple analysis, as there is not a like-to-like comparison being done for outcome based on Goal, when the Goals are in different currencies.  Similarly, comparing the results of geographically dispersed countries by month is problematic, as there are different seasons in the same month, depending which country a person is in. 
### Additional Analysis Suggestions
Due to these limitations, there are several different tables and associated graphical displays that I would include in an analysis of this data, to provide deeper insight and a more accurate deliverable to my client.  I would take the Outcome by Goal data and apply a currency conversion (based on a determined spot rate) to state all campaigns in one currency, eliminating misplacement of campaigns into different cohorts because of Currency noise.  For the Outcome by Launch Date analysis, I would want to add an analysis of the different seasons of the countries, based on their geographical region/hemisphere, which is information not provided in the raw dataset.  Having this information would allow me to present data by month, by season, as winter and summer occur simultaneously in different hemispheres, and simply saying “campaigns perform better during the summer months” is not entirely accurate when the data/scope of the analysis is not restricted to a single like-geographical/seasonal region.

	
