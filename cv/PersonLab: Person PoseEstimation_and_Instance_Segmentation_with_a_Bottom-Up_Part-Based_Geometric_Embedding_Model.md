# PersonLab: Person Pose Estimation and Instance Segmentation with a Bottom-Up, Part-Based, Geometric Embedding Model

[paper](https://arxiv.org/pdf/1803.08225.pdf)
[github](https://github.com/octiapp/KerasPersonLab)

* 2018
* citation 77+

# 摘要

我們提出了一種由下至上的方法(box-free bottom-up approach)來解決多人圖片中的人類姿態估計以及個體分割任務(the tasks of pose estimation and instance segmentation)，使用一個有效的單一模型(effiecient single-shot model)，這個模型我們稱之為PersonLab，這個模型著手於語意級分割以及部分姿態來進行建模(semantic-level reason amd object-part associations using part-based modeling)，我們的模型使用一個CNN來學習每獨立的keypoints並預測他們的位移，如此一來我們就可以把keypoints綁起來，、再組合成一個人的樣子。

進一步地說，我們提出一個幾何嵌入的描述子(a part-induced geometric embedding descriptor)來我們可以人類的語意pixel關聯起來，組合成一個人，接著產出一個instance-level的分割。

我們的系統是基於一個全卷積的架構(fully-convolutional architecture)來幫助我們有效的推論，在這樣的場景下，拍攝圖片中的人數跟效率是無關的，我們在COCO dataset上訓練，在COCO test-dev的資料級上使用single scale的推論上keypoint平均精度(average precision)達到了0.665，使用multi-scale的推論可以達0.687，這樣的成果比起先前的由下至上姿態估計(all previous bottom-up pose estimator systems)提升非常多，同時我們也是第一個在COCO dataset 人類個體分割任務，由下至上方法中，產出一個具有競爭力結果的。我們分辨人類的平均精度是0.417。

# Keywords

Person detection, pose estimation, segmentation and grouping

# 作者

George Papandreou
yler Zhu
Liang-Chieh Chen
Spyros Gidaris
Jonathan Tompson
Kevin Murphy
