
Notes on Personality Detection

* [Survey Analysis of Machine Learning Methods for Natural LanguageProcessing for MBTI Personality Type Prediction (2017)](https://pdfs.semanticscholar.org/a73a/238cfe4b906d51c3b66f1e9b58a1801596e4.pdf)

  They conducted several experiments on MBTI dataset from Kaggle. Dataset contains 8600 lines with 16 personality types. Each line starts with the personality type, followed by 50 posts of the user from PersonalityCafe forums.
  Preprocessing is applied to the raw text:
     1. converting lowercase
     2. NLTK lemmatizer to combine word forms
     3. Replacing special text (URLS, numbers, dates, emojis) with tokens
     4. Separating punctuation from text.
     5. Assigning words to numerical indices based on frequency in our training set (?)

   For feature selection, they use bag of words, with hyperparameter B that indicates the max number of words (starting from the most frequent).

    Baseline -> multiclass Softmax classifier 16-classes
    Other methods -> Naive Bayes, SVM
    Proposed -> Deep Learning as encoder/decoder architecture
    Best results on text data with DL as 38 %.


* [Recent Trends in Deep Learning Based Personality Detection (2019)](https://deepai.org/publication/recent-trends-in-deep-learning-based-personality-detection)
   With the increasing interest in personality detection, they conducted a review over deep-learning based methods.
   The methods are divided into three groups by the dataset types: text, audio and visual.
   The general approach using textual data is first feature extraction using (close or open vocabulary techniques) and apply end-to-end network.
   The network generally is based on LSTMs and CNNs. In audio data, MFCC features are used and with visual data cNNs used.
   There are bimodal and trimodal datasets/methods also. 