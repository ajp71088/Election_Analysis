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
  * ![image](https://user-images.githubusercontent.com/107162310/176481802-9baacdcc-e98e-4f9c-815d-5a7a3e480889.png)
* Jefferson County cast 10.5% of the total votes (38,855)
* Denver County cast 82.8% of the total votes (306,055)
* Arapahoe County cast 6.7% of the total votes (24,801)
  * ![image](https://user-images.githubusercontent.com/107162310/176482061-8018b6f4-deb9-49b9-b1b9-ff3e19414811.png)
* Denver County has the largest number of votes
  * ![image](https://user-images.githubusercontent.com/107162310/176482156-093f7a7b-14f6-495c-aa3c-caa9d23ba2ed.png)
* Candidate Charles Casper Stockham received 23.0% of the total votes (85,213)
* Candidate Diana DeGette received 73.8% of the total votes (272,892)
* Candidate Raymon Anthony Doane received 3.1% of the total votes (11,606)
  * ![image](https://user-images.githubusercontent.com/107162310/176482258-af09543e-52e1-4956-a690-01e86ee82ee9.png)
* The winning candidate was Diana DeGette, whose 272,892 votes accounted for 73.8% of the total votes cast
  * ![image](https://user-images.githubusercontent.com/107162310/176482312-ebe4e125-d3f1-4fbd-982a-7d2b6cc1078c.png)

#### Election-Audit Summary
This audit script using Python code can be used with no adjustments for any election with a database that follows the same format, specifically with columns (left-to-right) of unique ballot IDs, county, and candidate. Ensuring that all elections under the care of the Colorado Board of Elections follow this format when producing their raw data will allow for audits that cut down on cost by the ability to reuse code.

##### Suggested Script Modification to Track Precinct Results
The script can also be modified to allow for more detailed analysis or to adjust to a different sort of ballot. For instance, if the raw data could also include the precinct that each ballot ID was cast in, the analysis could deliver that data to allow for the Board to know the turnout on a more micro level.

##### Suggested Script Modification to Track Candidate Results by County or Precinct
Currently, the audit was asked to deliver the results on the total votes for each candidate and the total votes for each county. But it does not ask for the results of each candidate in each county. If requested, the candidate vote counts can be adjusted to also count and track candidate results by county (or a more micro level like precinct, presuming the raw data includes it) to allow for detailed analysis on how a given candidate performed by geographical location.
