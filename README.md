# IMDB-sentiment-analysis-by-genre
increased sentiment analysis accuracy by using scored genre specific lexicon (compared to using general scored general lexicon)

"aclImdb":
original dataset (Potts, 2011)



"url_info_extractor.ipynb" :
This is used for scrapping movie titles and genres from IMDB website. 
URLs of a movie are needed and the ULR must include the movie ID. For example, in "http://www.imdb.com/title/tt0893406/usercomments", "tt0893406" is the movie ID and anything after this is optional.



"Logistic_regression_models.ipynb":
include training and testing model python code 
one should run "machine learning using all the data" section then run "Sum of word scores model (General model 2 and genre specific models)" section with different lexicons and genre names to get the genre specific model output
or run "machine learning using all the data" section then run "Sum of word scores model (General model 2 and genre specific models)" section with general lexicon to get the genreal model 1
or run "machine learning using all the data" section then run "BOW models (General model 1)" section to get general BOW model



"Genre_split.ipynb": 
This is used for splitting the original dataset (IMDB reviews) into their movie genre folders. For example, a comment of a movie labeled with "Drama" and "Horror" on IMDB will be sorted into both "Drama" and "Horror" folders.

This includes the python file to generate genre specific bow (both testing and training), extra features (both testing and training), updated lexicon (only training) and positive and negative reviews sorted in genre folders (both testing and training)

one can just run through the python file to get exactly same files as those included in the folder (you need to change the file path in the python code)

"genre" folder has every output included, if you goes in, you can find:
1. updated bow in "bow" folder including the genre specific bow for both training and testing set 
2. extra features in "exclamation_count" and "word_count" folders for both training and testing set 
3. updated lexicon in "lexicon" folders for only training set
4. "pos" and "neg" folders including positive and negative reviews sorted in genre folders for both training and testing set respectively
5. "for_pmi_only" folder including both positive and negative reviews sorted in genre folders for only training set
