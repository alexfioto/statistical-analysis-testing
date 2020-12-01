README.md

# 2017-2018 SAT/ACT Data Analysis


### Introduction
Using SAT/ACT data from 2017 and 2018, this project details and documents the fundamentals of data analysis utilizing the following libaries:
- **matplotlib**: data visualization
- **numpy**: scientific computing
- **pandas**: data importing, cleaning, and exploratory analysis
- **scipy**: statistical testing
- **seaborn**: data visualization

### Overview
The following topics are covered:

- Importing libraries and datasets
- Initial data inspection
- Data Cleaning
- Creating data dictionaries in markdown
- Exploratory data analysis
- Data visualization and interpretation using matplotlib and seaborn
- Conclusions and recommendations

## Problem Statement

There is a lot of data in the world. How can we organize, explore, understand, gather useful insights and make informed decisions from it? This project demonstrates a powerful and effective process to answer these questions utilizing python and some of its most powerful libraries.  

## Executive Summary

We will be analyzing ACT/SAT data from 2017 and 2018. 

First we import the necessary libraries: 
 - matplotlib: data visualization
 - numpy: scientific computing
 - pandas: data analysis
 - scipy: statistical testing
 - seaborn: data visualization
 
Next, we import, inspect and clean our data using pandas. We will make sure all datatypes are appropriate for analysis, correct any errors found by cross referencing the data source, rename columns for ease of use, drop any duplicate columns and merge our data.

Using pandas, we will explore and analyze our data looking for trends and patterns. We will examine participation rates and average total scores between the ACT and SAT.

Using matplotlib and seaborn, we will visualize our data using barplots, histograms, scatterplots, regplots, boxplots, and choropleth maps. Each visualization will be accompanied by a description and interpretation.

We will combine our analysis with outside research and dive deeper into a four states: Colorado, Florida, Illinois and Utah.

Lastly we will state our conclusions and recommendations based on our data analysis and outside research.

### Datasets

- [2017 SAT Scores](./data/sat_2017.csv)
- [2017 ACT Scores](./data/act_2017.csv)
- [2018 SAT Scores](./data/sat_2018.csv)
- [2018 ACT Scores](./data/act_2018.csv)

These data give average SAT and ACT scores by state, as well as participation rates for the classes of 2017 and 2018.

You can see the sources for the SAT data [here](https://blog.collegevine.com/here-are-the-average-sat-scores-by-state/) and [here](https://blog.prepscholar.com/average-sat-scores-by-state-most-recent), and the sources for the ACT data [here](https://blog.prepscholar.com/act-scores-by-state-averages-highs-and-lows) and [here](https://www.act.org/content/act/en/research/reports/act-publications/condition-of-college-and-career-readiness-2017.html). **Make sure you cross-reference your data with your data sources to eliminate any data collection or data entry issues.**


**This data has been compiled into CSV files which are also included in the *data* directory of this repo**


### Data Dictionaries

#### 2017 ACT Dataset
|Feature|Type|Dataset|Description|
|---|---|---|---|
|**state**|*string*|act_2017|USA state where data collected. The rest of the row's data is associated with the state labeled in this column.|
|**act_2017_participation**|*float*|act_2017|Percent of total students that took the test.|
|**act_2017_english**|*float*|act_2017|Average score on the english section. Scores range from 1 to 36.|
|**act_2017_math**|*float*|act_2017|Average score on the math section. Scores range from 1 to 36.|
|**act_2017_reading**|*float*|act_2017|Average score on the reading section. Scores range from 1 to 36.|
|**act_2017_science**|*float*|act_2017|Average score on the science section. Scores range from 1 to 36.|
|**act_2017_composite**|*float*|act_2017|Average composite score. Scores range from 1 to 36.|


#### 2017 SAT Dataset
|Feature|Type|Dataset|Description|
|---|---|---|---|
|**state**|*string*|sat_2017|State within the USA where data collected. The rest of the row's data is associated with the state labeled in this column.|
|**sat_2017_participation**|*float*|sat_2017|Percent of total students that took the test.|
|**sat_2017_readwrite**|*int*|sat_2017|Average score of the Evidence-Based Reading and Writing section of the SAT. Scores range from 200 to 800.|
|**sat_2017_math**|*int*|sat_2017|Average score of the Math section of the SAT. Scores range from 200 to 800.|
|**sat_2017_total**|*int*|sat_2017|Average total score of the SAT. Scores range from 400 to 1600.


#### 2018 ACT Dataset
|Feature|Type|Dataset|Description|
|---|---|---|---|
|**state**|*string*|act_2018|USA state where data collected. The rest of the row's data is associated with the state labeled in this column.|
|**act_2018_participation**|*float*|act_2018|Percent of total students that took the test.|
|**act_2018_composite**|*float*|act_2018|Average composite score. Scores range from 1 to 36.|


#### 2018 SAT Dataset
|Feature|Type|Dataset|Description|
|---|---|---|---|
|**state**|*string*|sat_2018|State within the USA where data collected. The rest of the row's data is associated with the state labeled in this column.|
|**sat_2018_participation**|*float*|sat_2018|Percent of total students that took the test.|
|**sat_2018_readwrite**|*int*|sat_2018|Average score of the Evidence-Based Reading and Writing section of the SAT. Scores range from 200 to 800.|
|**sat_2018_math**|*int*|sat_2018|Average score of the Math section of the SAT. Scores range from 200 to 800.|
|**sat_2018_total**|*int*|sat_2018|Average total score of the SAT. Scores range from 400 to 1600.

#### Final Dataset
|Feature|Type|Dataset|Description|
|---|---|---|---|
|**state**|*string*|act_2017|USA state where data collected. The rest of the row's data is associated with the state labeled in this column.|
|**act_2017_participation**|*float*|act_2017|Percent of total students that took the test.|
|**act_2017_english**|*float*|act_2017|Average score on the english section. Scores range from 1 to 36.|
|**act_2017_math**|*float*|act_2017|Average score on the math section. Scores range from 1 to 36.|
|**act_2017_reading**|*float*|act_2017|Average score on the reading section. Scores range from 1 to 36.|
|**act_2017_science**|*float*|act_2017|Average score on the science section. Scores range from 1 to 36.|
|**act_2017_composite**|*float*|act_2017|Average composite score. Scores range from 1 to 36.|
|**sat_2017_participation**|*float*|sat_2017|Percent of total students that took the test.|
|**sat_2017_readwrite**|*int*|sat_2017|Average score of the Evidence-Based Reading and Writing section of the SAT. Scores range from 200 to 800.|
|**sat_2017_math**|*int*|sat_2017|Average score of the Math section of the SAT. Scores range from 200 to 800.|
|**sat_2017_total**|*int*|sat_2017|Average total score of the SAT. Scores range from 400 to 1600.
|**act_2018_participation**|*float*|act_2018|Percent of total students that took the test.|
|**act_2018_composite**|*float*|act_2018|Average composite score. Scores range from 1 to 36.|
|**sat_2018_participation**|*float*|sat_2018|Percent of total students that took the test.|
|**sat_2018_readwrite**|*int*|sat_2018|Average score of the Evidence-Based Reading and Writing section of the SAT. Scores range from 200 to 800.|
|**sat_2018_math**|*int*|sat_2018|Average score of the Math section of the SAT. Scores range from 200 to 800.|
|**sat_2018_total**|*int*|sat_2018|Average total score of the SAT. Scores range from 400 to 1600.

