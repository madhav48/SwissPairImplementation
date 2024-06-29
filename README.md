# Swiss Pairing Tournament Simulation

This repository simulates a coding tournament using a Swiss Pairing algorithm. The primary goal is to rank teams based on their performance in matches over multiple rounds, updating their ratings accordingly.

## Approach Overview

1. **Data Loading**:
   - Use pandas to load team data from a CSV file.
   
2. **Swiss Pairing Algorithm**:
   - **Initial Rating**: Provided in the input data.
   - **Outcomes**: Pair teams for matches.
   - **Adjustments**: Update team ratings based on match outcomes.
   - **Leaderboard**: Update and display the leaderboard.

## Key Components

- **Team Class**:
  - Represents a team, storing attributes such as name, rating, language, score, and history of opponents and match times.

- **SwissPairTournament Class**:
  - Manages the tournament, including pairing teams, simulating matches, and generating leaderboards.
  - **pair_teams**: Pairs teams ensuring similar ratings and constraints.
  - **match_teams**: Simulates matches, predicts winners, and updates ratings.
  - **get_leaderboard**: Sorts teams and breaks ties based on opponent ratings and match times.

## Simulation Process

1. **Initialization**:
   - Create team instances from the data and initialize a SwissPairTournament instance.
   
2. **Main Function (eval_result)**:
   - Repeatedly pairs teams, simulates matches, and updates the leaderboard for a set number of rounds.
   - Ensures that the number of byes does not exceed a specified limit.
   - Displays paired teams, winning teams, and updated leaderboards after each round.
   - Prints the final leaderboard at the end of the simulation.

