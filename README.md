# Data Wrangling Practice - WeRateDogs

## Introduction
This notebook was used to practice data wrangling on the tweet archive of Twitter user @dog_rates, also known as WeRateDogs. WeRateDogs is a Twitter account that rates people's dogs with a humorous comment about the dog. 

## Python Libraries
- os
- requests
- json
- numpy
- pandas
- matplotlib.pyplot

## Data Wrangling Report

### Gather
WeRateDogs Twitter data was gathered using three different methods
General tweet data was gathered manually from a csv file
Dog breed predictions for each tweet data was gathered programmatically from a tsv file
Number of favorites and retweets per tweet was gathered through Twitter's API
Once gathered, these data were converted to pandas dataframes, where they were assessed for data quality and tidiness issues and cleaned.

### Assess
This data was assessed both visually and programmatically for data quality and tidiness issues. Data quality issues included:
- Tweet timestamp of object data type
- Dog stage values (doggo, floofer, pupper, and puppo) included as individual columns
- Erroneous rating and dog name values
- Null values expressed as objects
- Inconsistently formatted values
- Tidiness issues included:
- Variables unrelated to the project
- Related variables spread across more than one dataframe

### Clean
These data quality and tidiness issues were then addressed with programmatic cleaning methods and exported to csv files.

### EDA
These csv files were then used in a brief exploratory data analysis that attempted to answer the following three questions:
1. Does rating correlate with number of retweets or favorites?
2. Does the amount of text correlate with the rating, number of retweets, or number of favorites?
3. Does dog breed correlate with rating, number of retweets, or number of favorites?

### Conclusions
The exploratory data analysis showed: 
1. Weak correlations between rating and retweet count with a correlation coefficient of 0.21 and between rating and favorite count with a correlation coefficient of 0.28.
2. No correlations between text length and rating with a correlation coefficient of -0.10, text length and number of retweets with a correlation coefficient of 0.11, and text length and number of favorites with a correlation coefficient of 0.15.
3. The distributions of both retweet count grouped by dog breed and favorite count grouped by dog breed are both long-tailed, right-skewed distributions. The three dog breeds with the highest average number of retweets per post are the Miniature Schnauzer with 11,293, Tibetan Terrier with 10,786, and Irish Terrier with 8,245. The three dog breeds with the highest average number of favorites per post are the Tibetan Terrier with 50,631, Giant Schnauzer with 25,619, and the Yorkshire Terrier with 24,758.
