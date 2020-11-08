# Digging Into Self-Supervised Monocular Depth Estimation

# 摘要
若要取得規模化的取得pixel level的深度圖標籤(ground-truth depth data)是一件非常具有挑戰性的事，為了克服這個限制
self-supervised learning可以幫上大忙，在這篇文章中，我們提出的幾項改善，我們的結果不論是定性地還是定量地都改善了深度圖的自監督方法(self-supervised methods)，自監督的單相機訓練通常使用超複雜的網路結構，損失函數，以及圖像模型(image formation models)，上面提到的這些都有助於彌補監督方法的不足，我們要向大家展示一個簡單的模型，以及幾個特別的設計，幫助我們達成預測上的改善，我們提出以下三項設計

1. 最小在投影損失(a minimum reprojection loss)，這項設計是用於更強健的處理遮擋
2. 全解析度的多尺度採樣(a full-resolution multi-scale smapling)，用於減少視覺偽影(visual artifacts)
3. 自動遮罩損失(an auto-masking loss)，用此來忽略那些違反相機運動假設的訓練像素(ignore training pixels that violate camera motion assumptions)

我們個別展示了上面三樣設計的有效性，而且在KITTI資料及上展現了當前最好的結果。

# 其他導讀

https://zhuanlan.zhihu.com/p/70651836

# Demo Video

https://www.youtube.com/watch?v=sIN1Tp3wIbQ
