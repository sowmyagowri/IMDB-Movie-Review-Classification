# IMDB-Movie-Review-Classification
Python program to classify movie reviews based on Knn

#### Approach:
1.  The input training data and testing data were first “cleaned” using a pre-processor function (user-defined) to remove all words that do not contribute to the sentiment of the review.
2.  This pre-processed review of training and testing data were then converted to TF-IDF CSR sparse matrices and L2 normalized.
3.  The cosine similarity between the L2-normalized testing data and L2-normalized training data was then calculated based on the formula

4.  The top k values in each of the row in the above calculated cosine similarity matrix was then taken. This is now the list of k training   reviews that are closest to the test review. 
5.  The total number of positive reviews and the total number of negative reviews were then determined for the top k training reviews.    
    The test review was then labeled as positive if the total number of positive reviews was higher while the review was labeled              negative if the total number of negative reviews was higher.
