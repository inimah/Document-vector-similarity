
Human (sometimes - not in all cases) can easily retrieve useful information from documents or categorizing documents, by looking at the contextual meaning of  words in a document, for instance. This also includes (but not necessarily) finding association / semantic meaning between words or documents in a natural way. Natural, since we, human, have been through a long process of learning language from the first time we were taught to read and speak. Computer, however, only understands logical mathematical function. To build a perfect language model that reflects every aspect of language understanding, this mathematical model may also need to be equipped with the ability to understand complex structure of language (e.g. by providing dictionary or look-up corpus, heuristic rules, and human annotation - which is labour-intensive and time consuming in many real world applications). This approach, however, is also a contradictive at some point, since highly depending on human feedbacks or annotations means we are disregarding the "subjectivity" aspect of human understanding on words and language. 

Word vector space model, exemplifies intellegent simplicity how we preceive words in geometrical space. Rather than trying to exactly mimic all aspects in linguistics,  

As such, to obtain a good languange model, the following nontrivial challenges :
- how to extract useful features (e.g. word vector representation) from the unstructured document, by only using mathematical ?
- how to find (hopefully) interesting pattern in the word-document clusters to be further evaluated with the original class label (if anys)

The different (and connection!) with previous studies???:
- focus on unsupervised approach (clustering)
- document-to-document level similarity, instead of word level similarity
- similarity metric distance for high dimensionality vector (since each word vector of WE represents n-dimensional vector, n depends on number of neurons used in training the word embedding)
