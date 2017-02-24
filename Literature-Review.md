I decide to create a brief summary of my literature review w.r.t to "Document vector similarity".

**Most likely to be my favourite papers (How do I know? I just know...) --> to be read**

| Reference        |Summary | 
| ------------- | ------------- | 
| \[1]. (Goldberg, 2016)      |  | 
| \[2]. https://openreview.net/pdf?id=SyK00v5xx      |  | 
| \[3]. (Schnabel, 2015) |  | 
| \[4]. (Levy, et al., 2015) |  |
| \[5]. (Arora, et al., 2016) |  |
| \[6]. (Joulin, et al., 2016) |  |
| \[7]. (Tai, et al., 2015) |  |
| \[8]. https://openreview.net/pdf?id=H1VyHY9gg | |


\[1]. Goldberg, Yoav. "A primer on neural network models for natural language processing." Journal of Artificial Intelligence Research 57 (2016): 345-420.

\[2]. Arora, Sanjeev, et al. "A Simple But Tough-to-Beat Baseline for Sentence Embeddings" (under review at ICLR2017)

\[3]. Schnabel, Tobias, et al. "Evaluation methods for unsupervised word embeddings." EMNLP. 2015.

\[4]. Levy, Omer, Yoav Goldberg, and Ido Dagan. "Improving distributional similarity with lessons learned from word embeddings." Transactions of the Association for Computational Linguistics 3 (2015): 211-225.

\[5]. Arora, Sanjeev, et al. "Linear algebraic structure of word senses, with applications to polysemy." arXiv preprint arXiv:1601.03764 (2016).

\[6]. Joulin, Armand, et al. "Bag of tricks for efficient text classification." arXiv preprint arXiv:1607.01759 (2016).

\[7]. Tai, Kai Sheng, Richard Socher, and Christopher D. Manning. "Improved semantic representations from tree-structured long short-term memory networks." arXiv preprint arXiv:1503.00075 (2015).

-----------------------------------------------------------------------------

**1. Word Embedding (WE)**

| Reference        | Keywords / Approaches  | Summary | Comments |
| ------------- |-------------| ------------- | ------------- | 
| \[1]. (Mikolov, et al., 2013a)      | a | | |
| \[2]. (Mikolov, et al., 2013b)      | b      |  | |
| \[3]. (Mikolov, et al., 2013c) | c      |  | |

My summary:



**2. Document/Sentence distance (sentence representation)**

| Reference | Keywords / Approaches  | Summary  | 
| ------------- |-------------| ------------- |
| \[4] (Cedric, et al., 2015) | Pair texts (sentences) similarity; Combination of word-embedding and tf-idf weighting; Skip gram | <ul><li>**Experiments**: Wikipedia corpus, word2vec, skip gram negative sampling, 5 words context windows, 400 dimensions (hidden neurons)</li><li>Compares on different sentence length (10, 20, 30 words)</li><li>Extract pairs (5M) &amp; non-pairs (5M) of semantically related texts (sentences),</li><li>**Vector representation** (to calculate cosine similarity): averaging WE, maximum WE, combining WE with TF-IDF weighting</li><li>**Result**: combination mean WE-TFIDF works well in shorter sentences (10 words). For longer texts (20 &amp; 30 words), mean WE-TFIDF from top 30% words with highest IDF outperforms other methods. Between distance metrics, Euclidian performs best.</li></ul> | 
| \[5]. (Weston, et al., 2014) | Hashtags (words) prediction based on context text (sentence), Averaging word embedding; CNN | <ul><li>generates WE with word2vec</li><li>use pre-trained WE on CNN</li><li>in WE feature extraction, vector summation &amp; average, TF-IDF weighting are used</li></ul> | 
| \[6]. (Santos & Ganti, 2014) | word-level embedding &amp; character-level embedding; Max vector | <ul><li>**Datasets**: texts of sentiment analysis domain from moview review &amp; twitter</li><li>use max operation to extract global fixed size of sentence feature/vector</li></ul>  | 
| \[7]. (Collobert, et al., 2011) | Multi-task learning WE, Averaging word vector | <ul><li>use max as compared to averaging methods of WE to represent sentence-embedding, but for multi-view purposes and comparison of benchmark syntactic-level tasks: e.g. POS tagging, chunking, NER, semantic role labelling</li><li>use pre-trained WE from larger unlabelled data as word look up table</li></ul> |
| \[8]. (Godin, et al., 2014) | POS tagging, Shallow net (skip gram) |  <ul><li>WE for POS tagging vs. manual feature engineering</li><li>best result: using word2vec skipgram with negative sampling and context window of 3</li></ul>
| \[9]. (Kang, et al., 2014) | Short-text matching (Q&A or conversation semantic matching), Multi Layer Perceptron and trimming to a fixed length |<ul><li>Compares vector space model (tf-idf cosine similarity), Latent Semantic Indexing (LSI)</li><li>tf-idf weighting of WE and then use top n word vectors</li></ul>|
| \[10]. (Zhang & LeCun, 2015) | K-means clustering of WE, temporal CNN |<ul><li>The authors apply CNN for ontology classification, sentiment analysis, and text categorization</li><li>it compares BOW, word2vec (BOW centroids), and CNN resulting CNN outperforms other models</li></ul>|
| \[11]. (Le & Mikolov, 2014) | Paragraph2Vec | <ul><li>claim to cover texts in any length: sentence, paragraph, document</li></ul> |
| \[12]. (Kusner, et al., 2015) | word-to-word similarity, closeness of word-pairs, minimal distance, moving distance | <ul><li>Aims to address challenge: similarity between uncommon words and synonym that is not addressed by frequency-based vector representation (e.g. name of people vs. their title: President, Prime Minister)</li><li>text documents as weighted point of embedded words</li><li>calculating distance between documents with word centroid distance (k-nearest neighbor)</li></ul>   | |
| \[13]. (Zheng & Callan, 2015) |  term-weighting, linear regression   | | |
| \[14]. (Hu, et al., 2014) |  pair & non-pair text fragments   | | |

**My Comments:**

\[4]. <ul><li>I don't quite understand why the authors specifically mention this multiplication (multiplying 400 dimension WE with the importance factors) (page 4 of 6) since minimizing lost function should be included in the generation stage of WE. Probably to highlight the importance of hyperparameter configuration in this stage then?</li></ul> 

\[5]. <ul><li>Skimming, my first intention is to know how the experiments generate sentence-vector representation</li><li>w.r.t. CNN, not sure if the authors' intention to use this NN architecture is either: because linear projection of input-first convolutional layer (shared weights), for dimensional reduction purpose, or because this NN has this "K" parameter that similar with window context in skip gram - but then with dense vector representation as input (?) Is it because they want to penalize negative vector values of WE (?) or expecting the benefit of pre-trained features if anys (?)</li></ul> 

\[6]. <ul><li>the authors only focus on longer sentence since they remove sentences that &lt; 20 or have &lt; 5 words &amp; discard any numerical values within text - probably because the text source is microblogs and they only want to focus in sentence polarity</li><li>This character-level embedding as convolutional layer, probably as same as stemming then?</li><li>I still don't quite understand with CNN experimental design - due to paper skimming - since they also used word2vec to generate WE</li></ul> 

\[7]. <ul><li>This paper is one of my favourites. The authors use WE representation for several benchmark tasks - which are extremely useful when you want to build syntactic look-ups for speech and language models (e.g. POS tagging, NER, ..) specifically for other language that is not as mature as english (w.r.t the availability of these lexical and syntactic corpus/dictionary).</li> <li>My remaining question, however, is the original motivation of this WE extraction. We want to use low representation of features (i.e. word vector), but then re-use (evaluate) this lower representation to further create high-level features(?) - but of course it can also be as a benchmark study that representation learnt from NN can achieve state-of-the-art results of hand-crafted features</li><li>Need to revisit</li></ul>

\[8]. <ul><li>The authors do not specifically explain in detail about document vector representation (assumption: probably because they do not investigate this matter). But they describe WE as per-word feature vector that can be concatenated into a single feature vector (which can be either a vector averaging or maximum approach) representing NN weight input vector for predicting the POS tag of central word</li></ul>

\[9]. <ul><li>The authors adopt the concept of canonical correlation analysis (i.e. to examine relationship between 2 multivariate sets of variables - in this case is 2 pair of Q&amp;A sentences), as such they need to define fixed length of n words within a sentence and then find correlation matrix between pair of sentences as a square matrix input of NN to predict matching (similarity) score of these 2 sentences. **BUT** in their study it's mainly for matching sentences. So it would highly depend on common words between these 2 Q&amp;A sentences, pairs of conversation as training sets, **WHILE** in our case it's different and purely unsupervised way (we use a collection of unlabelled documents consisting of sentences and words to be further clustered based on similarity distance)</li><li>It's not important (due to my frustation haha), but I don't quite understand why the authors use this "deep features" term - since basically it's a vector representation of pairs of sentence</li></ul>

\[10]. <ul><li>From their experiments, the authors claim that BOW features differ depending on data sets while word2vec features are same (?) - and it might also be the reason why BOW outperforms word2vec. The authors also hold the assumption that word2vec model does not have this linear separability as expected (?)</li></ul>

\[11].

\[12].

\[13].

**Overall comments/summary for paper in this topic**
<ul><li>WE models mostly perform well on tasks: word analogy, paraphrase identification, information retrieval, benchmark study for handcraft features (POS tagging, NER)</li></ul>

**3. Distance metrics**

| Reference        | About           | 
| ------------- |:-------------:| 
| (author,year)      | a | 
| (author,year)      | b      |  
| (author,year) | c      |   

My review:

**4. Document clustering**

| Reference        | About           | 
| ------------- |:-------------:| 
| (author,year)      | a | 
| (author,year)      | b      |  
| (author,year) | c      |   

My review:

**5. Deep Neural Networks**

| Reference        | About           | 
| ------------- |:-------------:| 
| (author,year)      | a | 
| (author,year)      | b      |  
| (author,year) | c      |   

My review:

**6. Evaluation**

| Reference        | About           | 
| ------------- |:-------------:| 
| (author,year)      | a | 
| (author,year)      | b      |  
| (author,year) | c      |   

My review:


**References:**

\[1]. T. Mikolov, W.-t. Yih, and G. Zweig, “Linguistic Regularities in Continuous Space Word Representations,” in Proceedings of NAACL HLT, Apr. 2013.

\[2]. T. Mikolov, I. Sutskever, K. Chen, G. Corrado, and J. Dean, “Distributed Representations of Words and Phrases and their Compositionality,” in NIPS 2013: Advances in neural information processing systems, Oct. 2013.

\[3]. T. Mikolov, K. Chen, G. Corrado, and J. Dean, “Efficient Estimation of Word Representations in Vector Space,” in Proceedings of Workshop at ICLR, Jan. 2013.

\[4]. De Boom, Cedric, et al. "Learning semantic similarity for very short texts." Data Mining Workshop (ICDMW), 2015 IEEE International Conference on. IEEE, 2015. 

\[5]. J. Weston, S. Chopra, and K. Adams, "#TagSpace: Semantic embeddings from hashtags," in Proceedings of the 2014 Conference on Empirical Methods in Natural Language Processing (EMNLP), 2014.

\[6]. C. N. dos Santos and M. Gatti, "Deep Convolutional Neural Networks for Sentiment Analysis of Short Texts," in COLING 2014, the 25th International Conference on Computational Linguistics, Dublin, Jul. 2014, pp. 69–78

\[7]. R. Collobert, J. Weston, L. Bottou, M. Karlen, K. Kavukcuoglu, and P. Kuksa, "Natural Language Processing (Almost) from Scratch," The Journal of Machine Learning Research, vol. 12, Feb. 2011.

\[8]. F. Godin, B. Vandersmissen, A. Jalalvand, W. De Neve, and R. Van de Walle, “Alleviating Manual Feature Engineering for Part-of-Speech Tagging of Twitter Microposts using Distributed Word Representations,” in Workshop on Modern Machine Learning and Natural Language Processing, NIPS 2014, Oct. 2014.

\[9]. L. Kang, B. Hu, X. Wu, Q. Chen, and Y. He, “A Short Texts Matching Method using Shallow Features and Deep Features,” in Third CCF Conference, NLPCC 2014, Nov. 2014.

\[10]. Zhang, Xiang, and Yann LeCun. "Text understanding from scratch." arXiv preprint arXiv:1502.01710 (2015).

\[11]. Q. V. Le and T. Mikolov, “Distributed Representations of Sentences and Documents,” arXiv.org, May 2014.

\[12]. M. J. Kusner, Y. Sun, N. I. Kolkin, and K. Q. Weinberger, “From Word Embeddings To Document Distances.” ICML, pp. 957–966, 2015.

\[13]. G. Zheng and J. Callan, “Learning to Reweight Terms with Distributed Representations,” in the 38th International ACM SIGIR  Conference. New York, New York, USA: ACM Press, 2015, pp. 575–584

\[14]. B. Hu, Z. Lu, H. Li, and Q. Chen, “Convolutional Neural Network Architectures for Matching Natural Language Sentences,” in NIPS 2014: Advances in Neural Information Processing Systems, 2014, pp. 2042–2050.

\[15]. Socher, Richard, et al. "Parsing natural scenes and natural language with recursive neural networks." Proceedings of the 28th international conference on machine learning (ICML-11). 2011.


**Other References (Books!):**

\[1]. Goodfellow, Ian, Yoshua Bengio, and Aaron Courville. Deep learning. MIT Press, 2016. [web version](http://www.deeplearningbook.org/)

\[2]. Martin, James H., and Daniel Jurafsky. "Speech and language processing." 3rd edition. [draft - web version](https://web.stanford.edu/~jurafsky/slp3/)

\[3]. Widdows, Dominic, and Dominic Widdows. Geometry and meaning. Vol. 773. Stanford: CSLI publications, 2004.

