# Project Reddit

## Data:
I downloaded a Reddit dataset of ~4,000 comments from Reddit using its API. The comments come from the post-game threads on the Celtics and NBA subreddits. My original intent was to do a sentiment analysis comparing these two threads but I am not sure how I will got about this when I don't have clearl sentiment scores. Perhaps I will use the upvote/downvote scores.  

## Initial Results and Visuals:
I have made initial steps to preprocess the data removing new lines, links, punctuations, alphanumerics, and making all the text lowercase. I then used both Count Vectorizer and TF-IDF. I've also taken initial stabs at LSA, NMF, and LDA with the latest allowing me to have a visual. 

![Screen Shot 2021-11-09 at 3 37 13 AM](https://user-images.githubusercontent.com/89528655/140890300-a6e5427a-611b-4386-9605-003cfe72d8ca.png)

Here I have used pyLDAvis to visualize a 15 component LDA model on the Celtics text set and TF-IDF. So far, the topics aren't very clear and it's obvious I need to filter by more stopwords. I have tried using 1-10 topic numbers as well and nothing too useful yet. 

## Next Steps/Concerns:
- I may need more data but that may be tricky. I have deliberately narrowed down to post-game threads so that the posts from the NBA subreddit are Celtics oriented. There are only 10 post-game threads so far and I have taken from all of them. One solution to this is instead taking top users and topic modeling on that but that would make it more difficult to compare across subreddits.
- Even if I were to keep my original dataset, I may look to group it by users so that each document is the sum of that user's contributions to the subreddit. 
- How am I going to measure sentiment without any actual scores? Need to look into VADER and TextBlob.
- I have not reached this stage yet but what is my endpoint after delineating topics? Trying to think about what to produce for the presentation.  
