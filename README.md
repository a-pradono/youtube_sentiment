<p align="center">
  <img width="300" height="250" src="https://github.com/a-pradono/youtube_sentiment/blob/main/images/pac_header.jpg">
</p>
<p align="center">
  <em>Photo by <a href=https://wallpapercave.com/all-eyez-on-me-wallpapers>WallpaperCave</em>
</p>

## Table of Contents

- [I. Introduction](#i-introduction)
- [II. Data and Methodology](#ii-data-and-methodology)
- [III. Results](#iii-results)
- [IV. Conclusions](#iv-conclusions)

## I. Introduction
It is no doubt that Tupac Shakur was one of the most influential rappers of all time and I am a huge fan of him. He was a legend and was one of my favorite musicians. In 2017, there was a movie called All Eyez on Me that tells a story about the life of Tupac Shakur. I haven't seen this movie yet, but I remember vividly when the trailer came out on YouTube a couple of years ago, some of my friends told me that the trailer was lame and some others told me that it was worth watching. What about the opinion of the other people that already watched this trailer? Let's dive into it. In this project, sentiment analysis has been implemented on the YouTube video comments of the All Eyez on Me trailer. Sentiment analysis is a natural language processing technique used to interpret and classify emotions whether is positive, neutral, or negative in subjective data.

## II. Data and Methodology
The data of this project was conducted from [All Eyez on Me Trailer #1 (2017)](https://www.youtube.com/watch?v=njnwYSybwko&t=3s) YouTube video, posted by Movieclips Trailers. Furthermore, various comments from this video were scraped and stored into a data frame that consists of +2000 observations. 

<p align="center">
  <img width="300" height="100" src="https://github.com/a-pradono/youtube_sentiment/blob/main/images/workflow.jpg">
</p>

The workflow above illustrates how I performed sentiment analysis for this project. First of all, several parameters are needed to be set to scrape information from the video using YouTube data API. Second, the result from scraping data was stored into csv data format to perform data cleaning before further analysis. Finally, sentiment analysis using VADER has been identified to better understand the number of opinions from people through their comments regarding this trailer YouTube video.

## III. Results
Initially from scraping, this data consists of 2072 rows x 3 columns. However, we all know that users of YouTube came from around the world and perhaps not all of those comments resulted in the english language. Therefore, I tried to detect the language with only english language in the data frame which resulted in 1701 rows x 3 columns and is shown by this figure below.

<p align="center">
  <img width="400" height="200" src="https://github.com/a-pradono/youtube_sentiment/blob/main/images/figure-01.jpg">
</p>

Sometimes, data not always come perfectly. The figure below illustrates how I performed text cleaning using a regular expression to get rid of '\n' special character like in row number 361 for instance.

<p align="center">
  <img width="400" height="200" src="https://github.com/a-pradono/youtube_sentiment/blob/main/images/figure-02.jpg">
</p>

Since there are comments with and without likes, I would like to know how many comments in the YouTube video that get likes from other users. The figure below shows that most of the comments with likes only have 29% while the comments without likes have dominated the data frame by 71%.

<p align="center">
  <img width="250" height="250" src="https://github.com/a-pradono/youtube_sentiment/blob/main/images/figure-03.jpg">
</p>

Due to the sentiment metrics of the comment as shown in the figure below, it turned out that this trailer has a significant of positive comments and followed by neutral comments and negative comments. The range compound score of sentiment metrics is -1 that leads to more negative and 1 which leads to more positive with -0.05 to 0.05 as neutral.

<p align="center">
  <img width="250" height="300" src="https://github.com/a-pradono/youtube_sentiment/blob/main/images/figure-04.jpg">
</p>

Finally, the results of positive and negative words can be visualized using word cloud. The first figure is for the positive sentiments and the second figure is for the negative sentiments of the All Eyez on Me trailer YouTube video's comments as shown below.

<p align="center">
  <img width="400" height="200" src="https://github.com/a-pradono/youtube_sentiment/blob/main/images/figure-05.jpg">
<p align="center">
  Positive words
</p>

<p align="center">
  <img width="400" height="200" src="https://github.com/a-pradono/youtube_sentiment/blob/main/images/figure-06.jpg">
<p align="center">
  Negative words
</p>


## IV. Conclusions
The objective of this project was to classify people's opinions whether is positive, neutral, or negative based on YouTube video comments of the All Eyez on Me trailer. The conclusions made from this project are:
  * YouTube data API is convenient for scraping data, but you need to first register for google developers console to get your own key API. 
  * There are 29% of comments with likes and 71% of comments without likes in the data frame.
  * This trailer video has more positive comments followed by neutral comments and negative comments due to the sentiment metrics.
  * Overall, sentiment analysis using VADER is very encouraging to understand not only the basic context but the emphasis on capitalization and punctuation.
