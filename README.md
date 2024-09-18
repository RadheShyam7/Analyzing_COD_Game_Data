# STAT380-FinalProject

### Authors:
- Aryan Chimnani
- Daniel Gao
- Radhe Shyam Vatluri

### Date:
May 1, 2024

---

## Overview

This repository contains the code and analysis for the final project of STAT 380, which investigates various research questions related to a dataset of online matches from a first-person shooter video game (Call of Duty). The project consists of several tasks that involve data cleaning, exploratory data analysis, and predictive modeling using machine learning techniques.

---

## Project Structure

- `CODGames_p1_380.csv`, `CODGames_p2_380.csv`, `CODGameModes.csv`, `CODMaps.csv`: Datasets used in the analysis.
- `FinalProject.Rmd`: RMarkdown file containing the code and detailed explanations for each task.

---

## Libraries Used
- `tidyverse`: For data wrangling and visualization.
- `readxl`: For reading Excel files.
- `RecordLinkage`: To compute string similarity.
- `e1071`, `caTools`, `caret`, `randomForest`, `FNN`: For machine learning algorithms and evaluation.

---

## Tasks Overview

### Task 1: Map Voting Analysis

This task examines which maps are most likely to win when presented as an option to players. The analysis includes cleaning the dataset for misspelled map names and calculating the probability that each map wins when it's an option.

**Steps:**
1. Cleaned the data to account for spelling errors using `jarowinkler` string similarity.
2. Calculated the winning probabilities for each map using regex and summarizing techniques.
3. Created a visualization using `ggplot2` to show the probability of each map winning the vote.

**Results:**
- Maps with the highest probability of winning the vote:
  1. Raid
  2. Crossroads Strike
  3. Nuketown '84
  4. Diesel
  5. Standoff

### Task 2: Generative AI Model Comparison

We compared the quality of a solution provided by a generative AI model with our own solution. The AI code produced was incorrect, and we analyzed both the AI-generated code and our own manually written code.

**Key Points:**
- AI-generated code misunderstood parts of the question, producing incorrect results.
- We used `jarowinkler` to address misspelled map names, while the AI did not handle this well.

### Task 3: Game Type vs. Total Experience

This task explores how different game types affect the total experience earned by players, controlling for their score.

**Steps:**
1. Cleaned the `GameType` data to remove inconsistencies (e.g., removing "HC - ").
2. Visualized the relationship between `Score`, `TotalXP`, and `GameType`.
3. Created a linear regression model to quantify the effect of `Score` and game type on `TotalXP`.

**Results:**
- The regression model showed that `Score` and certain game types (e.g., Hardpoint and Domination) significantly impacted `TotalXP`.

### Task 4: Predicting Match Outcome

In this task, we built three machine learning models to predict match outcomes (win or loss) based on individual player performance metrics such as eliminations, deaths, score, damage dealt, and total XP earned.

**Models Used:**
1. Random Forest
2. k-Nearest Neighbors (kNN)
3. Naive Bayes

**Results:**
- kNN achieved the highest accuracy at **68.94%**, outperforming both Random Forest and Naive Bayes.

---

## Conclusion

Through this project, we explored data cleaning, probability analysis, and machine learning models to answer questions about map voting behavior, player experience, and match outcomes in Call of Duty. The kNN model proved to be the most accurate in predicting match outcomes based on performance metrics.

---

## Instructions

To run this project:
1. Clone the repository.
2. Open the `FinalProject.Rmd` file.
3. Install the required libraries: `tidyverse`, `readxl`, `RecordLinkage`, `e1071`, `caTools`, `caret`, `randomForest`, `FNN`.
4. Knit the RMarkdown file to produce the analysis in HTML format.

---
