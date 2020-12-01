# Factorization Machines

[paper](https://www.csie.ntu.edu.tw/~b97053/paper/Rendle2010FM.pdf)

[github pyFM](https://github.com/coreylynch/pyFM)

[github tffm](https://github.com/geffy/tffm)

It has been a while, the paper is published on 2010.

# abstract

1. combine the advantages of SVM with factorlizationm models
2. FM model all interactions between variables using factorized parameters.
3. FM is able to estimate interactions with huge sparsity.
4. FM can be calculated in linear time.
5. FM can easily apply without expert knowledge.
6. FM can mimic these models(matrix factorization, parallel factor analysis or specialized models like SVD++, PITF, FPMC)

# idea

## describe the problem

### regression and clasfication

prediction / label 

$y : \R^{n} \rarr T$

target domain :  $T$

regression 
$T = \R$ 

classification

$T = \{+, -\}$

training dataset $D = \{(x^{(1)}, y^{(1)}), \{(x^{(2)}, y^{(2)}), ...\}$

feature vector from real value 

$X \in R^{n}$

## ranking

target domain $T = R$

pairwise training data 

e.g.

feature tuple $(x^{(A)}, x^{(B)}) \in D$ means $x^{(A)}$ should be randked higher than $x^{(B)}$ 

Though the pairwise ranking relation is antisysmmetric, it is sufficient to use only positive training instances.

## sparse data

$X$ is highly sparse. Almost all of the elements $x_{i}$ of a vector $x$ are zero.

$m(x)$ - the number of non-zero elements in the feature vector $x$.

$\bar{m}_{D}$ - the average nunmber of non-zero elements $m(x)$ of all vectors $x \in D$.

huge sparsity ($\bar{m}_D << n$)

1. event transactions
2. purchases in recommender systems
3. text analysis(bag of word approach)

basically, large categorical variable domains.

## Example

movie review system 

user $u \in U$ rates a movie(item) $i \in I$ at a certian time $t \in \R$ with a rating $r \in \{1, 2, 3, 4, 5\}$. Let users $U$ and items $I$ be :

$U=$ {Alice(A), Bob(B), Charlie (C), ...}

$I=$ {Titanic(Ti), Notting Hill(NH), Star Wars (SW), Star Trek(ST), ...}

observed data $S$ : 

$S$ = {(A, TI, 2010-1, 5), (A, NH, 2010-2, 3), (A, SW, 2010-4, 1), 
(B, SW, 2009-5, 4), (B, ST, 2009-8, 5), 
(C, TI, 2009-9, 1), (C, SW, 2009-12, 5)}

# other-discussion
