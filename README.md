# Communicate Data Findings
This repository contains the anaysis of the dataset from the Bay Wheels which is bike sharing organisation based in the California, US. 
This project is for the Data Analyst online course at the Udacity as my last project to complete the course. 

**Title**: Bay Wheels Bike Sharing System Usage Pattern 2019/2020, <br/>
**Data Range**: `September, 2019 to August, 2020`, <br/>
**Data Source**: Data is made available to us by the Bay Wheels on their [website](https://s3.amazonaws.com/baywheels-data/index.html), <br/>
**Data Format**: CSV formatted.

**Data Wrangling and Cleaning**: I tried to keep the data clean to the point that it contained only the columns that were necessary for my analysis. Some of them follows:
 ```
  - delete some of the columns which wont be required for the analysis
    such as:
     `start_station_latitude`, 
     `start_station_longitude`, 
     `end_station_latitude`, 
     `end_station_longitude`,
     `start_lat`,
     `start_lng`,
     `end_lat`,
     `end_lng`,
  - `started_at`: the column values are in str format should be datetime obj,
  - `ended_at`: the column values are in str format should be datetime obj,
  - duplicated_rows: remove the duplicated rows,
  - `started_at` and `start_time` two columns has the same value,
  - `ended_at` and `end_time` two columns has the same value,
  - create new columns which contains the `year`, `month` and `day` when the bike was hired.
  - columns `member_casual` and `user_type` represents the same value, merge the values and replace one of the values with the other, for example as seen `user_type` has `Subscriber` and `Customer` values and `member_casual` has values `casual` and `member` values. They are all same. Hence for our dataframe we will user `Subscriber` and `Customer` values.
  - `duration_sec`: column value is in seconds, will convert them in mins to have smaller values and rename the column from `duration_sec` to `duraion_mins`.
```

**Analysis**: There are version of the analysis that one could follow and are uploaded to this repo, 
1. `exploration.ipynb`: This is where the ground work of the Data Gathering, Data Assessing and Data Cleaning has been done and there is lot of rough work being done in terms of visualisations and has the observations defined. Not all the observations are meaningfull though, its more of a rough work. 
2. `slide_deck.ipynb`: This is clean notebook with the subset of the visualisations from the `exploration.ipynb` notebook, with clear questions and observations.
3. `slide_deck.slides.html`: This the navigable html page which contains all the headings, questions, answers and visualisation from the `slide_deck.ipynb` notebook. The notebook is converted using a javascript called `output_toggle.tpl`.
4. `output_toggle.tpl`: javascript to convert the notebook into the html slides. 


During the Analysis of the dataset, I wanted to look at visualisations and answers to the question what are the different users type and how is their ridership different in terms of the ride duration, how different in the way they access the bike, and preferred time of the day/month of year of their ridership. Also, while at it I also wanted to look at the impact of COVID-19 on the above visualisations and change in behaviour of both the users. 

**Summary**: Subscriber and Customer are the two different types of the user of the Bay Wheels and they differ in the way they access the bike, when they access and how they access the bike and for how long. The answer to all these questions are available in the `slide_deck.ipynb` which also visualises the impact of the COVID-19 on the behaviour of the users and impact on their ridership.
