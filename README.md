# MoHR: Recommendation Through Mixtures of Heterogeneous Item Relationships

This is our TensorFlow implementation for the paper:

Wang-Cheng Kang, Mengting Wan, Julian McAuley. *[Recommendation Through Mixtures of Heterogeneous Item Relationships.](https://arxiv.org/pdf/1809.09739.pdf)* In Proceedings of ACM Conference on Information and Knowledge Management (CIKM'18)

Please cite our paper if you use the code or datasets.

The code is tested under a Linux desktop with TensorFlow 1.2.

## Datasets

The `Automotive` from Amazon is included in the repo. All datasets (after pre-processing) can be downloaded from:

- *[Amazon Automotive](http://cseweb.ucsd.edu/~wckang/MoHR/data/AutomotivePartitioned.npy)*
- *[Amazon Beauty](http://cseweb.ucsd.edu/~wckang/MoHR/data/BeautyPartitioned.npy)*
- *[Amazon Clothing](http://cseweb.ucsd.edu/~wckang/MoHR/data/ClothingPartitioned.npy)*
- *[Amazon Toys](http://cseweb.ucsd.edu/~wckang/MoHR/data/Toys_and_GamesPartitioned.npy)*
- *[Amazon Games](http://cseweb.ucsd.edu/~wckang/MoHR/data/Video_GamesPartitioned.npy)*
- *[Google Local](http://cseweb.ucsd.edu/~wckang/MoHR/data/GooglePartitioned.npy)*
- Steam (raw): [reviews](http://cseweb.ucsd.edu/~wckang/steam_reviews.json.gz), [game info](http://cseweb.ucsd.edu/~wckang/steam_games.json.gz)


## Model Training

A simple way to train our model is (with default hyper-parameters): 

```
python main.py --dataset=Automotive 
```

For the `Automotive` dataset, the model should be converged in 600 epochs, you should be able to see the test AUC in the log file reach 0.8.

For more details (e.g. learning rate, regularizations, etc), please refer to the code. 
