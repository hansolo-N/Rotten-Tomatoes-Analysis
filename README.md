# 🍅🍅 Rotten-Tomatoes-Analysis

## Introduction 
In this analysis, we explore the relationship between audience and critic scores for movies listed on Rotten Tomatoes. Rotten Tomatoes provides a unique platform where both professional critics and general audiences can rate movies, offering a dual perspective on the perceived quality of films. Understanding the correlation—or lack thereof—between these two sets of scores can reveal interesting insights into how movies are received by different groups.

> This analysis leverages data visualizations to compare and contrast the scoring patterns of audiences and critics. By examining the distribution of scores and the overall correlation between the two, we aim to answer several key questions:

- Do critics and audiences generally agree on movie ratings?
- How consistent are critics in their scoring compared to the variability seen in audience scores?
- Are there significant discrepancies between what critics value in movies versus what resonates with audiences?

## Technologies
- Programming Language: Python
- Jupyter Notebook
- Microsoft Power Bi

## Data Overview

- Dataset
> - id - id of the movie (Integer)                    
> - title - title of the movie (string)                 
> - audienceScore - audience's score for the movie out of a 100 (Integer)        
> - tomatoMeter - critics score for the movie out of a 100  (Integer)           
> - rating - the maturity rating given for the movie e.g. PG-13 (string)              
> - ratingContents - the different ratings for the movie (string)         
> - releaseDateTheaters - date movie was released in cinemas  (string)   
> - releaseDateStreaming  - date movie was released for streaming (string) 
> - runtimeMinutes - the runtime of the movie in minutes (Integer)
> - genre - what genre(s) the movie belongs to (string)                   
> - originalLanguage - the original language of the movie (string)      
> - director - director(s) of the movie (string)               
> - writer - writer(s) of the movie (string)               
> - boxOffice - how much the movie made in the box office ($-dollars) (string)              
> - distributor - the primary distributor of the movie (string)              
> - soundMix - the mixer of the movie, if there was any (string) 

The dataset can be found on Kaggle : https://www.kaggle.com/datasets/andrezaza/clapper-massive-rotten-tomatoes-movies-and-reviews?select=rotten_tomatoes_movies.csv

## Data Cleaning and Preprocessing
  
- releaseDateTheaters and releaseDateStreaming Features were converted to appropriate datetime types
- created year columns for both streaming and cinema movies
- replaced null values in title Feature with string value indicating no title
- For the audienceScore Feature missing values were replaced with the mean audienceScore and then rounded
- For the TomatoMeter Feature missing values were replaced with the mean TomatoMeter and then rounded
- replaced empty rating values with the most common maturity rating (PG-13)
- replaced empty rating contents with string value indicating no rating contents
- for runtimeMinutes, replaced null values with mean runtimeMinutes
- these fields were replaced with string values for null values:
  - genre
  - originalLanguage
  - director
  - writer
  - releaseDateTheaters
  - releaseDateStreaming
  - BoxOffice (replaced with '0' string which helped to extract numeric values at a later stage)
 
## Exploratory Data Analysis (EDA)
- Distribution of Scores
- Correlation Analysis

## Key Findings
1. Correlation Between Audience and Critic Scores
- The analysis revealed a moderate positive correlation of 0.65 between audience and critic scores. This suggests that while there is some alignment between the two groups, they often have differing opinions on the quality of movies.
- Scatter Plot Analysis: The scatter plot shows a concentration of data points along the diagonal line, indicating instances where audience and critic scores align. However, there is a noticeable spread, particularly for movies with mid-range scores, where audience and critic ratings diverge significantly.

3. Distribution of Scores
- Audience Scores: The distribution of audience scores is slightly right-skewed, with a significant peak around the 60-70 range, suggesting that audiences tend to rate movies more leniently, with most movies receiving a positive rating.
- Critic Scores: In contrast, critic scores are more normally distributed with a sharper peak around 60. Critics appear to be more consistent in their evaluations, with fewer extreme high or low ratings compared to audiences.

4. Outliers and Discrepancies
- There are notable outliers where the audience score is significantly higher than the critic score. For example, popular blockbusters with heavy fan followings often receive higher audience ratings, despite receiving lukewarm responses from critics.
- Conversely, certain critically acclaimed films (often indie or art house) receive high critic scores but lower audience ratings, indicating a possible disconnect between critical acclaim and general viewer enjoyment.

## Conclusion
The analysis of Rotten Tomatoes movie ratings reveals both alignment and divergence between audience and critic evaluations. While there is a moderate positive correlation between the two sets of scores, the differences highlight varying preferences and expectations.

Critics tend to be more consistent and critical in their evaluations, favoring films with artistic merit and depth, often reflected in the higher scores for drama and art house genres. Audiences, on the other hand, show a preference for entertainment value, leading to higher ratings for action-packed blockbusters and mainstream films, regardless of critical reception.

These findings underscore the importance of considering both audience and critic perspectives when evaluating a movie’s overall reception. For movie studios, marketers, and filmmakers, understanding these dynamics can help tailor strategies to cater to different segments of the movie-watching public.

Future analyses could delve deeper into specific factors influencing these ratings, such as the impact of marketing, social media influence, or the role of genre and franchise popularity in shaping audience and critic perceptions.

## PowerBi
further visualizations were presented on PowerBi.
![PowerBi visuals.](RT_PowerBiVisuals.pdf)

