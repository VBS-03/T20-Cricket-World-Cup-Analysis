# T20 World Cup Data Analysis

### Dashboard Link : https://app.powerbi.com/reportEmbed?reportId=0f54cdc9-bb53-424e-85e6-bc4ad89780a9&autoAuth=true&ctid=da6b8e5b-b111-4ee7-8826-33808fed6472

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

![1](https://github.com/VBS-03/T20-Cricket-World-Cup-Analysis/assets/162421729/cf218aff-b588-407d-8a07-ea7b903b7048)

- Step 4 : We observed that the 'dismissal' column is not giving us a clear understanding regarding whether the batsman is out/notout.Hence, we added a column to the above dataframe mentioning whether the batsmann is out/notout based on whether the dismissal column contains a value or not.

![snap 2](https://github.com/VBS-03/T20-Cricket-World-Cup-Analysis/assets/162421729/2e02d38b-8e05-49b1-bd5f-a299d5526dc1)

- Step 5 : Dropped the 'dismissal' column as it is not more required for our analysis. 
- Step 6 : We observed some unwanted characters in the "batsmanName" column. Hence, we replaced the unwanted character with blank.

![snap 3](https://github.com/VBS-03/T20-Cricket-World-Cup-Analysis/assets/162421729/a93b941d-f63c-445a-a7d2-8826cdf23c46)
- Step 7 : Going ahead, we realised that the 'batting summary' datset and 'match result' dataset has no common column between them through which we can perform the join operations on them to futher carry out our analysis. 
- Step 8 : We decided to create a common column 'match_id' in the 'batting summary' dataset using the match column in the same dataset.
- Step 9 : We created a dictionary using the 'team1','team2' and 'match_id' columns in the 'match_result' dataset and utilized the dictionary to map the 'match_id' to the 'match' column in the 'batting summary' dataset thereby creating a 'match_id' column in the 'batting summary' dataset as well.

![snap 4](https://github.com/VBS-03/T20-Cricket-World-Cup-Analysis/assets/162421729/3ba8643e-8b2e-4602-bb89-1c0a4fecf8a7)

![snap 5](https://github.com/VBS-03/T20-Cricket-World-Cup-Analysis/assets/162421729/cce45331-abc0-4544-b0ea-419e344c9af3)

![snap 6](https://github.com/VBS-03/T20-Cricket-World-Cup-Analysis/assets/162421729/00925d32-c6bf-4ed7-becd-3321e9d0978c)

![snap 7](https://github.com/VBS-03/T20-Cricket-World-Cup-Analysis/assets/162421729/22e2a959-4330-4e08-81e2-6f71bcb0b3b9)

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

![snap 8](https://github.com/VBS-03/T20-Cricket-World-Cup-Analysis/assets/162421729/06220db9-58d2-41a5-8f1f-8d1ca5280203)

2. Anchors/Middle Order:

![snap 9](https://github.com/VBS-03/T20-Cricket-World-Cup-Analysis/assets/162421729/2dc89aa0-466f-49fb-b961-e58219ac1ffb)

3. Finisher/Lower Order Anchor:

![snap 10](https://github.com/VBS-03/T20-Cricket-World-Cup-Analysis/assets/162421729/4c2a294e-a9f4-44e8-b990-5527bd2ee479)

4. All-ROunders/ Lower Order:

![snap 11](https://github.com/VBS-03/T20-Cricket-World-Cup-Analysis/assets/162421729/bffd32c3-97ce-4b78-9e51-5a095a5f6c36)

5. Specialist fast bowlers:

![snap 12](https://github.com/VBS-03/T20-Cricket-World-Cup-Analysis/assets/162421729/389cefaa-6923-4727-bc13-ec92c57b530e)

- Step 14 : Used this criteria to design the report and which contains 'Player Analysis' and the "final 11" dashboard that could help the SME to select his 11 players.

- Step 15 : The dashboards created are totally interactive and the tooltips are also created which could help to get all the information about the players just by hovering over their name.

# Snapshot of Dashboard (Power BI DESKTOP)

![snap 13](https://github.com/VBS-03/T20-Cricket-World-Cup-Analysis/assets/162421729/f78c579d-ee0a-40ef-b6a3-6184da0fed56)

 
![snap 14](https://github.com/VBS-03/T20-Cricket-World-Cup-Analysis/assets/162421729/db7e2e24-4358-4fbb-b38b-a90e0cb38026)

# Insights

This Interactive dashboard can be utilized to select the top 11 players over the globe, enabling the formation of a team with a 90% probability of winning matches.
