# Stacked Capsule Autoencoders

[paper](https://arxiv.org/pdf/1906.06818v2.pdf)

[github](https://github.com/google-research/google-research/tree/master/stacked_capsule_autoencoders)

2019

Adam R. Kosiorek
Sara Sabour
Yee Whye Teh
Geoffrey E. Hinton

# 摘要

Objects are composed of a set of geometrically organized parts. We introduce
an unsupervised capsule autoencoder (SCAE), which explicitly uses geometric
relationships between parts to reason about objects. Since these relationships do
not depend on the viewpoint, our model is robust to viewpoint changes. SCAE
consists of two stages. In the first stage, the model predicts presences and poses of
part templates directly from the image and tries to reconstruct the image by appropriately arranging the templates. In the second stage, SCAE predicts parameters of
a few object capsules, which are then used to reconstruct part poses. Inference in
this model is amortized and performed by off-the-shelf neural encoders, unlike in
previous capsule networks. We find that object capsule presences are highly informative of the object class, which leads to state-of-the-art results for unsupervised
classification on SVHN (55%) and MNIST (98.7%).

人們通常透過物體的幾何形狀去了解他們，我們介紹了一種非監督式的膠囊網路(capsule autoencoder)，這種網路使用幾何關係來記憶物體，而這種幾何關係並不會因為視角改變而改變，因此建立出來的模型具有視角強健性
非監督膠囊網路(SCAE)由兩階段組合，第一階段，模型會試著重新排列模板來重建圖像，以預測目前物件的姿態，第二階段，模型則會預測幾個模型則會預測幾個對象膠囊的參數(該膠囊用於重建圖像)，和之前的膠囊網路不同的地方是，我們發現object capsule presences能夠非常好的擷取物件的資訊，也因此我們在非監督式SVHN以及非監督式 MNIST都取得了SOTA

# 其他導讀

[AAAI Conference 知乎導讀](https://zhuanlan.zhihu.com/p/106305139?fbclid=IwAR2HvU3dZKbETUazn4vRfYOLEiOJD2hqkGz4QgSWyx6Z405rU5NM9sU20tA)

物件偵測上主要基於兩種方法:

* 傳統手工特徵，例如HOG, LP等等，通常涉及很多手動操作，這樣深層次的結構很難被發現
* CNN，使用end to end learning，透過所有圖像使用相同的知識，這種方法獲得巨大的成功，但是他們在很多方面與人類感知不同

CNN存在的問題:

* CNN雖然對於區域特徵的描述能力很好，但是他們對以下的情況實質上處理得非常差
  + 視角轉換    
  + 旋轉
  + 剪切(放大伸縮)
  + 光照
  + 對抗性

膠囊網路，通過可查看所有部件的autoencoder，進而推斷物體膠囊的位置與姿勢

# 被激發的想法

這篇文章中作者們試圖發明一種別於CNN的特徵擷取方法，2020年Transformer也開始展開和CNN的比較，爾後是否會進入一個非CNN稱霸的神經網路世界市值得期待的，本文也清楚的點出了CNN網路的問題
