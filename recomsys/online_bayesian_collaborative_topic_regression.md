# Collaborative topic regression  for online recommender systems: An online and Bayesian approach


citation : 47+

year : 2017

[paper](https://ink.library.smu.edu.sg/cgi/viewcontent.cgi?referer=http://scholar.google.com.tw/&httpsredir=1&article=4705&context=sis_research)

[github]

[doc for github](https://kuanchoulai10.github.io/index.html)


benchmark - 

1. MovieLens-10M-Plot, MovieLens-1M-Plot
   
2. Plot : collecting additional text content for each of the movie items - 

   * specifically, we collect the related text of plot summary of each item listed in the IMDB, hence, we have the text document to represent each movie.
   

# Abstract

Collaborative Topic Regression (話題協同回歸) 結合了兩個概念 1. 機率化的矩陣分解(probabilistic matrix factorization) 以及主題模型(Topic Modeling, e.g. LDA)

現存的CTR模型有2個主要的限制

1. 模型設計是基於 btach learning - 因此對於 streamming data / big data 不太適合
2. the item-specific topic proportions of LDA are fed to the downstream PMF, but not reverse.

我們提出一套新的推論算法 - Online Bayesian Inference algorithm for CTR model, 這是一套能夠從data stream 有效學習，可規模化的算法，我們的實驗結果戰士了此算法在真實世界資料集上的有效性

# Idea

1. Bayesian approach for online learning 
2. PMF, LDA

# Experiment

1. Dataset : 
   MovieLens-10M-Plot, MovieLens-1M-Plot
2. Metric : 
    RMSE - rating - regression problem
3. Evaluation procedure : 
   1. RMSE on the test set after every 5000 online iterations
   2. log-lilelihood of each word in text collection of topic modeling

4. Baseline : 
   1. RMSE : 
      1. Online Passive-Aggressive(PA) algorithm(2014)
      2. bdi-CTR(2011)
      3. odi-CTR
      4. obi-CTR
   2. preximity
      1. pass


# Result

# Other Discussion

MovieLens 10M stats:

records : 10,000,053 (10M)
user : 69,878
items : 10,681

Not Implemented

check : 

https://www.cakeresume.com/kcl10-pm-view

https://www.linkedin.com/in/kuanchoulai/




