# Election_Analysis

## Project Overview
This Election Audit Analysis was performed to help determine the winner of a local congressional election. Of the counties that participted and the candidates who were in the running, a popular vote winner needed to be determined as well as which county had the highest voter turnout.

#### Resources:
The election data was provided in an Excel spreadsheet titled election_results.csv. The election winner, along with additional information, was determined using Python 3.10.1 in Visual Studio Code 1.63.2. 

#### Deliverables:
The Colorado Board of Elections has asked for the following information to provide a comprehensive outcome of the election audit:

1. Find the total number of votes that were cast in the election.
2. Find all of the counties that participated in the election.
3. Calculate the total number of votes cast in each county, as well as the percentage of total votes that were cast in that county.
4. Determine which county had the largest voter turnout.
5. Find all of the candidates that received votes in the election.
6. Calculcate the total number of votes each candidate received, as well as the percentage of total votes they received.
7. Determine the winning candidate based on popular vote and provide their vote count and vote percentage.

## Results
The analysis of the election shows that:
- There were 369,711 votes cast in the election.
- There were 3 counties that participated in the election: 
1. Arapahoe
2. Denver
3. Jefferson
- The county results were as follows:
    - Arapahoe had 24,801 votes cast, which came out to 6.7% of the total votes.
    - Denver had 306,055 votes cast, which came out to 82.8% of the total votes.
    - Jefferson had 38,855 votes cast, which came out to 10.5% of the total votes.
    - From these results, it is clear that Denver had the largest voter turnout of all the counties.
- The candidates that received votes were: 
1. Charles Casper Stockham
2. Diana DeGette
3. Raymond Anthony Doane.
- The candidate results were as follows:
    - Charles Casper Stockham received 23.0% of the votes and 85,213 total votes.
    - Diana DeGette received 73.8% of the votes and 272,892 total votes.
    - Raymon Anthony Doane received 3.1% of the votes and 11,606 total votes.
- The winner of the election was:
    - Diana DeGette who receied 73.8% of the votes and 272,892 total votes.

#### Election Results Image

##### The image below shows the election results as seen in the VS Code Python text file:

![VS_Code_txt_image](https://user-images.githubusercontent.com/94764735/148705273-70c9f3d0-a76f-45a2-87f4-b0f90619f612.png)


## Challenge Summary
As was detailed above, the code in this election analysis provided the desired outcomes of this particular election. The current code is catered specifically to the election data that was provided; however, it can certainly be repurposed to work for other elections. With a few updates here and there, an election commission could use this code script for other election results that they are tasked with analyzing.

To begin, the script should be copied to a new visual studio code file. Once the script is in a new file, the first step would be to change the data that the script is referencing. As long as the new election results data is in a csv file and saved in the “Resources” folder, the ends of the third and fourth lines of the scrip could be changed at:

`(“Resources”, “election_results.csv”)` & ` (“analysis”, “election_analysis.txt”)`

And converted to fit a new election like so:

`(“Resources”, “new_election_results.csv”)` & ` (“analysis”, “new_election_analysis.txt”)`

Once the new election data file is referenced, the code can be changed to fit whatever is contained in that new file. If the columns were labeled a little differently, like say the “candidate name” and “county” columns were switched around, it would be wise to switch the names of the candidate variable and county variable so that it makes sense which column each variable is referencing.

Also, the code could be updated to analyze an additional column if this `new_election_results.csv` file had one. Say for example, there is an additional column in the new file that contains the candidate’s party affiliation. A new list and dictionary could be added to the script like so:

`party_affiliation = []`

and 

`party_votes = {}`

Then, the winning party affiliation would need to be initiated to start at a blank slate, and the party votes initiated to start at zero (as seen below):

‘winning_party = ""` 

and 

`party_vote_count = 0`


Once that is taken care of, new segments of code can be added to the script right below where the candidate and county code was written. The easiest way to add this new code would be to copy the code created for the candidate information and replace the lists, dictionaries, variables, etc. with the ones that were just created for the party affiliation. Although this example was for an additional “party affiliation” column, it could be used for almost any additional column that might be added on to the data set.

Lastly, even if the second csv file (`new_election_results.csv`) contianed data for the same election, this script can still be applied to output it's results into the same text file. For example, say there were an election where the commission needed to determine the municipal results as well. If that municipal data were in the `new_election_results.csv` file, the main step would be to make sure that the csv file is saved to the same “Resources” folder that the first csv file is in. As long as that is taken care of, that fourth line of code (that was shown how to update earlier) wouldn’t have to be updated. Leaving it the same would ensure that the results of this municipal election data are displayed in the same `election_analysis.txt` output, along with what is already in there.
