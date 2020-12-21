---
title: Methodology
layout: default
filename: methodology
--- 

# Methodology
### Construction of Dataset

The data was acquired in two parts. The first part consists of a dataset that tracked the 2017 and 2018 state legislative elections in districts all across the country, sourced from Dr. Carl Klarner’s master dataset of state legislative election returns.¹ The second part consists of data compiled by DailyKos which tracks the results of the 2016 Presidential election in each of the state legislative districts across the country.²

After piecing together many Google Sheets, I merged the data in R such that each row represented a state legislative election (2017 / 2018) as well as the Presidential election in that district (2016). 

I then removed districts with the following characteristics:
- Any state legislative election uncontested by either major party
- Any district that elected more than one representative³ 
- Special elections for unexpired terms 

Then I calculated the percentage of the total vote that each state legislative and Presidential candidate received. Third party voters were included in the total tallies, but districts with significant third party shares in legislative elections, or Presidential election (such as Utah or New Mexico 2016) were signified with another variable. 

Finally, I calculated the overperformance of state legislative candidates compared to the result of their Presidential standard bearer in the district. A positive value means they got a higher share of the vote than their Presidential candidate in the district, while a negative value means they got a lower share. 

All subsequent graphs / tables are drawn from these last two values, that of Democratic and Republican state legislative over/under performance. 

All together, the final dataset consists of 3,385 contested state legislative elections across 46 states. 

### Works Cited & Notes

¹ Klarner, Carl, 2018, "State Legislative Election Returns, 1967-2016: Restructured For Use", [https://doi.org/10.7910/DVN/DRSACA](https://doi.org/10.7910/DVN/DRSACA) , Harvard Dataverse, V1, UNF:6:hjXo+znmhZCoZ5P4cMo7Yw== [fileUNF]

[Dr. Klarner](https://www.klarnerpolitics.org/) provided me with the dataset updated to the years 2017 and 2018. As I am a student, he also graciously provided it to me for free. 

The dataset I used did not include Nebraska elections, as they are nonpartisan, or Louisiana elections, as they employ a unique jungle primary system. Thus, NE and LA are excluded from analysis. 

<br/><br/>
² DailyKos, “Daily Kos Elections Statewide by LD (public),” 2020.
[Link to Google Sheets](https://docs.google.com/spreadsheets/d/1YZRfFiCDBEYB7M18fDGLH8IrmyMQGdQKqpOu9lLvmdo/)

This data did not include Alabama, Mississippi, or Arkansas. I later found Arkansas from another source: [Dave's Redistricting 2020.](https://davesredistricting.org/) Thus, AL and MS are excluded from analysis.
<br/><br/>
³ This excluded districts where voters can vote for multiple candidates and multiple representatives are subsequently elected, such as in Vermont, Arizona, Maryland, or New Jersey. It also excludes floterial districts such as in New Hampshire. 

It does not exclude cases like West Virginia, where each State Senate district has two seats that alternate every two years between elections for four-year terms. 

It also does not exclude nested districts, that is, where a State Senate district is made up of two or more State House districts. If the House seats are elected independently as single members, they are included, but if they are elected by positions A & B within one district (as in Washington or Idaho), they are excluded. The Senate seats are included in both cases.

Thus, the final composition consisted of single-member districts (the vast majority), West Virginia’s staggered Senate districts, the State Senate districts of legislatures with nested districts, and the House districts of said nested legislatures if they were elected as single-member districts. 


