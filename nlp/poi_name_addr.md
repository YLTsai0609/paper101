# Paper Title

[POI 擷取:商家名稱辨識與地址配對之研究](http://www.aclclp.org.tw/clclp/v19n4/v19n4a1.pdf)

[github - N/A](link2)

benchmark - 

# Abstract

1. 適地性服務(Location-based Service)有多種用途，例如
   1. 行動裝置上的地點查詢 - 查詢餐廳，加油站
   2. 路線導航

2. 收集網路上包含地址網頁來建立一個具有商家名稱與地址關聯性的資料庫
3. 分析 - 商家與組織名稱上的命名一些共同特性
4. CRF模型進行NER預測

# Idea

## 自動標記來建立訓練資料

Base Data - 

1. (ground-truth $y$) - 104 求職網、愛評網、工商名錄網站 - 撰寫Parser取得大量商家名稱與地址的組合
2. ($x$) - Mapping網頁語料
3. 訓練CRF

39.6萬筆網頁

68.8萬筆商家名稱及地址組合(ground-truth)

## Uni-Labelling & Full-Labelling

以 Google Snippets 為資料來源的處理流程
不僅只用單一的商家名稱來協助標記（稱之為 UniLabeling)
是採用所用商家名稱來進行標記（稱之為 FullLabeling），其餘皆與以整個網頁為資料來
訓練資料處理流程如下所述

?????

## Creating Dataset

網頁文章常常利用結構化資訊，排版，等表達方式將文字內容傳達給使用者

將網頁內容轉成文字後，移除空白累字元，已連續三個換行符號當作分隔符號，將文字切為許多區塊(Block)

如此一來可以盡可能讓訓練樣本涵蓋商家名稱，也能有較多的非商家名稱範例(Positive and Negtive Samples)


## Preprocessing

針對原始網頁 : 

圓型括號(通常表示補充說明) : `(、（、﹙` -> `(`

非圓形括號(通常有強調的意味) : `[、{、〔、｛、〈` -> `[` 

換行符號，地址電話、時間... 等正規表示法取代成特殊的序列單元，加強邊界特徵

## 序列單元 & 標記

1. 「土地」、「阿嬤祖傳菜包肉粽仙草」- 常用詞彙
2. 「18 度 c 巧克力工坊」、「591 租屋」 - 中英數字字元交錯出現
3. 「努哇克咖啡」、「蕾克爾烘培坊」 - 音譯詞
4. 「蘆薈花園雲南食府」、「三峽歷史文物館」- 地名

Stanford Segmenter + POS Tagger 來創造特徵

BIEO 標註法

## 特徵

Outside Feature : 落在商家名稱的左右 - 無法正確判斷商家名稱，僅能提供輔助

Inside Feature : 強烈判斷資訊 - 大部分商家名稱由三個部分組成
    
    1. Real Name(真名)
    2. 產品或是服務(Service or Product)
    3. 地標性詞彙(Landmark)

燦坤3C量販店 -> 燦坤/3C/量販店 or 燦坤/3C 量販/店

麗嬰房 -> 麗/嬰/房 

嬰指的是提供兒童用品

對Ground-truth捅進統計

會、城、房、站 - 具有地標性詞彙的特徵(Landmark Feature)

建立"服務"、"產品"清單 - 例如"嬰"

<img src='../asset/poi_1.png'></img>

# Result

# Other Discussion

related paper

[基於已知名稱搜尋結果的網路實體辨識模型建立工具](https://www.aclweb.org/anthology/O15-1015.pdf)

[基於 Web 之商家景點擷取與資料庫建置](https://www.aclweb.org/anthology/O15-1018.pdf)
