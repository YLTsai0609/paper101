# Content-based recommendations with Poisson factorization

[paper](https://papers.nips.cc/paper/2014/file/97d0145823aeb8ed80617be62e08bdcc-Paper.pdf)

[code - official C++ star : 62+](https://github.com/premgopalan/collabtm)

[code - thirdparty python star 24+](https://github.com/david-cortes/ctpfrec/tree/4c88ce5020ab0d0fd3b0f5ad3c2389b77529c477)

year : 2014

citations : 187+

benchmark - 

1. arXiv dataset(10 years) 120,297 users, 825,707 articles, 43M observations.
2. Mendeley - 80,000 users, 260,000 articles, 5M observations.

[connected papers](https://www.connectedpapers.com/main/d01508b7f10468b47712cfdc19c028997b541dd1/Contentbased-recommendations-with-Poisson-factorization/graph)

# Abstract

1. Model both reader behavior and article text with Posson distribution.
2. exploit stochastic variational inference to model massive real-world datasets.

# Idea

Collaborative Topic Poisson Factorization (CTPF) model makes an assumption such that both ratings and item of datasets have a Poisson distribution.

By this way, CTPF is only concerend with non-zero ratings during training **therefore it is much more efficient and scalable compares to CTR model**.

# Result

# Other Discussion

[A Master thesis about Collaborative Topic Model Storyline](https://www.docdroid.net/8c4Ze1M/ctmp-paper-pdf#page=8)

[His paper and github 2019](https://github.com/buzzer4mornin/CTMP-ThesisProject)