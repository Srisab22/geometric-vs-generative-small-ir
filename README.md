Geometric vs. Generative Retrieval Models (Small Datasets)
This project compares how two main Information Retrieval models perform:

Geometric Model: Vector Space Model (VSM) using TF-IDF and Cosine Similarity

## Generative Model: Query Likelihood Model (QLM) with Dirichlet Smoothing

The evaluation is done using two well-known small datasets: CISI and CRAN.

Datasets

CRAN (Cranfield Collection): A standard dataset used for testing IR systems.

CISI (Institute for Scientific Information): A classic IR dataset available online.

Findings & Conclusion

For these small datasets, the TF-IDF–based geometric model usually performs better than the Query Likelihood Model.

Key reasons:

Data Sparsity:
Small datasets like CRAN and CISI have limited documents and vocabulary. This makes it hard for probabilistic models to build reliable language models without overfitting or underfitting.

Strength of TF-IDF:
TF-IDF works very well for keyword matching and giving higher weight to rare but important terms. This is ideal for small, topic-focused datasets with simple document structures.

Smoothing Challenges:
QLM heavily depends on smoothing parameters (e.g., Dirichlet’s μ). In small datasets, choosing a single parameter that fits all queries is difficult, which reduces the model’s effectiveness.

Future Improvements

To boost the performance of the retrieval system—especially the generative side—the following ideas can help:

Use Larger Datasets:
Bigger and more diverse datasets will help probabilistic models like QLM learn better term distributions and generalize more accurately.

Apply Query Expansion:
Expanding queries with related or frequent terms (including Pseudo-Relevance Feedback) can help capture synonyms and improve matching between queries and document text.

Adaptive Smoothing:
Instead of using one fixed smoothing value, the system can try multiple values automatically and select the best one for each query to improve overall accuracy.
