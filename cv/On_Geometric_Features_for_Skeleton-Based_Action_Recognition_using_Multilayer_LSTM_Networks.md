# On Geometric Features for Skeleton-Based Action Recognition using Multilayer LSTM Networks

[paper](http://cvlab.cse.msu.edu/pdfs/Zhang_Liu_Xiao_WACV2017.pdf)

[github](https://github.com/Sy-Zhang/Geometric-Feature-Release)

2017, IEEE, WACV, 140+

Songyang Zhang

Xiaoming Liu

Jun Xiao

# 摘要

RNN - based 的方法在基於骨架輸入的動作識別取得了出色的表現，近期(2017)，這些方法被侷限在骨架點的座標，而提升準確度的方法主要是把RNN模型用各種方法拓展到空間上(spatial domains)，不同於此類模型直接從關節座標(joint coordinates)探索不同部分的關聯，我們提出一種簡單且普遍的的空間模型，可以直接增加這些RNN模型的表現，更精確地說，在之前工作的啟發中，我們選了幾組簡單的幾何特徵(geometric features)，在一個3層的LSTM上做實驗，我們觀察到這些關節之間的基於關節以及選定線之間的距離幾何特徵(the geometric relational features based on distances bertween joints and selected lines)比起其他特徵表現得出色，並且在4個資料集中取得SOTA，並且，我們演示了第一層LSTM的input gate在sparsity weight的情況下，且輸入幾何特徵，僅需要較少量的data就可以訓練起來。

# 關鍵字

* skeleton based action recognition
