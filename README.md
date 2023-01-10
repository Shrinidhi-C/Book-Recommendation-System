# Book-Recommendation-System
During the last few decades, with the rise of Youtube, Amazon, Netflix, and many other such web services, recommender systems have taken more and more place in our lives. From e-commerce to online advertisement recommender systems are today unavoidable in our daily online journeys.

![image](https://user-images.githubusercontent.com/57758182/211599254-da68604a-c304-43b3-8029-913df35560fa.png)


Generally recommended systems are the algorithms that suggest relevant items to users. Given
the “Book-Crossing” dataset with different files for books, users, and ratings, an attempt is made to
recommend books to users based on the dataset. Book recommendation not only helps users in
obtaining the next book of their interest to read but also the algorithm allows users to explore new
interests. In this project, we study different paradigms of recommender systems, for each of which we
describe their theoretical basis, study their working, and implementation, and discuss their pros and
cons.

Data preprocessing is performed in order to validate the anomalous data, handle missing
values, check the outliers, perform feature formatting, etc. The missing values in the features are
chosen to be replaced by the respective median value. The exploratory data analysis gives the basis
for hypotheses/understandings that are listed as follows.

● Agatha Christie, William Shakespeare, and Stephen King are the authors with the most number
of books being published. Therefore, these authors could be recommended based on most
books being published.

● 1996, 2002, and 1999 mark the years with the most number of books published.

● Harlequin, Silhouette, and Pocket have published the most number of books.

● The mean average rating of the books is around 8, and the distribution is left-skewed.

● USA (California, Texas), Canada(Ontario), Uk, and Germany host the largest number of book
publications and have obtained a large number of ratings as well.

● The Lovely Bones: A Novel by Alice Sebold, Wild Animus by Rich Shapero, and The Da Vinci Code
by Dan Brown are the books that are among the highest-rated ones. These could be the most
popular ones among the wide range of users.

● Stephen King, Nora Roberts, and J.K.Rowling are the authors with the most ratings. Hence,
these authors’ works can be recommended to any new user.

New features “Average-Rating” and “Book-Rating-Count” are introduced that are obtained
using the feature ‘Book-Rating”. The “Average-Rating” gives the mean rating of the book. Whereas, the
“ Book-Rating-Count” indicates the number of users that have rated the book.

Different paradigms of recommender systems, considered for the implementation of book
recommender system are:

1. Popularity-Based Recommender System

It's a kind of recommendation system that works on the principle of popularity and/or
whatever is trending. Average-Rating is used to make popular recommendations given that the book
has a minimum required number of ratings. It is advantageous due to its simplicity, less computational
usage, and ease to keep updated. However, there is a Lack of personalization, and poor accuracy in
recommendations, implying fewer profits generated.
The popular books that are recommended by the algorithm are quite popular ones with decent
ratings on “GoodReads”.

2. Weighted-Average-based Recommender System

The index used for recommendation here is the weighted average score. It is calculated using
‘Book-Rating’, the mean rating of books in the dataset, and requires a minimum number of ratings to
be considered for recommendation. Though the algorithm doesn’t make recommendations that are
sensitive to users’ preferences, it can be considered to perform pretty well, given the requirement for
generic recommendations.

The most rated books based on weighted average ratings consider the optimal proportion of both the
average rating of the book and the number of ratings into account.

3. Memory-Based Collaborative Filtering Recommendation System

Initially, data is filtered in order to get the users that have rated a required number of books
and the books that do have a minimum number of ratings required. Given the preferred book of the
user, the algorithm recommends books similar to the preference given. The similarity between the
books is computed using the book ratings that are stored in the user-item interaction matrix, based
on the cosine rule. It tries to bring the item-based similarity and make similar recommendations.

However, this method is not scalable, in applications with large data due to high computations.
The algorithm recommends books similar to the preferred one based on a similarity score of about
3.36.

4. Model-Based Collaborative Filtering Recommendation System
New representations of books and users are built based on a model that considers dense
vectors of reduced dimension. Recommendations are done following the model information. It relies
on the user-item interaction matrix and assumes latent factors in order to explain the interactions.
Matrix factorization method SVD(Singular Value Decomposition) is considered that decomposes the
huge sparse user-item interaction matrix into a product of dense and small user and item factor
matrices.

Given a user, the model returns the information regarding books that are rated by the user and the
top book recommendations that can be explored by the user. (unseen/new to the user).
The evaluation using the tuned SVD model results in an RMSE value of 1.50.
The user/item-specific recommendation requires prior data, leading to the cold-start problem.
Therefore possible solutions for the same would be to use the hybrid model of popularity-based/
weighted-average-based recommenders with the collaborative filtering approaches that require
user/item data.
