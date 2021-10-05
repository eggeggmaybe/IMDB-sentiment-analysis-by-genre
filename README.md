# IMDB-sentiment-analysis-by-genre
increased sentiment analysis accuracy by using scored genre specific lexicon (compared to using general scored general lexicon)

The object of this project is to see if doing sentiment analysis using genre specific lexicon (updated from original dataset (Potts, 2011)) will increase accuracy. The code used in the project is supplied. In short, the original dataset including movie comments will be divided into genres folders. Each genre will have their own lexicon with word scores and this is updated using the original scored lexicon. The update is just simple polarity switch based on semantic orientations (SO) because I didn't mimick the original way to create the scored lexicon. For example, "funny" can be +1.5 in the original scored lexicon but it can be -2 in a "Horror" movie review.

"aclImdb":
original dataset (Potts, 2011)
This can be downloaded from "https://ai.stanford.edu/~amaas/data/sentiment/".

"Logistic_regression_models.ipynb":
A simple logistic regression classifier. You can use yours.

"url_info_extractor.ipynb" :
This is used for scrapping movie titles and genres from IMDB website. 
URLs of a movie are needed and the ULR must include the movie ID. For example, in "http://www.imdb.com/title/tt0893406/usercomments", "tt0893406" is the movie ID and anything after this is optional.

"Genre_split.ipynb": 
This is used for splitting the original dataset (IMDB reviews) into their movie genre folders. For example, a comment of a movie labeled with "Drama" and "Horror" on IMDB will be sorted into both "Drama" and "Horror" folders.
This includes the python file to generate genre specific bow (both testing and training), extra features (both testing and training), updated lexicon (only training) and positive and negative reviews sorted in genre folders (both testing and training)

After you run "Genre_split.ipynb":
"genre" folder has every output included, if you goes in, you can find:
1. updated bow in "bow" folder including the genre specific bow for both training and testing set 
2. extra features in "exclamation_count" and "word_count" folders for both training and testing set 
3. updated lexicon in "lexicon" folders for only training set
4. "pos" and "neg" folders including positive and negative reviews sorted in genre folders for both training and testing set respectively
5. "for_pmi_only" folder including both positive and negative reviews sorted in genre folders for only training set
