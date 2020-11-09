# Personalized_Activity_Recognition_with_Deep_Triplet_Embeddings

[paper](https://arxiv.org/abs/2001.05517)

year : 2020

# Authors

# 導讀
在基於慣性感測器的人類行為識別運動中(inertial human activity recognition)使用監督式學習有一項極大的挑戰，也就是不同個體的同樣動作(heterogeneity of data between individual users)，在一些非個人化的演算法中有著不好的成績，我們基於一個全卷積神經網路提出一種個人化的行為識別方法，我們針對categorical cross entropy以及triplet loss進行了實驗，並基於不同的個體，我們建立了一種新的triplet loss function，並且在公開的人體姿態識別資料集(MHEALTH, WISDM, SPAR)比較準確率，分佈外的行為偵測，embedding在新的動作上的generalization，新的subject triplet loss有著最好的表現

# 被激發的想法

這裡的三個資料集都是sensor-based的資料，和2D畫面資料比起來，不同的動作容易產生更大的inter-class variance

摘要中提到的OOD(out-of-distribution)的task，在文獻中可以多加關注
