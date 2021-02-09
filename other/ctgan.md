# Modeling Tabular Data using Conditional GAN

[paper](https://arxiv.org/pdf/1907.00503.pdf)

[github - pytorch](https://github.com/sdv-dev/CTGAN)

benchmark - 7 simulated and 8 real datasets(UCI machine learning) with several baysian network baselines.

from UCI, Kaggle, MNIST

1. adult
2. census
3. covertype
4. intrusion 
5. news
6. credit from Kaggle
7. MNIST28
8. MNIST12

# Abstract

1. Modeling the probability distribution of rows in tabular data and generating realistic synthetic data is hard.
2. Continuous columns nay have multiple modes whereas discrete columns are sometimes imblanced.
3. Existing statistical and dnn fail to synthetize those data - we solved this by our design : conditional generator.

# Idea

1. Mode-specific Normalization by VGM
2. Conditional Generator 
3. Training by Sampling
4. TVAE Model

# Result

7 simulation data

8 real dataset from UCI machine learning

1. adult

# Other Discussion

[VGM - BayesianGaussianMixture from sklearn](https://scikit-learn.org/stable/modules/generated/sklearn.mixture.BayesianGaussianMixture.html)

[(ML 16.6) Gaussian mixture model (Mixture of Gaussians)](https://www.youtube.com/watch?v=Rkl30Fr2S38)

[Gaussian Mixture Models](https://www.youtube.com/watch?v=q71Niz856KE)
