# Movie_Recommender
I had created a basic Natural Language processing movie system a while back and here is how it worked.

I used the [Top 10,000 movies dataset from Kaggle]([https://www.github.com/cruelkratos](https://www.kaggle.com/datasets/ahsanaseer/top-rated-tmdb-movies-10k)https://www.kaggle.com/datasets/ahsanaseer/top-rated-tmdb-movies-10k).
Firstly i did some basic pre-processing of the datset such as removing null values checking for duplicates etc.

# Algorithm:
Firstly i used the sklearn library's CountVectorizer implementation which automatically removes stop words (stop words include stuff like 'and' 'or' 'is' etc.) as they don't implicitly convey any meaning to the sentiment of the text.
Tokenization now takes place which is often done through a sub-word approach.
Stemming:
Portter's Stemmer Algorithm - based on the idea that a suffix == sub-suffix + some extra stuff
we use this algorithm to convert words like -> walked/walks/walking to walk.
Finally we vectorize the words and apply a function called cosine similarity to calculate the distance between the tags of all movies
the top-5 smallest distance ones are reccomended by the algorithm.
each distance is calculated as follows:
$$\cos{\theta} = \frac{A\cdot B}{|A||B|} = \frac{\sum_{i\in N} A_iB_i}{|A||B|} $$

pretty basic stuff tbh i am just learning NLP rn.
