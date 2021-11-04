# Fake-News-Classifier-using-BiDirectional-LSTM
**Data Set** - https://www.kaggle.com/c/fake-news/data#. You can download the data from here.  
We will use both LSTM and Bi-Directional LSTM to see which performs better.  
## LSTM
Drop the null values first and seperate the dependent and independent features. We will be working on the title column alone.  
### Preprocessing
Removing all characters except alphabets. Converting everything to lower case and create a list of words. Remove the stopwords and use porter stemmer on the remaining words. Finally joining the words back and appending each sentence into a list.  
We do one hot representation of the words of each sentence by selecting a vocabulary sixe of 5000(This can take any value according to you). You will notice that we get vectors of varying lengths. So we do padding of them and add 0's to make all of them reach the same length. We create the LSTM model after that. We even try adding dropout layers. We split the data in train and test sets. Finally we check the accuracy.

## Bi-Directional LSTM
All the steps will be the same as above. Only in model creation we will add a bidirectional lstm layer instead of a lstm layer.  

**We are getting almost similar accuracy from both the models here. But in many cases Bi-Directional LSTM performs better.**
