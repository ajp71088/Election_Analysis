# Election_Analysis

### Overview of Election Audit
Conducting an audit on a recent local congressional election on behalf of the Colorado Board of Elections. Tasks required to accomplish the audit:

1. Calculate the total number of votes cast.
2. Get a complete list of candidates who received votes.
3. Get a complete list of counties participating in the election.
4. Calculate the total number of votes each candidate received.
5. Calculate the total number of votes cast in each county.
6. Calculate the percentage of votes each candidate won.
7. Calculate the percentage of total votes each county cast.
8. Determine the winner of the election based on popular vote.
9. Determine the county with the largest voter turnout.

#### Election-Audit Results
* There were a total of 369,711 votes cast in the election
* Jefferson County cast 10.5% of the total votes (38,855)
* Denver County cast 82.8% of the total votes (306,055)
* Arapahoe County cast 6.7% of the total votes (24,801)
* Denver County has the largest number of votes
* Candidate Charles Casper Stockham received 23.0% of the total votes (85,213)
* Candidate Diana DeGette received 73.8% of the total votes (272,892)
* Candidate Raymon Anthony Doane received 3.1% of the total votes (11,606)
* The winning candidate was Diana DeGette, whose 272,892 votes accounted for 73.8% of the total votes cast

#### Election-Audit Summary
This audit script using Python code can be used with no adjustments for any election with a database that follows the same format, specifically with columns (left-to-right) of unique ballot IDs, county, and candidate. Ensuring that all elections under the care of the Colorado Board of Elections follow this format when producing their raw data will allow for audits that cut down on cost by the ability to reuse code.

##### Suggested Script Modification to Track Precinct Results
The script can also be modified to allow for more detailed analysis or to adjust to a different sort of ballot. For instance, if the raw data could also include the precinct that each ballot ID was cast in, the analysis could deliver that data to allow for the Board to know the turnout on a more micro level.

Presuming that the raw data output would place the precinct in a column after the county but before the candidate, this can be done through a few steps. First assign a precinct list variable and precinct votes dictionary that pulls from the correct row in the data source:

![image](https://user-images.githubusercontent.com/107162310/176215699-84c7019a-becb-4a96-9428-bfb38636d826.png)

Next assign variables to track the largest precinct voter turnout, similar to the county tracking:

![image](https://user-images.githubusercontent.com/107162310/176215845-6cabc851-ab23-4171-8fbb-9b4bf2904361.png)

The rest of the updates would follow suit, essentially repeating the exact code tracking counties or candidates but adjusting it for precincts. Here's a final example that includes some of the conditionals within the first for loop of the original code, now updated for precincts:

![image](https://user-images.githubusercontent.com/107162310/176217502-c6fa7098-d970-417c-bc37-1b84400c629b.png)

The remaining code would be simple enough to adjust to include precincts.

##### Suggested Script Modification to Track Candidate Results by County or Precinct
Currently, the audit delivers results on the total votes for each candidate. But it does not look at candidate results by county or precinct. 




