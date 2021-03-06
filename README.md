# RecoTour

This repo intends to be a tour through some recommendation algorithms in
python using various dataset.

At the moment there is only one dataset, the
[Ponpare](https://www.kaggle.com/c/coupon-purchase-prediction) coupon dataset,
which corresponds to a coupon purchase prediction competition at Kaggle (i.e.
recommending coupons to customers).

**The core of the repo are the notebooks** in the  `Ponpare` directory. They
intend to be self-contained and in consequence, there is some of code
repetition. The code is, of course, "notebook-oriented". In the future I will
include a more modular, nicer version of the code in the directory
`py_scrips`. If you look at it now it might burn your eyes (you are warned, I
would not go there).

**UPDATE 1 (30-08-2018)**: I have included a more modular (nicer looking) version of a
possible final solution (described in
`Chapter16_final_solution_Recommendations.ipynb`) in the directory
`final_recommendations`.


The notebooks have plenty of explanations and references
to relevant papers or packages. My intention was to focus on the code, but you
will also find some math.

All the code in the notebooks has run on a **c5.4xlarge** instance or a **p2.xlarge** instance when running deep learning algorithms.

This is what you will find in the notebooks:

1. Data processing, with a deep dive into feature engineering
2. Most Popular recommendations (the baseline)
3. Item-User similarity based recommendations
4. kNN Collaborative Filtering recommendations
5. GBM based recommendations using `lightGBM` with a tutorial on how to optimize gbms
6. Non-Negative Matrix Factorization recommendations
7. Factorization Machines recommendations using `xlearn`
8. Field Aware Factorization Machines recommendations using `xlearn`
9. Deep Learning based recommendations (Wide and Deep) using `pytorch`
10. Neural Collaborative Filtering using the movielens dataset can be found in a companion [repo](https://github.com/jrzaurin/neural_cf)

I have included a notebook with what it could be a good solution for this
problem in "the real word".

So, where do we go from here? These are some of the things I intend to include
when I have the time:

### Datasets

1. The [Amazon Product Data](http://jmcauley.ucsd.edu/data/amazon/) dataset (or well, a fraction of it)
2. Other datasets that are better suited for Deep Learning based algorithms,
containing text, images if possible and user behavior.

### Algorithms

1. Graph based recommendation algorithms
2. [Neural Collaborative Filtering](https://www.comp.nus.edu.sg/~xiangnan/papers/ncf.pdf)

	**UPDATE: 17-10-2018:** Neural collaborative Filtering has been added in a companion [repo](https://github.com/jrzaurin/neural_cf).

3. [Sequence based recommendation algorithms](https://florianwilhelm.info/2018/08/multiplicative_LSTM_for_sequence_based_recos/)
4. Others...

### Miscellaneous

1. Illustration of how to use other evaluation metrics apart from the one
shown in the notebooks ( the mean average precision or MAP) such as the
Normalized Discounted Cumulative Gain
([NDCG](https://en.wikipedia.org/wiki/Discounted_cumulative_gain)).

	**UPDATE 2 (21-09-2018)**: I have included a script called `using_ncdg.py` in the directory `py_scripts` that is intended to illustrate how one would use NDCG for the Ponpare Problem.

I hope the code here is useful to someone. If you have any idea on how to improve the content of the repo, or you want to contribute, let me know.