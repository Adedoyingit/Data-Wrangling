## Data Wrangling

In this project I gathered data, assessed the data, cleaned and visualized the data.

### Gatherered data from three different sources:
> Downloaded the csv file provided on udacity (twitter-archive-enhanced.csv)

> I used request library to download twitter image predictions from a url (image-predictions.tsv)

> I used the tweet_json.txt provided by udacity since I was unable to get my API keys before the project deadline.
Note: This was to be done by using tweepy library to query data via Twitter API.

### Assessed Data

I assessed the data both visually and programmatically (using some python libraries). I detected eight (8) quality issues and two (2) tidiness issues. 

#### Quality issues:
1.datatype of timestamp should be datetime data type not object

2.incorrect format for expanded urls for example 'https://gofundme.com/ydvmve-surgery-for-jax,ht...'	

3.repeated urls in the expanded_url column in df_twitter

4.missing expanded_urls

5.in_reply_to_status_id, in_reply_to_user_id, retweeted_status_id, retweeted_status_user_id and retweeted_status_timestamp has many nan values.

6.indescribable column names p1, p1_conf, p1 dog, p2,....

7.some of the values in p1 column of the dataframe df_image_clean are in capital letters while others are in small letters

8.retweet_count and favorite_count has missing values after merging the dataframes

#### Tidiness issues:
1.the last four columns in df_twitter should be in a column

2.tweet_id in df_image and df_tweet should be merged to df_twitter

I cleaned the data and did some visualisations to get insights from the visuals.

#### Insights from the data set:
1.The pupper has the highest count of the other dog_types

2.The img_num does not affect retweet_count or favorite_count

3.There is a positive correlation between retweet_count and favorite_count