# Twitter Sentiment Analysis
## Introduction
This is a simple sentiment analysis code written in python to get the comparsion of sentiment of tweets for individual twitter handles in the form of plots, wordclouds and piecharts and get to know how the sentiment is affected by coronavirus.
Also, I have tried to make the code as user friendly as possible, later explained. The plots for sentiment_final.py includes:
1. Comparison of Average of sentiment/polarity per day 
2. Comparison of Sum of all sentiment/polarity per day
3. Comparison of Polarity of tweets per day 
4. Number of tweets per day
5. India's Daily Number of Deaths due to coronavirus vs Average of polarity of all input twitter handles.
6. India's Daily Number of Deaths due to coronavirus vs Polarity per day of all input twitter handles.


## Requirments
1. Twitter Api Keys and Tokens.
2. Python 3.7
3. textblob
4. numpy
5. tweepy
6. nltk
7. Internet Connection
## User Friendly Code Inputs
1. Analysis between any two Dates viz start date and end date.
2. Analysis of any number of users eg: 3,5,7 etc 
3. Individual Plots with comparison plots(mentioned above)
4. Having Plots with state daily cases and deaths. eg: Arvind Kejriwal and delhi corona cases.
5. Have plots with different shades on time axis as descriptive of different phases of an analysis.
## Getting Started 
1. Obtain Twitter Api key and tokens from twitter developer site. https://developer.twitter.com/en#/
2. Input the codes in method DownLoadData as:
        consumer_key = "XXX"
        consumer_secret = "XXX"
        access_key= "XXX"
        access_secret = "XXX"
3. Then run the code on your terminal using python3 twitter_sentiment_analysis.py and download the required libraries that are required using pip install library 
4. Now assuming all the required files are downloaded the code will execute
Since, the code is user friendly so user has to put in few values to start the analysis: 
For example, I want the analysis between Narendra Modi and Rahul Gandhi between any two dates. For instance, let the dates be 1/5/20 to 30/6/20 and I want to translate Hindi Tweets to English, have Individual Plots with comparsion plots(mentioned above). Lastly want to plot with sentiment of Rahul Gandhi with number of cases in Delhi and Narendra Modi with number of cases in Gujarat.
Also, I would like to analyse how tweet sentiment changes with different phases (lets assume 6), let the phases be 1/5/20 to 10/5/20, 10/5/20 to 20/5/20, 20/5/20 to 30/5/20, 30/6/20 -10/6/20, 10/6/20 to 20/6/20 and 20/6/20 to 30/6/20.

## Terminal Input Shown for Guidance 
The bold text must be the input given by the user and you need to enter twitter ids of people you want to analyse <br />
(base) PREETs-MacBook-Air:Desktop preetmalviya$ python3 twitter_sentiment_analysis.py <br />
Enter Start Date After 15/3/20: <br />
Type Date dd/mm/yy: **1/5/20** <br />
Start Date  2020-05-01 00:00:00 <br />
Enter End Date Before 1/7/20: <br />
Type Date dd/mm/yy: **30/6/20** <br />
Enter the number of users you want to analyse : <br />
**2** <br />
Enter Twitter Ids of user  1 <br />
**RahulGandhi** <br />
Enter Twitter Ids of user  2 <br />
**narendramodi** <br />
['RahulGandhi', 'narendramodi'] <br />
Do you want to translate tweets to English (True/False): **True** <br />
Do you want to compare individual accounts with corona cases (True/False): **True** <br />
Do you want to compare state wise data(True/False): **True** <br />
Format for state name: andhra pradesh as Andhra Pradesh and delhi as Delhi <br />
Enter State for RahulGandhi <br />
**Delhi** <br />
Enter State for narendramodi <br />
**Gujarat** <br />
['Delhi', 'Gujarat'] <br />
Number of periods you want to highlight :**6** <br />
Enter dates between 01/05/20 and 30/06/20 <br />
Enter date number1 after 01/05/20 <br />
Type Date dd/mm/yy: **10/5/20** <br />
Enter date number2 after 10/05/20 <br />
Type Date dd/mm/yy: **20/5/20** <br />
Enter date number3 after 20/05/20 <br />
Type Date dd/mm/yy: **30/5/20** <br />
Enter date number4 after 30/05/20 <br />
Type Date dd/mm/yy: **10/6/20** <br />
Enter date number5 after 10/06/20 <br />
Type Date dd/mm/yy: **20/6/20** <br />
Enter date number6 after 20/06/20 <br />
Type Date dd/mm/yy: **30/6/20** <br />

Files like state.csv, nation_level_daily.csv should be kept in the same directory as python file as from these files data is obtained to plot the graphs.
Source for state.csv https://www.kaggle.com/imdevskp/covid19-corona-virus-india-dataset?select=state_level_daily.csv
Source for nation_level_daily.csv https://www.kaggle.com/imdevskp/covid19-corona-virus-india-dataset?select=nation_level_daily.csv
If someone wants to have a look at the plots they can usingt the drive link:
https://drive.google.com/drive/folders/1bSGFvIY_BwebHcwL-0zBz9UG7ROVsGcm?usp=sharing

## Output 
RahulGandhi <br />
Total number of Tweets including retweet without text= 122 <br />
Total number of retweets= 1503222 <br />
Number of English Tweets = 74 <br />
Number of Hindi Tweets = 40 <br />
Number of Tamil Tweets = 0 <br />
Number of Gujrati Tweets = 0 <br />
Number of Marathi Tweets =0 <br />
retweet of text tweets= 1412970 <br />
average retweest of text tweets=12394.473684210527 <br />
total_negative= 29 <br />
total_positive= 55 <br />
neutral=29 <br />
How people are reacting on RahulGandhi by analyzing 114 tweets. <br />
General Report: <br />
Weakly Positive <br />
Detailed Report:  <br />
9.65% people thought it was positive <br />
32.46% people thought it was weakly positive <br />
6.14% people thought it was strongly positive <br />
6.14% people thought it was negative <br />
14.91% people thought it was weakly negative <br />
4.39% people thought it was strongly negative <br />
25.44% people thought it was neutral <br />
48.25% people thought it was overall positive <br />
25.44% people thought it was overall negative <br />
 <br />
narendramodi <br />
Total number of Tweets including retweet without text= 309 <br />
Total number of retweets= 2100242 <br />
Number of English Tweets = 209 <br />
Number of Hindi Tweets = 53 <br />
Number of Tamil Tweets = 1<br />
Number of Gujrati Tweets = 4<br />
Number of Marathi Tweets =2<br />
retweet of text tweets= 1919508 <br />
average retweest of text tweets=7135.717472118959 <br />
total_negative= 35 <br />
total_positive= 162 <br />
neutral=72 <br />
How people are reacting on narendramodi by analyzing 269 tweets. <br />
General Report: <br />
Weakly Positive <br />
Detailed Report:  <br />
21.56% people thought it was positive <br />
31.97% people thought it was weakly positive <br />
6.69% people thought it was strongly positive <br />
2.60% people thought it was negative <br />
10.04% people thought it was weakly negative <br />
0.37% people thought it was strongly negative <br />
26.77% people thought it was neutral <br />
60.22% people thought it was overall positive <br />
13.01% people thought it was overall negative <br />
Number of Total Words for RahulGandhi 1774 <br />
Number of Total Words for narendramodi 4940 <br />

## Functions Explained 
Since I like working in a single file, all the code is present in a single file viz sentiment_final.py. Hence, the following is the explanation of different methods used if anyone wants to modify them.

