# Part of Speech Tagger 

Part of speech(POS) of a word is its grammatical property like noun, pronoun, verb, adjective etc. POS tagging is assigning words in a corpus with their respective parts of speech. The pos_tagger.ipynb notebook shows how to pos tag for custom corpus through nltk.

* **Unigram** -
Most frequent tag for the word in training corpus.
* **Bigram** -
It uses a tuple consisting of the token’s base type and the tags of the 1(n-1) preceding tokens.
* **Trigram** - 
It uses a tuple consisting of the token’s base type and the tags of the 2 preceding tokens. It then picks the tag which is most likely for that context. The bi/trigram  does not support unknown words on its own it is backed off with (n-1)gram.
* **HMM** -
Unobservable states are pos tags and observable ouputs are words.

## Result
To undertand how well our pos tagger is assigning tags standard metrics like accuracy, precision, recall and fscore are used.
Following are the metrics for different tagger methods evaluated.

Tagger | Accuracy |Precision | Recall | F1score
-------|----------|----------|--------|--------
Unigram|  85.13   |   91.2   | 85.13  | 87.48
Trigram|  86.54   |   92.66  | 86.54  | 89.15       
HMM    |  43.64   |   87.27  | 43.64  | 51.41

###### Tools Used
* Jupyter Notebook (Python 3)
* Nltk (for tagged file reading etc.)
* Scikit-learn
