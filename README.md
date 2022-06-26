# Election_Analysis

### Project Overview
A Colorado Board of Elections employee has given you the following tasks to complete the election audit of a recent local congressional election.

1. Calculate the total number of votes cast.
2. Get a complete list of candidates who received votes.
3. Calculate the total number of votes each candidate received.
4. Calculate the percentage of votes each candidate won.
5. Determine the winner of the election based on popular vote.

### Resources
- Data Source: election_results.csv
- Software: Python 3.7.6, Visual Studio Code 1.68.1

### Summary
The analysis of the election show that:
- There were 369,711 votes cast in the election.
- The candidates were:
  - Diana DeGette
  - Raymon Anthony Doane
  - Charles Casper Stockham
- The candidate results were:
  - Diana DeGette received 73.8% of the vote and 272,892 votes.
  - Raymon Anthony Doane received 3.1% of the vote and 11,606 votes.
  - Charles Casper Stockham received 23.0% of the vote and 85,213 votes.
- The winner of the election was:
  - Diana DeGette, who received 73.8% of the vote and 272,892 votes.

### Challenge Overview
To accomplish this analysis, the challenge was to write efficient Python code that would be able to perform all the calculations in as few steps as possible. This was done by assigning the requested calculations as variables initially equal to 0, and then using a conditional for loop:

```
># Add our dependencies.
>import csv
>import os
># Assign a variable to load a file from a path.
>file_to_load = os.path.join("Resources", "election_results.csv")
># Assign a variable to save the file to a path.
>file_to_save = os.path.join("analysis", "election_analysis.txt")
># Initialize a total vote counter.
>total_votes = 0
># Candidate options and candidate votes.
>candidate_options = []
>candidate_votes = {}
># Track the winning candidate, vote count, and percentage.
>winning_candidate = ""
>winning_count = 0
>winning_percentage = 0
># Open the election results and read the file.
>with open(file_to_load) as election_data:
    >file_reader = csv.reader(election_data)
    ># Read the header row.
    >headers = next(file_reader)
    ># Print each row in the CSV file.
    >for row in file_reader:
        ># Add to the total vote count.
        >total_votes += 1
        ># Get the candidate name from each row.
        >candidate_name = row[2]
        ># If the candidate does not match any existing candidate, add the
        ># the candidate list.
        >if candidate_name not in candidate_options:
            ># Add the candidate name to the candidate list.
            >candidate_options.append(candidate_name)
            ># And begin tracking that candidate's voter count.
            >candidate_votes[candidate_name] = 0
        ># Add a vote to that candidate's count.
        >candidate_votes[candidate_name] += 1
```

### Challenge Summary
Through this audit, I was able to learn some of the fundamental building blocks in Python for statistical analysis.
