# Make Skeleton-based Action Recognition Model Smaller, Faster and Better

[paper](https://arxiv.org/pdf/1907.09658.pdf)
[github](https://github.com/fandulu/DD-Net)
2019
Fan Yang Nara Institute of Science and Technology
Sakriani Sakti1 RIKEN, AIP, Japan
Yang Wu  Kyoto University, Japan
Satoshi Nakamura Institute of Science and Technology

# 摘要

雖然基於骨架的動作識別在近年來已經取得成功，但現有的方法要馬模型太大，要馬推論太慢，為了解決這個問題，我們分析了骨架序列並提出雙特徵雙運動網路(Double feature Double motion Network, DD-Net)，透過這個輕量級的網路架構(0.15百萬的參數量)，DD-Net可以達到非常快的速度，在單GPU上達到3500FPS，單CPU上2000FPS，透過利用強健的特徵，DD-Net在**SHREC**(3d hand actions)以及**JHMDB**(body actions)達到SOTA，我們的code放在[這裏](https://github.com/fandulu/DD-Net)

# 關鍵字

* skeleton based action recognition, Body Actions, Hand Gestures

# 主要想法

在真實世界的應用場景中，skeletion-based model由於input data小，不像圖像資料raw data的數量一大堆，應該能夠用少量的參數達到足夠好的效果，因此我們調查了骨架序列的性質來提出DD-Net，該架構串流了Joint Collection Disatnace(JCD)特徵以及一個雙尺度運動特徵(two-scale global motion feature)

1. JCD特徵可以對位置視點變化(location-viewpoint variation)更強健
2. motion scale在不同的scale之下有不同的效果，time down sampling[1]
3. 分別彼此強相關的關節點以及弱相關性的

為了克服以上特性，先前的工作提出了較為複雜的網路結構，這導致了較大的模型尺寸
相反地，我們將滿足以上特性的架構拆分為兩個部分，input feature以及network，JCD特徵能夠達成位置視角不變性(location-viewpoint invariant)，與其他的簡單特徵比較，他非常容易計算，而且參數量少，因為global motion無法被JCD特徵捕捉，我們引述了一個雙尺度的運動特徵來增強DD-Net的泛用性
該雙尺度結構讓我們能夠對motion scale具有強健性
經過了embedding的過程，DD-Net可以自動地學到適當地**關節相關性**，這點較難在特徵工程上直接做出

比起其他較為複雜的網路模型，DD-Net在我們的實驗資料及上有著更好的generalization，不論是效率上還是準確度上，DD-Net非常適合拿到現實應用場景中
有參考Fusing geometric features for skeleton-based action recognition using multilayer lstm networks

# 被激發的想法

1. 根據我們之前的簡報，沒有做downsampling的序列行為資料noise過多，可能是導致模型overfitting的原因
