#Cricket Visual Analytics System#

This Python script provides a visual analytics system for analyzing the career statistics of Indian cricketers in Test, ODI, and T20 formats. The application fetches data from ESPNcricinfo, stores it in a MySQL database, and generates a variety of plots to visualize the performance of both batsmen and bowlers.

Features
Data Fetching: Fetches the latest career statistics for Indian cricketers from ESPNcricinfo.

Database Storage: Caches the fetched data in a local MySQL database to avoid redundant downloads.

Multiple Formats: Supports analysis for Test, One-Day International (ODI), and Twenty20 (T20) matches.

Role-Based Analysis: Provides separate statistical visualizations for batsmen and bowlers.

Interactive Menu: A command-line interface allows the user to select the match format and player role they wish to analyze.

Data Visualization: Generates a comprehensive set of plots for in-depth analysis, including:

For Batsmen:

Runs vs. Strike Rate

Runs vs. Batting Average

Comparison of Hundreds vs. Fifties

Percentage of Runs from Boundaries

Boxplot of Runs vs. Matches Played

Correlation Heatmap of Batting Stats

Trend of Ducks Across Players

For Bowlers:

Best Bowling Figures

Comparison of 4-Wicket and 5-Wicket Hauls

Economy Rate vs. Strike Rate

Wickets vs. Bowling Average

Boxplot of Wickets vs. Matches Played

Bar Graph of Innings vs. Wickets

Correlation Heatmap of Bowling Stats

Prerequisites
Before running the script, you need to have the following installed:

Python 3

pandas

SQLAlchemy

PyMySQL

Matplotlib

Seaborn

A running MySQL server instance.

You can install the required Python libraries using pip:

pip install pandas sqlalchemy pymysql matplotlib seaborn

Setup
Create a MySQL Database:

Start your MySQL server.

Create a new database named cricket. You can do this by running the following command in your MySQL client:

CREATE DATABASE cricket;

Configure the Database Connection:

Open the Python_IND.ipynb file.

Locate the following line in the main function:

db_engine = create_engine('mysql+pymysql://root:@localhost:3306/cricket')

Modify the connection string with your MySQL username, password, host, and port if they are different from the default (root user with no password on localhost:3306).

How to Run
Open a terminal or command prompt.

Navigate to the directory where you have saved the Python_IND.ipynb file.

Run the script using a Jupyter Notebook environment.

The script will welcome you and present a menu to choose the match format (Test, ODI, T20).

After selecting a format, you will be prompted to choose between analyzing 'Batsmen' or 'Bowlers'.

The script will then fetch the data (if not already in the database) and generate a series of plots for the selected category.

You can choose another category or format, or type 'quit' to exit the program.

Visualizations
The script generates the following plots to help you analyze player performance:

Batsmen Analysis
Runs vs. Strike Rate Scatter Plot: Visualizes the relationship between the total runs scored and the strike rate of each batsman.

Runs vs. Average Bubble Chart: Compares total runs and batting average, with the size of the bubble representing the number of matches played.

Hundreds vs. Fifties Stacked Bar Chart: Shows the number of centuries and half-centuries scored by each player.

Boundary Percentage Bar Plot: Displays the percentage of a batsman's total runs that were scored from fours and sixes.

Matches vs. Runs Boxplot: Provides a statistical summary of runs scored based on the number of matches played.

Batting Stats Heatmap: Shows the correlation between different batting metrics like Runs, Average, Strike Rate, etc.

Ducks Trend Line Plot: Illustrates the number of times each batsman has been dismissed for a duck.

Bowler Analysis
Best Bowling Figures Bar Plot: Highlights the best bowling performance (in terms of wickets taken) for each bowler in a single match.

Fourfers vs. Fifers Stacked Bar Chart: Compares the number of 4-wicket and 5-wicket hauls for each bowler.

Economy vs. Strike Rate Scatter Plot: Shows the relationship between a bowler's economy rate and their strike rate.

Wickets vs. Average Bubble Chart: Compares the total wickets taken and the bowling average, with bubble size indicating the number of matches played.

Matches vs. Wickets Boxplot: Gives a statistical overview of wickets taken based on the number of matches played.

Innings vs. Wickets Bar Graph: Visualizes the relationship between the number of innings bowled and the wickets taken.

Bowling Stats Heatmap: Displays the correlation between various bowling statistics like Wickets, Economy, Strike Rate, etc.
