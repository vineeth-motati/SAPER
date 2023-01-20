# SAPER
Sentiment analysis, also known as opinion mining, is a type of natural language processing (NLP) that involves evaluating the sentiment or emotion behind a piece of text. In this paper, the authors apply sentiment analysis to public opinions of candidates on Twitter.

## Process 

1. In order to use the Twitter API, you must have a developer account and create a new app to get your API keys(app_key, app_secret, oauth_token, oauth_token_secret).
2. Once you have your API keys, you can use the Twython library to connect to the Twitter API and search for tweets using a specific keyword or hashtag(for example `JSP`,`TDP`,`YSRCP`) through `t.search(q=q,count=200)`.
3. The returned tweets are then preprocessed and cleaned to remove unnecessary information and special characters.
4. The TextBlob library is then used to perform sentiment analysis on the tweets using `analysis = TextBlob(tweet)` and `.sentiment.polarity`.
5. Based on the polarity of the sentiment, the tweets are classified as positive, negative or neutral.
6. The script returns a Dataframe containing the tweets and their corresponding sentiment scores.
7. The script also returns the percentage of tweets which are positive, negative and neutral.

## Note
- Some additional preprocessing and data cleaning can be done before running the analysis on tweets.
- You can also use other libraries such as NLTK for preprocessing.
- The analysis could be more in-depth by adding more features and columns to the dataframe.

In conclusion, we have presented a method for conducting sentiment analysis on public opinions of candidates on Twitter. By collecting and analyzing tweets related to the candidates, the authors were able to determine the sentiment, polarity, and subjectivity of the tweets, and compare the sentiment among the candidates. The word cloud generated from the tweets also provided valuable insights into the topics of most concern to the public. Overall, this analysis can be a valuable tool for understanding the opinions and feelings of the public towards a particular topic or individual.