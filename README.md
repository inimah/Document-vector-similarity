# Document-vector-similarity

Experiments about word-document vector, which includes:
- text-document similarity distance
- text-document clustering
- more insight on data, e.g. what characteristics makes one document differs with others: specific words used in the document? (in topical categorization), polarity of orientation? (in sentiment analysis or opinion mining)   
- evaluation on unsupervised word embedding
- evaluation of heterogeneous data sets (text, html, xml, microblogs)
- evaluation on words in different language (e.g. Dutch embedding)

Further reading towards motivations behind this study (and a brief summary of literature review!) can be read <a href="Background-Motivations.md"> {{here}} </a>

**#We use the following data sets in this study:**

Basically these data sets need to include challenges in learning unstructured data, such as:
- Negation issue (mostly found in sentiment analysis) 
- Word morphological issue (e.g. mouse vs. mice)
- Synonym
- Different document (sentence) length

1. Toy (syntetic) data sets
   
   Text documents (total 24 docs) are purposefully generated for investigating common IR-similarity distance problems. Each document consists of a single sentence that either has "dog", "cat", or "mouse" words. The purpose of this toy data sets is for analysing how word-embeddings approach(es) will perform on finding the similarity in this small set of unlabelled data that can be easily evaluated (by human feedback). 
   
   The example of sentences in document corpus:
   
2. Shakespeare plays
   
   Consists of Shakespeare's play and poetry data sets, which are categorized into 4 genres (comedy, history, tragedy, poetry). Preliminary experiments (https://github.com/sereprz/ShakespeareTextAnalysis) has investigated the word vector of similar data sets but more focusing on the analysis of specific words in topical categorization and sentiment analysis problems. Likewise, we want to expore how document clustering with detect interesting insights and (hopefully) useful patterns in this classification problem.


3. Essay data

   Data sets are retrieved from https://www.kaggle.com/c/asap-aes. This data consist of the following attributes:
   - essay ID
   - essay-set ID (category ID of essay based on Da Set #n--ReadMeFirst documents)
   - score1 and score2 (only for train.tsv, the other data set like public_leaderboard.tsv has separated label solution public_leaderboard_solution.tsv)
   - essay text

4. Newsfeed data sets
   tba

5. Dutch wikipedia embedding
   tba

Methods:

1. Feature extraction (Sentence-document vector representation)
<ul><li>TF-IDF Bag of Words</li><li>Skip gram with vector averaging</li><li>Skip gram with vector min-max</li><li>Skip gram with TF-IDF weighting</li></ul>

2. Distance metrics:
<ul><li>Cosine similarity</li><li>Euclidian distance</li><li>Jaccard similarity</li><li>...</li></ul>

3. Evaluation

