# PresidentialElection

**1.VADER Sentiment Analysis :**<br>
VADER (Valence Aware Dictionary and sEntiment Reasoner) is a lexicon and rule-based sentiment analysis tool that is specifically attuned to sentiments expressed in social media. VADER uses a combination of A sentiment lexicon is a list of lexical features (e.g., words) which are generally labeled according to their semantic orientation as either positive or negative. VADER not only tells about the Positivity and Negativity score but also tells us about how positive or negative a sentiment is. <br>


The Compound score is a metric that calculates the sum of all the lexicon ratings which have been normalized between -1(most extreme negative) and +1 (most extreme positive).

-positive sentiment : (compound score >= 0.05)<br>
-neutral sentiment : (compound score > -0.05) and (compound score < 0.05) <br>
-negative sentiment : (compound score <= -0.05)<br>


**2.Multinomial Naive Bayes :**<br>
The framework of this sentiment analysis project <br>
It contains fourmodules as follows:<br>
● Data Preprocessing <br>
● TF-IDF Vectorization <br>
● Naive Bayes Classifier <br>
● Prediction <br>

We compute the TF-IDF values for all the words in the tweets in the training as well the testing set. The TFIDF Vectorizer outputs a sparse matrix where each row corresponds to the index of particular tweet and each column corresponds to the index  of a word in that tweet with that word’s TF-IDF value stored that the specific row and column. We consider unigrams and bigrams of different words in each tweet which provides us with better understanding of the sentiment. The matrix of the training set is given as input to the classifier along with the sentiment classification of each tweet.The matrix of the testing set is then used to predict the sentiment classification.<br>

**3.BERT :**<br>
**BERT** stands for **Bidirectional Encoder Representations from Transformers**<br>
● Bidirectional - to understand the text you’re looking you’ll have to look back (at the previous words) and forward (at the next words)<br>
● Transformers -  Transformer model. The Transformer reads entire sequences of tokens at once. In a sense, the model is non-directional, while LSTMs read sequentially (left-to-right or right-to-left). The attention mechanism allows for learning contextual relations between words.<br>
● (Pre-trained) contextualized word embeddings - The ELMO paper introduced a way to encode words based on their meaning/context. Nails has multiple meanings - fingernails and     metal nails.<br>

  **Data Preprocessing**
    You might already know that Machine Learning models don’t work with raw text. You need to convert text to numbers (of some sort). BERT requires even more attention. H

  ● Add special tokens to separate sentences and do classification<br>
  ● Pass sequences of constant length (introduce padding)<br>
  ● Create array of 0s (pad token) and 1s (real token) called attention mask<br>
  ● The Transformers library provides  a wide variety of Transformer models (including BERT). It works with TensorFlow and PyTorch! It also includes prebuild     tokenizers that     do the heavy lifting for us.<br>
