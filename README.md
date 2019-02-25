## Table of Contents
1. [Installation](#installation)
2. [Introducing a Dataset](#dataset-introduction)
3. [Project Motivation](#project-motivation)
4. [Data Preparation](#data-preparation)
5. [File Descriptions](#files)
4. [Results](#results)

### Installation <a name="installation"></a>
For running this project, the most important library is Python version of Anaconda Distribution. It installs all necessary packages for analysis and building models. 
 
### Introducing a Dataset <a name="dataset-introduction"></a>
Data for analyzing trends in Boston's Airbnb is available for free in Kaggle.com and here. This dataset contains data on listings with a huge number of features, user's reviews and calendar info for Airbnb homes in Boston.

### Project Motivation <a name="project-motivation"></a>
I chose this project to understand the trends of Airbnb in Boston area and analysis is done through addressing the following questions.
1. How well can we predict a listing's price and what features correlate well with the pricing?
2. Where to invest in a property in Boston to get the maximum number of returns from Airbnb?
3. How well can we predict reviews and what aspects are correlated with the reviews?

### Data Preparation <a name="data-preparation"></a>
This dataset has 3,585 observations and 95 features. The target features for analysis are price, review_scores_rating. To proceed with the analysis, data wrangling should be done as this data set is really messy.

1. I had to clean up the values in several columns: the price column had a dollar sign ($) and comma (,) characters and was in object format. I removed these so the data can be translated into an integer.
2. The data types for other columns like the number of bedrooms, bathrooms, accommodates also required a change so they can be used in calculations.
3. Few columns such as neighbourhood_group_cleansed, jurisdiction_names, license, has_availability were dropped from the dataset as there were no recordings associated with them. These were all empty columns present in the data.
4. City column had a lot of duplicate entries with few case-sensitive entries, space addition issues, etc. All replicates were replaced with a single city code name and this cleaned data was put into a new column called city_cleansed in listings data. City column also had an unusual entry in some native language which was considered for dropping because there was only one entry as such and I was not losing so much data dropping it.

### File Descriptions <a name="files"></a>
There is a notebook available here to showcase work related to the above questions and wrangling process. There are 3 data files used to address the above qustions
1. reviews.csv - it has data related to listing's reviews.
2. calendar.csv - it contains listing's calendar and availability info
3. listings.csv - it anchors all data about listings.


## Results<a name="results"></a>
The main observations of the code are published [here](https://medium.com/@susmitha.gudapati/a-data-driven-story-of-airbnb-in-boston-7a27c5267d38).