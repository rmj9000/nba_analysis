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



1. Use this template to create your GitHub project repo. Click the **Use this template** button, then click **Create a new repository**.

1. Copy the URL of your repository to your clipboard.

1. In VS Code, select **File** -> **Open Folder**.

1. Select your `vscode-projects` folder, then click the **Select Folder** button on Windows, or the **Open** button on Mac.

1. From the top menu in VS Code, select **Terminal** > **New Terminal** to open the terminal.

1. In the terminal, type `git clone` followed by the URL of your GitHub repository. Then hit **Enter**. This command will download all the files in your GitHub repository into your vscode-projects folder.

1. In VS Code, select **File** > **Open Folder** again.

1. This time, navigate to and select the folder for the project you just downloaded. Then, click **Select Folder**.

1. A virtual environment is necessary when working with Python projects to ensure each project's dependencies are kept separate from each other. You need to create your virtual environment, also called a venv, and then ensure that it is activated any time you return to your workspace.
Click the gear icon in the lower left-hand corner of the screen to open the Manage menu and select **Command Palette** to open the VS Code command palette.

1. In the command palette, type: *create environment* and select **Python: Create Environment…**

1. Choose **Venv** from the dropdown list.

1. Choose the Python version you installed earlier. Currently, we recommend Python 3.12.8

1. **DO NOT** click the box next to `requirements.txt`, as you need to do more steps before you can install your dependencies. Click **OK**.

1. You will see a `.venv` folder appear in the file explorer pane to show that the virtual environment has been created.

1. **Important**: Note that the `.venv` folder is in the `.gitignore` file so that Git won't track it.

1. Return to the terminal by clicking on the TERMINAL tab, or click on the **Terminal** menu and choose **New Terminal** if no terminal is currently open.

1. In the terminal, use the command below to install your dependencies. This may take several minutes.

 ```console
 pip3 install -r requirements.txt
 ```

1. Open the `jupyter_notebooks` directory, and click on the notebook you want to open.

1. Click the **kernel** button and choose **Python Environments**.

Note that the kernel says `Python 3.12.8` as it inherits from the venv, so it will be Python-3.12.8 if that is what is installed on your PC. To confirm this, you can use the command below in a notebook code cell.

```console
! python --version
```

## Deployment Reminders

* Set the `.python-version` Python version to a [Heroku-22](https://devcenter.heroku.com/articles/python-support#supported-runtimes) stack currently supported version that closest matches what you used in this project.
* The project can be deployed to Heroku using the following steps.

1. Log in to Heroku and create an App
2. At the **Deploy** tab, select **GitHub** as the deployment method.
3. Select your repository name and click **Search**. Once it is found, click **Connect**.
4. Select the branch you want to deploy, then click **Deploy Branch**.
5. The deployment process should happen smoothly if all deployment files are fully functional. Click the button **Open App** at the top of the page to access your App.
6. If the slug size is too large, then add large files not required for the app to the `.slugignore` file.
