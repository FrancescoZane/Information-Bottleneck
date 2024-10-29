# Information-Bottleneck

In the era of information overload, efficiently extracting relevant information from large datasets while discarding irrelevant details is crucial. The Information Bottleneck (IB) method, introduced by Tishby, Pereira, and Bialek, provides a principled approach for achieving this balance. This project aims to implement the IB method for clustering words from a collection of labeled texts, ultimately identifying words that maximally distinguish different text sources.

### The Information Bottleneck Method¶
The IB method focuses on finding a compressed representation of a random variable $$X$$ (in this case, words) that retains as much information as possible about another variable $$Y$$ (representing the labels of the text sources). This is achieved by optimizing a trade-off between the mutual information $$I(\tilde{X}; X)$$ and $$I(\tilde{X}; Y)$$, where $$\tilde{X}$$ is the compressed representation. The objective function is given by:

$$
L = I(\tilde{X}; X) - \beta \cdot I(\tilde{X}; Y)
$$
 
Here, $$\beta$$ is a trade-off parameter that balances compression and relevance.
