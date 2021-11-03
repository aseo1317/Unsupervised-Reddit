# Cup Half-Empty

## Question
Few things inspire more passion than sports. Positive, negative, or somewhere in between, sports fans aren't shy about expressing their feelings about their favorite teams. Social media, such as Reddit and Twitter, has provided more outlets than ever before, allowing fans to provide both knee-jerk reactions and long explanations. Often these feelings tend to be either overly critical or overly optimistic about their teams compared to how the fans of that sport (but not of that specific team) feel. In this project, I will be looking to compare how Boston Celtics fans feel about their team vs how the rest of the NBA's fans feel about the Celtics. Because team access is more direct than ever before, fans' opinions seem to have a greater effect on team management than ever before. Through this analysis, team owners and C-suites can see how (un)reasonable their fans are about different topics. Fans themselves can also benefit from this analysis to see if the temperature of their opinions is somewhat in line with the general NBA fanbase. 

## Data
I will be using Reddit's API to acquire data from both the Celtics subreddit as well as the general NBA subreddit. I may start off general but an easy comparison may be the "post-game" threads that immediately pop up following a game. I'm not quite sure which method I will go with but an initial search shows PRAW, pushshift, and PSAW as options to acquire the data. Each sample/unit of analysis will be a Reddit post with body or a comment of the post. I expect to see names most frequently including top players Jayson Tatum, Jaylen Brown, and Marcus Smart as well as ex-coach and current-GM Brad Stevens followed by basketball lingo such as "defense", "shooting", or "rebounding". I expect the Celtics subreddit to have a worse sentiment on the team than other NBA fans, because Boston sports fans are notoriously harsh on all of their teams.  

## Tools
I will be using one or a combination of PRAW, pushshift, and PSAW for data acquisition. For text processing, I will be using NLTK, spaCy, and Scikit-learn. For visualization, I will be using Matplotlib, Seaborn, and Tableau. 

## MVP Goal:
I hope to get to the topic modeling stage discussed in class such as Latent Semantic Analysis and Non-Negative Matrix Factorization. If I can get to this stage for both subreddits, I will be in a good place to gauge general sentiments. 
