IPL data analysis


Data Analysis is a process of inspecting, cleansing, transforming and modelling data with the goal of discovering useful information, informing conclusions and supporting decision-making. Data Analysis has multiple facets and approaches, encompassing diverse techniques under a variety of names, while being used in different business, science, and social science domains.
The analytics team of INDIAN PREMIER LEAGE  association, BCCI association, or Anyone who speculate IPL matches with interest would love to know the answer of few questions that my data analysis on IPL DATASET would answer. My analysis contains– who is best player in IPL, Number of matches won by each team per year, Dependency of match on toss winner’s decision, Total number times a team has won the match from 2008 to 2019, and also talks about effect of toss decision on a match that is won by run or wickets.
IPL Dataset can be obtained here on Kaggle. It was published by ms. Rajmi. It contains following data fields: -
Id -  An unique number for each match.
Season – year in which a particular match was played.
 Date - Displays the date on which match was played.
Team1 – Displays the name of first team.
Team2 - Displays the name of second team.
 Toss-winner – Displays the name of team which has won the toss.
Toss-decision – Option choosed in between bat or field.
Result – Displays if the match was tie or not.
Dl-applied – Shows if the dl is applied in a match or not.
Winner – Displays the name of the team which has won.
Win by run – It displays the  number of runs by which the team has won.
Win by wicket – It displays the number of wickets by which the team has won.
Player of match – It shows the name of man of the match .
Venue – It displayed the name of the stadium at which match has been played.
City – It is the name of the city at which the match has been played.
Umpire1 – Name of 1st umpire.
Umpire2 – Name of 2nd umpire.
Umpire3 – Name of 3rd umpire.






Scope Of Analysis

Anyone who is speculating the IPL matches with interest would love to know the factors on which they could predict the winner of match. This project on Indian Premiere League Statistics of India provides the overall Statistics details of the matches of IPL and teams progress in various aspects from the year 2008 to 2017. The people who are speculating the matches wishes to answer the following objective:-
To find out best player
To find out number of matches won by each team per year.
To find out the dependency of toss winner’s decision for winning match.
To find out number of times a team has won the match from 2008-2019.
To find out effect of toss decision on win by run or wicket.

Aim of this project is to answer the above objectives in the form of visualization by creating a dashboard to convey the answers effectively and efficiently.


















ETL PROCESS

In computing, extract, transform, load (ETL) is a process in database usage to prepare data for analysis, especially in data warehousing. Data extraction involves extracting data from homogeneous or  purposes of querying and analysis; finally, data loading describes the insertion of data into the final target database such as an operational data store, a data mart, or a data warehouse. A properly designed ETL system extracts data from the source systems, enforces data quality and consistency standards, conforms data so that separate sources can be used together, and finally delivers data in a representation-ready format so that application developers can build applications and end users can make decisions. 

Precisely, ETL is defined as a process that extracts the data from different RDBMS source systems, then transforms the data (like applying calculations, concatenations, etc.) and finally loads the data into the Data Warehouse system. ETL stands for Extract, Transform and Load.

Before ETL, the dataset looked like this. This dataset is taken from Kaggle.




Through the process of ETL, we are going to clean the dataset and bring all the entities to their proper data format.

Step 1:  Remove null values from column city, player of match and umpire 1.

For this, we need to go to the top-right corner and click on (…) this icon. From the drop down list we need to select filters and then go to null values and select on keep only non-null values.





Step 2:  Removing an outliner from the ratings column.

The dataset had an entry with rating = 6. Now since rating can have values only from 0 to 5, this was clearly an outlier and a wrong value. The other entries of this row could not be trusted upon, so this particular entry was removed.



 

Step 3: Dropping unwanted column from the dataset.

Some of the columns in the dataset are of no use for the analysis purpose like, Umpire1, umpire2, and umpire3.



Step 4: Giving proper and appropriate column names.

The dataset does not have proper columns so our next step would be to giver proper column names to the columns wherever required.



Step 6: Creating a calculated field in excel

This was done after the cleaning process was already done in the tableau prep. From the Last Update column, a new column was created,  “toss winner = match winner”  which was done by using EXACT formula.





Using this function we compare the value in toss winner and winner to find if the toss winner is the match winner. If it is same then exact function returns true, else the function returns false.

Analysis Of Dataset


1.To find the best player of IPL.

The best player of IPL is one who is good overall. And the one who is good overall will become man of the match most of the time. So we create a pivot table with player of match as row label and count of player of match as a value column. 







For analysis, it is very clear that C.H GAYLE has became man of match for more number of time as it can be seen clearly from the graph. The count of man of match is highest for C.H GAYLE. Therefore 
C.H GAYLE  is the best player of IPL from 2008 to 2019. 


2.To show number of matches won by each team per year.

The data for different matches has been given in the dataset. To know if the number of win for a team is differing every year, and if so does this has any relation with the count of wins previous year. Is it increasing or decreasing with some common patter or it is just random. I have normally heard that CSK and MI are the top two teams of IPL, but how is this decided To find out so we create a pivot table with year as row label, winner as column label (it displays the name of teams) and count of winner as a value.





For analysis, the data clearly showed that there is no pattern in between the count of matches that each team win every season. But we achieved the answer for why are Mumbai Indians and Chennai super kings the top two teams of IPL. It is because they are most consistence in their performance and in almost every season the count of their wins is in top 3.


3.To show the dependency of toss winner’s decision for winning match.

I have seen people’s face turning happy when their team wins the toss and this made me curious about that how winning toss and the decision made would effect the match. Therefore I created a pivot table with toss decision as row label, toss winner= winner as column label and count of toss winner= winner as value.


 
From analysis, we saw that if the toss winner is match winner then toss decision “field” has 66% of chances to win. Therefore if a team is winning the toss and choose to field first then the chances of them winning is more. And if a team has not won the toss then the opponent team must choose to field. Then only the chance is more to win. But isn’t it contradicting , if we talk relatively then the winning chance after choosing field is more.


4.To find out the best team of IPL since 2008.
 
 To do so I have created the pivot table with winner as row label and count of win as value column.





From the analysis we can see that Mumbai Indians have won the maximum number of matches from 2008 to 2019.  Hence, best IPL team is Mumbai Indians.

 
5.To show effect of toss decision on win by runs and win by wickets.

Now here I had an question in my mind. And that was if the one who chooses to field would  win by more wickets or not? So I made an pivot table with toss decision as row label and win by wickets/runs value column.





From the analysis, it is very clear that the one who chooses to field wins by more wickets and also by more runs  which completely make sense.

Summary:

Thus, from IPL dataset we get to know that the best team is Mumbai Indians, overall winning chances increases if the toss winning team chooses to field first, best player is C.H GAYLE.
