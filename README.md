# Data Analysis on Reddit data, using Python  
  
The Python Reddit API Wrapper([PRAW](https://praw.readthedocs.io/en/latest/)) is used to extract information from Reddit. Analysis is carried out on this information using various Python libraries.  
  
## Overview  
  
[Reddit](https://reddit.com/) is a widely used social media website, with emphasis on social news aggregation, discussion and user content. [From Wikipedia](https://en.wikipedia.org/wiki/Reddit)  
> Reddit is an American social news aggregation, web content rating, and discussion website. Registered members submit content to the site such as links, text posts, images, and videos, which are then voted up or down by other members. Posts are organized by subject into user-created boards called "communities" or "subreddits", which cover a variety of topics such as news, politics, religion, science, movies, video games, music, books, sports, fitness, cooking, pets, and image-sharing. Submissions with more up-votes appear towards the top of their subreddit and, if they receive enough up-votes, ultimately on the site's front page.  
  
Using PRAW, data is retrieved from the website. Analysis is done in two Jupyter notebooks - one for a specific reddit post, while the other is for the analysis of two subreddits as a whole.  
  
## Dependencies used  
  
1. praw  
2. pandas  
3. matplotlib  
4. seaborn  
5. spacy  
6. textblob  
7. numpy  
  
## Details  
  
### [Sentiment Analysis on a specific Reddit post](https://github.com/pillaikartik10/python-reddit-analysis/blob/main/reddit-post-sentiment-analysis.ipynb)  
  
We select the [**Daily Discussion**](https://www.reddit.com/r/soccer/comments/noxewu/daily_discussion/) post dated 31st May 2021, from the [r/soccer](https://www.reddit.com/r/soccer/) subreddit as our specific post.  
  
We carry out the following operations :  
1. Read all comments beneath the post.  
2. Find out the sentiment value for each comment, using TextBlob.  
3. Clean the resultant data, and store it in a pandas DataFrame.  
4. Find out the total number of positive and negative comments.  
5. Find out the top 10 Proper Nouns used. This gives us an idea about the most-discussed topics.  
6. Find out the top 10 positive words used.  
  
### [Data Analysis and Comparison between two subreddits](https://github.com/pillaikartik10/python-reddit-analysis/blob/main/subreddit-analysis.ipynb)  
  
We select two subreddits for this purpose - [r/india](https://www.reddit.com/r/india/) and [r/politics](https://www.reddit.com/r/politics/).  
  
We carry out the following operations :  
1. For each subreddit,  
    a. Extract details of the top 100 posts from the last year, like account name, upvote ratio, total score(upvotes - downvotes), number of awards etc.  
    b. Analyse the source url of these posts.  
    c. Plot graphs between attributes like score, number of comments, number of awards etc to see whether any sort of relationship exists between them.  
2. For r/politics, find the most discussed topics among the top posts (by using the titles of the top 100 posts).  
3. Compare both subreddits using the respective descriptive statistics like mean score, mean upvote ratio, mean number of comments among their top 100 posts over the last year.
