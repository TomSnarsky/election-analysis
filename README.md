# election-analysis

## Overview of Election Audit

The purpose of this election audit is to deliver the results of the election at the level of both candidate and county. It is our goal to be able to elucidate not only the candidates' respective vote totals and percentage share of the vote (along with, of course, the winning candidate by popular vote), but also the countywise voter turnout and which county had the largest turnout/percentage share of the vote as well. The audit will render these results both via the command line and in a text file entitled "election_analysis.txt" in a format that is readable and clearly understandable to "person in the street" and election commissioner alike.

## Election-Audit Results

In the following bulleted list we address each of the most crucial election outcomes, along with the snippets of code that found them from the data for us.

- **How many votes were cast in this congressional election?** A total of 369,711 votes were cast in this election. We tabulated this figure by using a for loop to look through the entirety of the .csv file holding all the ballot information, and augmenting a vote counter variable for each entry in the .csv file as follows:
<img width="515" alt="image" src="https://user-images.githubusercontent.com/99628051/158044715-ca05922c-67e9-4df8-89bb-215e3c2450c8.png">

- **Provide a breakdown of the number of votes and the percentage of total votes for each county in the precinct.** Three counties' votes were represented in this election: Jefferson (with 38,855 votes, representing 10.5% of the total turnout), Denver (with 306,055 votes, representing 82.8% of the total turnout), and Arapahoe (with 24,801 votes, representing 6.7% of the total turnout). In order to tabulate these figures, we used code very similar to how we calculated the total and relative percentage share of the vote for each of the candidates, populating a list and dictionary and using them to calculate the percentage against the total. To begin with, we get the county vote totals:
<img width="607" alt="image" src="https://user-images.githubusercontent.com/99628051/158044884-0c7453d2-8b1b-4ce2-a7a3-c0e7a28b2472.png">

Then we used the vote totals to calculate percentage share by county, as well as using tracking variables to hold the highest-turnout county, count, and percent:
<img width="683" alt="image" src="https://user-images.githubusercontent.com/99628051/158044910-4092e17c-d40d-4fd2-ac8c-acd5c974d24c.png">

- **Which county had the largest number of votes?** Denver county had the largest numer of votes with 306,055, representing 82.8% of the total vote. We tabulated this figure using the aforementioned tracking variables as we looped through the counties, and then we printed this result to the terminal and the .txt file.
<img width="737" alt="image" src="https://user-images.githubusercontent.com/99628051/158044968-05197d40-6eee-4ab2-91bb-b43a95610ba7.png">

- **Provide a breakdown of the number of votes and the percentage of the total votes each candidate received.** Three candidates' votes were represented in this election: Charles Casper Stockham (with 85,213 votes, representing 23.0% of the total votes cast), Diana DeGette (with 272,892 votes, representing 73.8% of the total votes cast), and Raymon Anthony Doane (with 11,606 votes, representing 3.1% of the total votes cast). In order to tabulate these figures, we used code very similar to how we calculated the total and relative percentage share of the vote for each of the counties, populating a list and dictionary and using them to calculate the percentage against the total. To begin with, we get the candidate vote totals:
- <img width="626" alt="image" src="https://user-images.githubusercontent.com/99628051/158045086-ae72cb0d-3519-47d9-9649-7ec4ec2f02ac.png">

Then we used the vote totals to calculate percentage share by candidate, as well as using tracking variables to hold the winning candidate, count, and percent:
<img width="640" alt="image" src="https://user-images.githubusercontent.com/99628051/158045135-d5e9165f-ae23-4a43-8e4c-5652917c2b88.png">

- **Which candidate won the election, what was their vote count, and what was their percentage of the total votes?** The winning candidate was Diana DeGette with 272,892 votes, representing 73.8% of the popular vote. We tabulated this figure using the aforementioned tracking variables as we looped through the counties, and then we printed this result to the terminal and the .txt file.
<img width="649" alt="image" src="https://user-images.githubusercontent.com/99628051/158045193-2c0d3044-2097-4858-b583-1af68e7839ae.png">

## Election-Audit Summary

In summary, this election audit script gives several key pieces of information for understanding the outcome of many standard elections. The script is also highly modular and can be adjusted to track other important election features. For example, if we were using this script to analyze a national election, it would be very possible to add "State" (in addition to "county") as a level of analysis for considering turnout. Furthermore, our calculation of percentage share of the vote could be enhanced or modified to suit other understandings of the idea; for example, if we had data on the total number of registered voters in each state for a national election, we could calculate voter turnout percentage for each state in terms of how many of that state's registered voters actually cast a ballot. This might be a more meaningful measure of voter turnout across which to compare states, since states can have highly variable total populations.
