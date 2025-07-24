# NBA Most Valuable Player Analysis

## Objectives and Business Requirements

* Analyse NBA player data - regular box score data and advanced analytics to determine the Most Valuable Player of the Regular Season.

This is useful for advertisers who want to sponsor or use the likeness of the perceived best or most popular player in the league in their campaigns.

This is also useful for sportcasters and podcasters and other content creators.

This may also be found to be useful for those that play Fantasy League games where the analysis may help select players by looking at past performance in past seasons.

## Hypotheses:

Look at historical data

* Determine a model that indicates which player will be voted MVP. Be aware that there is something called "voter fatigue" where one player who has won the award multiple times may be overlooked for another player, even though they were deserving of that award. We will look at this and when this may have occurred. One famous non-MVP award is of the Rookie of the Year Award when Lebron James won it in his first year but Carmelo Anthony had the better statistics.

We will build a model that estimates MVP likelihood based on historical performance metrics. It starts with:

Key Inputs:

-PER (Player Efficiency Rating)
-WS (Win Shares)
-TS% (True Shooting Percentage)
-USG% (Usage Rate)
-BPM (Box Plus/Minus)

A simple weighted scoring formula where each stat has a coefficient based on historical MVP correlations. Later, we could explore regression or even decision trees.


## Future possibilites

* Real-time data during games and the season could be used with machine learning to determine a model for the current season using APIs with data from ESPN, NBA.com and Basketball Reference.

## Additional Comments

* There are many intangibles in a team sport that are not always shown in data and may not show the true value of a player, but it can help. There are other things to consider, such as which division or conference is "weaker" that season, the strength of schedule, points from the bench (substitutes/second string) and which games are won by a large or small margin.

# Datasets

Various data sets were used.
One was sourced from Co-pilot with team names, co-ordinates and manually adjusted to have data upto date in 2025.
nba-cities-coordinates-2025.csv

One was manually created to have the team names and URLs to team logos (nba-logo-urls-2025.csv)

2 data sets were downloaded from Kaggle:

a.
https://www.kaggle.com/datasets/dbtjdals/nba-mvp-candidates-1980-2022?select=master_table.csv

There are 2 files, one for partial data for 2022, and a larger file with data from 1980-2021, the file that was used: master_table.csv

b.
https://www.kaggle.com/datasets/thedevastator/historical-nba-finals-and-mvp-results/data?select=NBA+Finals+and+MVP.csv

File was renamed to lower case and spaces replaced with _ for usage:
nba_finals_and_mvp.csv

Credit: Tristan Malherbe ( https://data.world/datatouille ) as per usage instructions of the data set

# Analysis techniques used:

* Data extraction, cleaning and transformation in Jupyter Notebooks
* Visualisations in Jupyter Notebooks using matplotlib, seaborn and plotly
* Visualisation in Power BI: interactive dashboards and visual tools to analyse data per year.

Note: There are 7 Jupyter Notebook files:
01_objectives.ipynb
02_etl_a.ipynb
03_etl_b.ipynb
04_etl_c.ipynb
05_matplotlib.ipynb
06_mplip_seaborn.ipynb
07_plotly.ipynb

The first lists objectives, some of which are in this README file.
Files 02-04 are data extraction, cleaning and transformation
Files 05-07 are visualisations in matplotlib, seaborn and plotly.

The PowerBI file is in the PowerBI folder in /data/outputs/PowerBI
nba-visuals.pbix

# Ethical considerations:

Due to the public nature of professional sports, this data is freely and widely consumed and did not require anonymisation of player names. 

# Technologies used:
* VS Code
* Python
* Jupyter Notebook
* Power BI
* AI tools: Co-Pilot, Google Search with AI responses

## Development Roadmap
GitHub has been used for version control

# Data Analysis Libraries:
* Pandas- Purpose: Data loading, cleaning, and manipulation.
* NumPy- Purpose: Numerical operations and array handling.
* Matplotlib, Seaborn, Plotly- Purpose: Data visualisation to explore relationships between variables.
* PowerBI: Visualisations in PowerBI

## Project Contributors
GitHub user name:
* rmj9000

## Credits 
* Code Institute https://learn.codeinstitute.net/ and GitHub: https://github.com/Code-Institute-Solutions/da-README-template, https://github.com/Code-Institute-Org/data-analytics-template
* CoPilot for code correction, generation utilising various prompts

### Content and Media
* The data set is from https://www.kaggle.com/
* Instructions and project templates are from: 
Code Institute https://learn.codeinstitute.net/ 
and GitHub: 
https://github.com/Code-Institute-Solutions/da-README-template, 
https://github.com/Code-Institute-Org/data-analytics-template
* The icons in the footer were taken from [Font Awesome](https://fontawesome.com/)

## Acknowledgements
* The support and guidance received from tutors, coordinators and colleagues was very much appreciated. Thank you!
