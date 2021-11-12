# Project 75
Andrew Seo

## Abstract:
I have been an NBA and specifically Boston Celtics fan seemingly all my life. My fandom coincides with the global popularity of the league and the sport in general. A big factor of this rise came from the proliferation of social media. On Twitter, this informal community is made up of a strange amalgamation of beat reporters, analysts, memelords, and team loyalists. "NBA Twitter" has become a corner of Twitter in and of itself to the point where it is now an important official part of the NBA news cycle. Reddit, on the other hand, is mostly amateurs and therefore more representative of the average fan and their off the cuff opinions. As I am often in my own Celtics echochamber on both platforms, I wanted to see what the average NBA fan was talking about most since the season began. Starting with all Reddit submissions since the start of the season, I used NLP and Unsupervised Learning techniques to obtain the most commonly discussed topics.      

## Design:
The goal of this project was to find out what the "common NBA man" cared most about. This is most immediately accomplished using dimensionality reduction to get initial topics. These topics can take a variety of routes through further exploration, EDA, or clustering. While the original design is frankly for myself, potential audiences for this information are NBA front offices/owners, who are often in their own teams' echochambers, as well as advertisers, to better market products that correspond to the discussed topics.   

## Data:
I acquired the 12,000 most recent submissions from the NBA Subreddit using the PSAW package. In the original grab there were over 80 columns, many of which were useless. The most relevant columns were author, selftext, and title. 

## Algorithms:

**_Data Collection_**
1. Using PSAW, acquired the most recent 12,000 submissions on the NBA Subreddit
2. Removed some of the noisier post types including highlights and game threads (comments of these posts are useful but not the submissions themsleves) 
3. Created a subset from the original dataframe of relevant columns
4. Grouped by user and aggregated all of their posts from the time period into one document

**_Data Preprocessing_**
1. Created copy of document column so that we can see before and after
2. Mapped the document column several times including leaving only letters, lower casing, and removing extra spaces. 
3. Used NLTK's stopwords library as well as custom stopwords to take out commonly used terms from the documents.
4. Used CountVectorizer and TF-IDFVectorizer to tokenize and vectorize the documents

**_Model Picking_**
1. Applied CountVectorizer documents to LSA with 1-10 topics
2. Applied TF-IDFVectorizer documents to LSA with 1-10 topics
3. Repated steps 1 and 2 for both NMF and LDA.
4. Went through all the different topic amounts to determine which topic number and which model made the most sense.

## Tools
- PSAW package on Pandas to obtain the data
- NLTK for natural language processing
- Pandas for general EDA and other text preprocessing
- LSA, LDA, NMF for dimensionality reduction
- Matplotlib and Seaborn for visualization

## Communication
Presentation of findings attached to this written description. This includes visualizations and conclusions. 
