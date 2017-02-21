# Document-vector-similarity

Experiments about word-document vector space representation for unsupervised learning approach of unstructured data. This includes:
- text-document similarity distance
- text-document clustering
- more insight on data, e.g. what characteristics makes one document differs with others: specific words used in the document? (in topical categorization), polarity of orientation? (in sentiment analysis or opinion mining)   
- evaluation on unsupervised word embedding
- evaluation of heterogeneous data sets (text, html, xml, microblogs)
- evaluation on words in different language (e.g. Dutch embedding)

Further reading towards motivations behind this study (and a brief summary of literature review!) can be read <a href="Background-Motivations.md"> {{here}} </a>

We use the following data sets in this study:

1. Toy Information Retrieval (IR) data

Text documents (total 24 docs) are purposefully generated for common IR-similarity distance problems.Each document consists of a single sentence that either has "dog", "cat", or "mouse" words. The purpose of this toy data sets is for analysing how word-embeddings approach(es) will perform on finding the similarity in this small set of unlabelled data that can be easily evaluated (by human feedback). 
The example of sentences in document corpus:
   
2. Shakespeare plays
Shakespeare's play and poetry data sets, which are categorized into 4 categories of genres (comedy, history, tragedy, poetry). Preliminary experiments (https://github.com/sereprz/ShakespeareTextAnalysis) has investigated the word vector of similar data sets but more focusing on the analysis of specific words in topical categorization and sentiment analysis problems. Likewise, we want to expore how document clustering with detect interesting insights and (hopefully) useful patterns in this classification problem.


3. Newsfeed data sets


3. Dutch wikipedia embedding


Methods
