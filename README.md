# Information Retrival

## 1. Report statistics of the index
- The collection consists of 475 documents.
    
- The number of terms in the collection is 40172.
    
- The total term frequency in the collection is 348669.
    
- The average document length in the collection is 734.04 terms.

**The top 10 most frequent terms and their inverse document frequencies in the collection are:**

| Term | Frequency | Inverse Frequency |
|------|-----------|-------------------|
| one  | 432       | 0.09              |
| time | 409       | 0.15              |
| like | 384       | 0.21              |
| look | 368       | 0.26              |
| see  | 360       | 0.28              |
| go   | 359       | 0.28              |
| day  | 354       | 0.29              |
| get  | 354       | 0.29              |
| back | 352       | 0.31              |
| said | 347       | 0.31              |


## 2. Report results of Boolean queries
| Boolean Query      | Result                                                                                                                                                                                                                                                                                                                                                                                             |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ben AND june       | {0, 298, 149, 407, 410}                                                                                                                                                                                                                                                                                                                                                                           |
| ben OR june        | {0, 128, 141, 17, 149, 21, 407, 151, 410, 284, 290, 36, 422, 167, 298, 53, 186, 315, 59, 66, 327, 74, 75, 81, 85, 344, 225, 109, 237, 377, 123, 125, 126}                                                                                                                                                                                                                                  |
| ben AND NOT june   | {128, 225, 66, 36, 75, 123, 109, 141, 17, 85, 344, 315}                                                                                                                                                                                                                                                                                                                                          |
| ben OR adler NOT june | {128, 225, 66, 36, 75, 141, 109, 17, 315, 85, 344, 123}                                                                                                                                                                                                                                                                                                                                         |



## 3. Results of free text queries for ranked retrieval and comparison with Boolean retrieval 
    The results of a ranked retrieval process using the term-at-a-time (TAAT) algorithm returned the top 10 documents ranked by their relevance to a given query, the table lists the rank, document ID, cosine similarity, and document score of each of the 10 documents.

    Query: |Ben June|


| Rank | Doc ID | Cosine Similarity | Document Score |
|------|--------|-------------------|----------------|
| 1    | 0      | 0.62              | 0.62           |
| 2    | 149    | 0.56              | 0.56           |
| 3    | 298    | 0.55              | 0.55           |
| 4    | 407    | 0.47              | 0.47           |
| 5    | 410    | 0.46              | 0.46           |
| 6    | 17     | 0.37              | 0.37           |
| 7    | 36     | 0.34              | 0.34           |
| 8    | 66     | 0.31              | 0.31           |
| 9    | 75     | 0.30              | 0.30           |
| 10   | 85     | 0.29              | 0.29           |

    

    The Boolean query AND result of "Ben June" returns a set of documents that contain both terms "Ben" and "June". The result is a set of document IDs \fbox{0, 298, 149, 407, 410}.
    
    On the other hand, the Taat retrieval result for the same query returns a ranked list of documents sorted in descending order of their similarity score. The list is \fbox{0, 149, 298, 407, 410, 17, 36, 66, 75, 85}.
    
    The Boolean query AND result returns a set of documents that strictly contain both terms "Ben" and "June". It is a precise result but may not include all relevant documents. The Taat retrieval result, however, returns a ranked list of documents based on their similarity scores, which takes into account the relevance of documents that contain either "Ben" or "June" or both. The Taat result may include more relevant documents but may also include irrelevant documents.
    
    Overall, Boolean retrieval provides a precise answer, but it may not include all relevant documents, while ranked retrieval techniques like Taat retrieval provide a more comprehensive answer, but it may include irrelevant documents as well.