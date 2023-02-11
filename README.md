# Simple-Sentence-Paraphraser-in-python
simple paraphraser that replaces words with synonyms in the correct context, using NER, WordNet, and BERT word embedding  
We first apply NER to the sentence to recognize the named entities and ensure they won't be replaced in further operations.

Then for every word in the sentence we explore each of its synsets in WordNet with the same part of speach tag. Finally we try to replace the word with its potential synonym and check the similarity between the original word and the replace one using BERT word embedding and cosine similarity.

Now we have for every word a list of potential replacements with their similarity. The last step is to try all possible combinations to generate a sentence, and assign a score to each new sentence by multiplying the similarity of the replaced words and sort the sentences by score.
