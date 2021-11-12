# Project 75
Andrew Seo

## Abstract:
Over my first four years in New York, I was just another college student who treated alcohol (including wine) as a means to an end. In my last four years in New York, I have developed a love for wine, specifically natural wine. New York has also seen an explosive growth in wine and natural wines with new wine stores and wine bars opening seemingly monthly. Just ten minutes from me is an intersection with 3 wine bars all looking at each other and 2 wine stores. I want to share this love of wine and there is no better way to get people to like wines than by drinking good ones. I attempt to dig into a wine review dataset to determine which factors had the most impact on good wines. I used pandas to clean and perform EDA on my data, different scikit-learn packages for modeling, and matplot and seaborn for visualizations.

## Design:
My intended end goal of this project was to create a model(s) that could serve as a soft recommendation system for the average consumer or perhaps wine store employees looking for some recommendation guidance, with the caveat that wine can be very subjective so context and preference does matter. I tried out a variety of classification models and made adjustments to get a general sense of how they performed. After picking the best performing model, I tested on my holdout set.   

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
