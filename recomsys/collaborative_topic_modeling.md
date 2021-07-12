# Collaborative Topic Modeling for Recommending Scientific Articles

year : 2011
citation : 1658

[paper](http://www.cse.cuhk.edu.hk/irwin.king.new/_media/presentations/wangblei2011.pdf)

[code official C++](https://github.com/blei-lab/ctr))

[code - thirdparty - python](https://github.com/PreferredAI/cornac)

benchmark - CiteULike

# Abstract
combine traiditiomal collaborative filtering and probabilistic topic modeling.

It provides an interpretable latent structure foe user and items. and can form recommendations about both eexisting and newly published articles.

# Idea

## In-matrix prediction and Out-of-matrix prediction
<img src='../asset/ctm_1.png'></img>

In-matrix prediction : we can only predict the user-item ratings when the items that have been rated by at least one user in the system.

out-of-matrix-prediction : item 4 and 5 have never been rated (This is sometimes called **cold start problem**) whicn traiditional collaborative filtering algorothm cannot make predcitions.

## Recommendation by Matrix Factorization

## Probabilistic Topic Models

- used to discover a set of **topics** from a large collection of documents.
- topic distribution over terms
- interpretable low dimensional representation of documents.

LDA (latent Dirichlet allocation)

$k$ : Topics : $k=1, 2, ... K$

$j$ : itmes(articles) : $j=1,2,...J$

$N_{j}$ : words in each items(articles)

probability distribution : 


$K$ topics : $\beta = \beta_{1:K}$

articles : $w_{j}$

words(terms) : $n$

build topic model : 
For each article $w_{j}$

1. topic proportions $\theta_{j}$ ~ Dirichlet$(\alpha)$
2. For each word $n$
   1. Draw topic assignment $z_{jn}$~Mult$(\theta_{j})$
   2. Draw word $w_{jn}$ ~ Mult($\beta_{z_{jn}}$)

optimizer : variational EM

inference : variational inference

# Evaluation Procedure

# Result

# Other Discussion

[推荐系统有哪些比较好的论文？](https://www.zhihu.com/question/25566638/answer/112984019)

1. 嘗試解決冷啟動(混合user-item-rating matrix & Topic Modeling) - 至於解得好不好，要拿這些方法一起比較才準
2. 具推薦解釋性(by topic)

[Review the topic modeling from note](https://github.com/YLTsai0609/DataScience_Note/blob/master/Topic_Modeling_LDA.md)