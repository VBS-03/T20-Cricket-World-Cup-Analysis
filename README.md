# T20 World Cup Data Analysis

### Dashboard Link :

## Problem Statement


This dashboard facilitates the identification of the top 11 players worldwide, enabling the formation of a team with a 90% probability of winning matches.The team selected based on the analysis is expected to achieve an average score of at least 180 runs and possess the capability to defend an average of 150 runs.
Players were classified into specific roles including openers, middle order/anchors, finishers, all-rounders, and specialist fast bowlers based on predetermined criteria tailored to each role. These criteria played a crucial role in their selection as part of the top 11 players.

Finally, the analysis and dashboard will be utilized by the Subject Matter Expert (SME) to select players according to their specified conditions.

### Steps followed 

- Step 1 : Loaded the datasets that were initially in the JSON format into the Jupyter Notebook. We have 4 raw JSON files.
        
        -[t20_wc_player_info.json](https://github.com/VBS-03/Power_Bi_Projects/files/14987945/t20_wc_player_info.json)
        -[t20_wc_match_results.json](https://github.com/VBS-03/Power_Bi_Projects/files/14987990/t20_wc_match_results.json)
        -[t20_wc_bowling_summary.json](https://github.com/VBS-03/Power_Bi_Projects/files/14988001/t20_wc_bowling_summary.json)
        -[t20_wc_batting_summary.json](https://github.com/VBS-03/Power_Bi_Projects/files/14988011/t20_wc_batting_summary.json)

- Step 2 : Converted the nested dictionary present in the dataset into a flat list.
- Step 3 : Assigned the data to a 'Dataframe' using pandas.

![1](https://github.com/VBS-03/Power_Bi_Projects/assets/162421729/48225e67-8ddb-49ac-b883-5d5316acf4a7)

- Step 4 : We observed that the 'dismissal' column is not giving us a clear understanding regarding whether the batsman is out/notout.Hence, we added a column to the above dataframe mentioning whether the batsmann is out/notout based on whether the dismissal column contains a value or not.

![snap 2](https://github.com/VBS-03/Power_Bi_Projects/assets/162421729/2311227c-6b8f-4096-81e1-a06756422ec6)

- Step 5 : Dropped the 'dismissal' column as it is not more required for our analysis. 
- Step 6 : We observed some unwanted characters in the "batsmanName" column. Hence, we replaced the unwanted character with blank.

![snap 3](https://github.com/VBS-03/Power_Bi_Projects/assets/162421729/15b31cb8-e5f2-4354-8230-fb58af9250c7)
- Step 7 : Going ahead, we realised that the 'batting summary' datset and 'match result' dataset has no common column between them through which we can perform the join operations on them to futher carry out our analysis. 
- Step 8 : We decided to create a common column 'match_id' in the 'batting summary' dataset using the match column in the same dataset.
- Step 9 : We created a dictionary using the 'team1','team2' and 'match_id' columns in the 'match_result' dataset and utilized the dictionary to map the 'match_id' to the 'match' column in the 'batting summary' dataset thereby creating a 'match_id' column in the 'batting summary' dataset as well.
![snap 4](https://github.com/VBS-03/Power_Bi_Projects/assets/162421729/c0835204-8b50-4729-8489-3cc3778e223c)

![snap 5](https://github.com/VBS-03/Power_Bi_Projects/assets/162421729/f904dbd2-6d4f-4020-a96d-8c067615117f)

![snap 6](https://github.com/VBS-03/Power_Bi_Projects/assets/162421729/92db4217-c509-4621-80e0-f9179b378116)

![snap 7](https://github.com/VBS-03/Power_Bi_Projects/assets/162421729/89f488e5-5345-402d-9978-c41c428f8a72)

- Step 10 : Being satisfied with the final dataset after performing cleaning and transformation on the dataset, we have created a csv file of it which we will use to load the data into the power bi. 
- Step 11 : Performed the similar kind of steps of loading, cleaning and transforming the dataset to get a well organised data that could help us with our analysis ahead. And converted all of them into the CSV format files.

        - [dim_match_summary.csv](https://github.com/VBS-03/Power_Bi_Projects/files/14988426/dim_match_summary.csv)
        - [dim_players_images.csv](https://github.com/VBS-03/Power_Bi_Projects/files/14988433/dim_players_images.csv)
        - [fact_batting_summary.csv](https://github.com/VBS-03/Power_Bi_Projects/files/14988436/fact_batting_summary.csv)
        - [fact_bowling_summary.csv](https://github.com/VBS-03/Power_Bi_Projects/files/14988442/fact_bowling_summary.csv)

- Step 12 : We loaded all the dataset present in the csv files into the Power Bi Desktop.

- Step 13 : Created all the DAX required to perform the analysis and dashboard creation based on the category wise parameters and the criteria corresponding to each of them.

## Category, Parameters and Criteria's mentioned below:

1. Openers:

![snap 8](https://github.com/VBS-03/Power_Bi_Projects/assets/162421729/4fe815dd-384c-4c24-9187-b7cdb2d805fb)

2. Anchors/Middle Order:

![snap 9](https://github.com/VBS-03/Power_Bi_Projects/assets/162421729/9e21ed12-b2f8-41fb-91fe-0b1da47a9f0b)

3. Finisher/Lower Order Anchor:

![snap 10](https://github.com/VBS-03/Power_Bi_Projects/assets/162421729/630539e6-cbb1-464e-995d-9aa58c4ae28e)

4. All-ROunders/ Lower Order:

![snap 11](https://github.com/VBS-03/Power_Bi_Projects/assets/162421729/c85982c8-50fe-4aa7-be07-5d0c597beb7d)

5. Specialist fast bowlers:

![snap 12](https://github.com/VBS-03/Power_Bi_Projects/assets/162421729/933c94a1-c667-4e09-8d5c-be92b3d88982)

- Step 14 : Used this criteria to design the report and which contains 'Player Analysis' and the "final 11" dashboard that could help the SME to select his 11 players.

- Step 15 : The dashboards created are totally interactive and the tooltips are also created which could help to get all the information about the players just by hovering over their name.

# Snapshot of Dashboard (Power BI DESKTOP)

![snap 13](https://github.com/VBS-03/Power_Bi_Projects/assets/162421729/49436aa0-c3e4-4b80-9e71-0d5b87f09098)

 
![snap 14](https://github.com/VBS-03/Power_Bi_Projects/assets/162421729/3e3cce86-17c1-41fc-a19d-9bbbce2990d9)

# Insights

This Interactive dashboard can be utilized to select the top 11 players over the globe, enabling the formation of a team with a 90% probability of winning matches.
