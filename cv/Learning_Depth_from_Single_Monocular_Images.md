# Learning_Depth_from_Single_Monocular_Images

[paper](https://proceedings.neurips.cc/paper/2005/file/17d8da815fa21c57af9829fb0a869602-Paper.pdf)

[github]

Ashutosh Saxena, Sung H. Chung, and Andrew Y. Ng

2006

# 摘要

考慮的單相機的深度估計，我們試著用監督式學習，對此我們收集了ground truth(多半是一些戶外環境，像是森林，樹，建築物等等)，groud-truth則是深度圖(depthmaps)
接著我們使用監督是學習來預測深度圖，input是一張圖片，output是一張深度圖，深度估計是一個非常具有挑戰性的問題(2006)，因為區域性特徵(像是一個點)，對於深度估計基本上無法提供足夠的資訊，，因此必須考慮整張圖的內容，我們的模型是使用一個Markov Random Field(MRF)來抓取多尺度的區域特徵以及整張圖片的全局特徵( Our model uses a discriminatively-trained
Markov Random Field (MRF) that incorporates multiscale local- and
global-image features)
並且，(and models both depths at individual points as
well as the relation between depths at different points.)，我們證明了即使在非結構場景中，我們的算法也經常能夠恢復相當準確的深度圖。

# 關鍵字

1. 手工圖像特徵 :  

   *  local feature : texture variations, texture gradients, and haze.
   *  global feature : occlusion relationships

2. MRF Model
3. jointly Gaussian MRF
4. Laplacian model
5. 3-D laser scanner for collecting images and their corresponding **depthmaps**
6. SICK 1-D Laser
