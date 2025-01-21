# setiment-analysis-of-Music

# Problem statement
Sentiment analysis has widely applied to examine the sentiment of customers implying their satisfaction with the service and product.However, one of limitation is it is difficult to underlying motivation of customers. For example, the sentiment analysis may determine customers'feeling toward sad song as negative sentiment. In fact, the sad feeling may imply they are touched by the song.  Therefore, sentiment analysis of comment is often supplemented with emotion analysis that offer underltying emotion behind customer costomers.  The project aims to investigate he phenomenon by collecting comments from 100 sad and 100 romance youtube music

# Project structure

# code_file

-Jupyter file involving web scrawling of 100 Rommance Song, data cleaning and transformation by pandas and regrex expression

-Jupyter file involving web scrawling of 5174 comments from 100 Rommance Song,calculation of emotion and sentiment scores by text2emotion and Vader model.

-Jupyter file involving web scrawling of 100 sad Song, data cleaning and transformation by pandas and regrex expression

-Jupyter file involving web scrawling of 5024 comments from 100 Sad Song,calculation of emotion and sentiment scores by text2emotion and Vader .



# Output_file

- csv file involving 5174 rows of comments from rommance song and column involving text and calculation of emotion and sentiment score

-csv file involving 100 rommance song and column involving statistic(viewcount,likecount,commentcount) and information(song_name,song_title) and calculation of average emotion and sentiment score of youtube video

- csv file involving 5024 rows of comments from sad song and column involving text and calculation of emotion and sentiment score

-csv file involving 100 rommance song and column involving statistic(viewcount,likecount,commentcount) and information(song_name,song_title) and calculation of average emotion and sentiment score of youtube video



# Powerbi file

- build the snowflake schema in the model view to create filter

- build the 3 dashboard demonstrate the relationship between emotion and sentiment score in both video and comment level 


