# setiment-analysis-of-Music

# Problem statement
Sentiment analysis has widely applied to examine the sentiment of customers implying their satisfaction with the service and product.However, one of limitation is it is difficult to underlying motivation of customers. For example, the sentiment analysis may determine customers'feeling toward sad song as negative sentiment. In fact, the sad feeling may imply they are touched by the song.  Therefore, sentiment analysis of comment is often supplemented with emotion analysis that offer underltying emotion behind listeners.  The project aims to investigate he phenomenon by collecting comments from 100 sad and 100 romance youtube music


# data source
rommance song Youtube playlist

https://www.youtube.com/playlist?list=PLgzTt0k8mXzE6H9DDgiY7Pd8pKZteis48


sad_song Youtube playlist

https://www.youtube.com/playlist?list=PL3-sRm8xAzY-w9GS19pLXMyFRTuJcuUjy

# Project structure

# code_file

rommance_song.ipynb
-Jupyter file involving web scrawling of 100 Rommance Song, data cleaning and transformation by pandas and regrex expression

rommance_song_comment.ipynb
-Jupyter file involving web scrawling of 5174 comments from 100 Rommance Song,calculation of emotion and sentiment scores by text2emotion and Vader model.

sad_song.ipynb
-Jupyter file involving web scrawling of 100 sad Song, data cleaning and transformation by pandas and regrex expression

sad_song_comment.ipynb
-Jupyter file involving web scrawling of 5024 comments from 100 Sad Song,calculation of emotion and sentiment scores by text2emotion and Vader .

**It is noted that the youtube V3 api key was stored at the external json file for the protection of privacy**

**please use your own youtube V3 api key instead**

# Output_file
rommance_song_ytcomment.csv
- csv file involving 5174 rows of comments from rommance song and column involving text and calculation of emotion and sentiment score

rommance_song_ytvideo_statistics.csv
-csv file involving 100 rommance song and column involving statistic(viewcount,likecount,commentcount) and information(song_name,song_title) and calculation of average emotion and sentiment score of youtube video

sad_song_ytcomment.csv
- csv file involving 5024 rows of comments from sad song and column involving text and calculation of emotion and sentiment score

sad_song_ytvideo_statistics.csv
-csv file involving 100 rommance song and column involving statistic(viewcount,likecount,commentcount) and information(song_name,song_title) and calculation of average emotion and sentiment score of youtube video



# Powerbi file

- build the snowflake schema in the model view to reduce data redundancy and storage efficiency
  
snowflake design for rommance song
<img width="1167" height="842" alt="image" src="https://github.com/user-attachments/assets/0f31bb62-1f3f-43e3-8b97-3af72f90adbb" />


snowflake design for sad song
<img width="1353" height="809" alt="image" src="https://github.com/user-attachments/assets/e221dba6-be02-438d-93ff-2b812691e815" />



-  create measure for counting Sentiment Category and applying "and" logic to the emotion intensity slicers 

dax_function for sad song
<img width="1258" height="770" alt="image" src="https://github.com/user-attachments/assets/95658a18-5b72-46ba-9adb-9ea6f4b27dc9" />


dax function for rommance song 
<img width="1353" height="809" alt="image" src="https://github.com/user-attachments/assets/bece6a76-ff4a-4d1c-9117-c9c9c6325446" />


- build the 3 dashboard demonstrate the relationship between emotion and sentiment score in both video and comment level 




# Implication

# In video level

emotion and sentiment analysis of youtube_video
![image](https://github.com/user-attachments/assets/072f44c9-b464-41dd-b5ac-baa36f10483b)

mildly positive sentiment category is the only sentiment category in 100 rommance song video. 

- It implied the distribution of sentiment score is not discernible in the video level

mild negative sentiment were occupied half of whole sentiment catory in 100 sad_song_video. In addition, sad emotion were the highest frequency and proportion of intense category among other emotion.   

- It implied the Negative sentiment are associated the people's sad feeling aroused from the song.

# comment level

emotion and sentiment analysis of rommance_song_video level
![image](https://github.com/user-attachments/assets/94af2e54-7e95-4366-be76-b429607f7c0d)

emotion and sentiment analysis of sad_song video_level
![image](https://github.com/user-attachments/assets/d6bbca10-0701-4b59-a320-340d2e8cde47)


1.the majority of sentiment Category and emotion intensity is positive sentiment and Happy in rommance song comment respectively.In contrast,the majority of sentiment Category is  negative sentiment and sad in sad song comment respectively.

-  It indicated the Negative/Sad entiment are also associated the people's sad/Happy feeling aroused from the sad and rommance song respectively

2.As applying the emotion slicers from mild and intense Happiness,the frequency of positive sentiment is increased. In contrast, As applying the emotion slicers from mild and intense negative emotion(fear,sad,angry),the frequency of positive sentiment is increased, likewise when applying positive and negative sentiment in sentiment slicers to emotion intensity. 

- It inidicated the positive/negative sentiment in Vader model is associated with happy and negative emotion in text2emotion model respectively. 

3. When applying the emotion slicers to Intense Happiness and mild negative emotion(fear, sad, angry), the frequency of strongly positive sentiment category is increased drastically both rommance and sad song comment as compared only applying Intense Happiness in emotion slicers.
- When the happiness emotion is coupled with other mild negative emotion, it is more likely to evaluate as positive sentiment,particularly for strong sentiment
ma

# Conclusion
The sentiment and emotion score is mixed with listening's feeling evoked by the song, but not only the degree of contentment of listeners on the song.However, when positive emotion is mixed with mild negative emotion, the comment is more likely determined as positive sentiment. It implied Vader model may understand the some of the context behind comment that listener may feel touched genuinely by the song,when positive emotion is contrasted with negative emotion. It helps determine the degree of listeners on the song.Therefore, It is suggested emotion and sentiment analysis should be applied simultaneously

