# SVMs
SVMs via sub-gradient descent and quadratic programming with sentiment analysis on tweets on US airline service quality. 

# Data Set
-The data comes in the form of a csv table. The columns most relevant to our task are 'text' and 'airline_sentiment'.
-Data must be represented as a [N x d] matrix, but what we have on our hands is unstructured text.
-The simplest solution to transform an airline review into a vector is bag of words. We maintain a global vocabulary of word patterns gathered from our corpus, with single words such as "great", "horrible", and optionally consecutive words (N-grams) like "friendly service", "luggage lost". Suppose we have already collected a total of 10000 such patterns, to transform a sentence into a 10000-dimensional vector, we simply scan it and look for the patterns that appear and set their correponding entries to 1 and leave the rest at 0. What we end up with is a sparse vector that can be fed into SVMs.
-The data is not balanced, with siginificant more negatives than neutral + positives. Therefore we group neutral and positive into one category and the final ratio of non-negative vs negative is about 1:2. This is consistent across train, val and test.


# Prediction Accuracy:

## Linear Kernel

![Linear Kernel SVM](https://user-images.githubusercontent.com/95513386/145899481-c447c3dc-3e31-4fe7-99e5-ebe01311a99b.jpg)

## Gaussian Kernel

![Gaussian Kernel SVM](https://user-images.githubusercontent.com/95513386/145899503-994ec500-2458-4313-a923-c7ba48f1bf66.jpg)
