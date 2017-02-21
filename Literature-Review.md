I decide to create a brief summary of my literature review w.r.t to "Document vector similarity", which I clustered into several topic categorization.  
--------------------------------------------------------------------
Column 1                                                Column 2
------------------------------------------------------  ------------
I want the contents of this cell to fit into one line   Word1 Word2

------------------------------------------------------  ------------

: **Column 2 is narrow.** For column 1: 54 dashes in Markdown source 
for separator line; for column 2: 12 dashes in separator line (22% of column 1).


--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
Column 1                                                Column 2
------------------------------------------------------  ------------------------------------------------------------------------------------------------------------------------------------------------------------------
I want the contents of this cell to fit into one line   Word1 Word2

------------------------------------------------------  ------------------------------------------------------------------------------------------------------------------------------------------------------------------

: **Column 1 is narrow.** For column 1: 54 dashes in Markdown source for
separator line; for column 2: 162 dashes in separator line (300% of column 1).


**1. Word Embedding (WE)**

| Reference        | Keywords / Approaches  | Summary | Comments |
| ------------- |-------------| ------------- | ------------- | 
| \[1]. (Mikolov, et al., 2013a)      | a | | |
| \[2]. (Mikolov, et al., 2013b)      | b      |  | |
| \[3]. (Mikolov, et al., 2013c) | c      |  | |

My summary:

**2. Document/Sentence distance (sentence representation)**

| Reference | Keywords / Approaches  | Summary | Comments |
| ------- |-------| -------------------------- |-------| 
| \[4] (Cedric, et al., 2015) | Pair texts (sentences) similarity; Combination of word-embedding and tf-idf weighting; Skip gram | <ul><li>**Experiments**: Wikipedia corpus, word2vec, skip gram negative sampling, 5 words context windows, 400 dimensions (hidden neurons)</li><li>Compares on different sentence length (10, 20, 30 words)</li><li>Extract pairs (5M) &amp; non-pairs (5M) of semantically related texts (sentences),</li><li>**Vector representation** (to calculate cosine similarity): averaging WE, maximum WE, combining WE with TF-IDF weighting</li><li>**Result**: combination mean WE-TFIDF works well in shorter sentences (10 words). For longer texts (20 &amp; 30 words), mean WE-TFIDF from top 30% words with highest IDF outnumbers other methods. Between distance metrics, Euclidian performs best.</li></ul> | <ul><li>I don't quite understand why the authors specifically mention this multiplication (multiplying 400 dimension WE with the importance factors) (page 4 of 6) since minimizing lost function should be included in the generation stage of WE. Probably to highlight the importance of hyperparameter configuration in this stage then?</li></ul> |
| \[5]. (Weston, et al., 2014) | Hashtags (words) prediction based on context text (sentence), Averaging word embedding; CNN | <ul><li>generates WE with word2vec</li><li>use pre-trained WE on CNN</li><li>in WE feature extraction, vector summation &amp; average, TF-IDF weighting are used</li></ul> | <ul><li>Skimming to know how the experiments generate sentence-vector representation</li><li>w.r.t. CNN, not sure if the authors' intention to use this NN architecture is either: because linear projection of input-first convolutional layer (shared weights), for dimensional reduction purpose, or because this NN has this "K" parameter that similar with window context in skip gram - but then with dense vector representation as input (?) Is it because they want to penalize negative vector values of WE (?) or expecting the benefit of pre-trained features if anys (?)</li></ul> |
| \[6]. (Santos & Ganti, 2014) | word-level embedding &amp; character-level embedding; Max vector | <ul><li>**Datasets**: texts of sentiment analysis domain from moview review &amp; twitter</li><li>use max operation to extract global fixed size of sentence feature/vector</li></ul>  | <ul><li>the authors only focus on longer sentence since they remove sentences that &lt; 20 or have &lt; 5 words &amp; discard any numerical values within text - probably because the text source is microblogs and they only want to focus in sentence polarity</li><li>This character-level embedding as convolutional layer, probably as same as stemming then?</li><li>I still don't quite understand with CNN experimental design</li></ul> |
| \[7]. (Collobert, et al., 2011) | Averaging word vector |  | |
| \[8]. (Godin, et al., 2014) | Multi Layer Perceptron |  
| \[9]. (Kang, et al., 2014) | Multi Layer Perceptron and trimming to a fixed length |   | |
| \[10]. (Zhang & LeCun, 2015) | Clustering |   | |
| \[11]. (Le & Mikolov, 2014) | Paragraph2Vec |   | |
| \[12]. (Kusner, et al., 2015) | word-to-word similarity, minimal distance, moving distance | - evaluating distance with knn classifier   | |
| \[13]. (Zheng & Callan, 2015) |  term-weighting, linear regression   | | |
| \[14]. (Hu, et al., 2014) |  pair & non-pair text fragments   | | |

My summary:

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


**Other References (Books!):**

\[1]. Goodfellow, Ian, Yoshua Bengio, and Aaron Courville. Deep learning. MIT Press, 2016. [web version](http://www.deeplearningbook.org/)

\[2]. Martin, James H., and Daniel Jurafsky. "Speech and language processing." 3rd edition. [draft - web version](https://web.stanford.edu/~jurafsky/slp3/)

\[3]. Widdows, Dominic, and Dominic Widdows. Geometry and meaning. Vol. 773. Stanford: CSLI publications, 2004.

