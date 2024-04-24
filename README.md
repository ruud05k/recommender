See analysis2.ipynb for Jupyter notebook.

Summary of findings:
Various models were explored for predicting book ratings. These included k-nearest neighbors (KNNBasic), matrix factorization (SVD and SVDpp), item-based collaborative filtering (SlopeOne), and a two-tower neural network. SVD and the two-tower neural network performed best for this dataset.

In contrast to SVD, the two-tower neural network can incorporate additional contextual features, such as user age and location. This is especially beneficial for users with limited interaction history, thus partially resolving cold start issues. Further, the neural network architecture is scalable and can easily be parallelized across multiple computational nodes, unlike SVD with its sequential nature.

Only explicit user feedback was considered, whereby the task was to predict ratings. In e-commerce environments, implicit user feedback (e.g. clicks) is much more abundant. For next steps, a dataset will be analyzed containing such implicit user feedback. This would also mean that the task would switch to predicting click-through-rate using binary cross entropy as loss function. Alternatively, the ranking could directly be predicted, for example by calculating the probability that item 1 ranks higher than item 2 (using a pair-wise ranking loss).


