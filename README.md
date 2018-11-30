Comparison of Three Recommender Systems on Goodreads Dataset
-------------------------------------------------------------
Jay Shi, William Su

Here's a guide to help you navigate through our files:

1. To understand and visualize our data, go to EDA.ipynb. There we perform a number of tasks including:
    1. Understanding the data (after cleaning and shrinking)
    2. Visualizing the three models through different plots
    3. Comparing all the models' MSE performance together

2. To understand how we loaded and cleaned our raw data go to：
    1. Folder: ExtractingMatrices
        - the extractThreeMatrices.ipynb notebook will show you how we
          converted a goodreads_interactions_fantasy_paranormal.csv file data
          into three sparse matrices
    2. Folder: ShrinkMatrices
        - the shrinkThreeMatricies.ipynb notebook will show you how
          we shrunk our original 3 sparse matrices
        - we decided to shrink the matrices because they were too large
          and took too much computing power to run

3. For UserUser model, go to
    1. Folder: UserUserModel
        - the sweepUserUSer.ipynb notebook will show you how we build our weighted
          user-user model and also how we swept through the parameters w1 and w2
        - user_user_sweep1.json ~ user_user_sweep7.json contains json of key (w1, w2)
          mapped to test_data MSE's

4. For MatrixFactorization model go to:
    1. Folder: MatrixFactorizationModel
        - the sweep_params_matrix_fact.ipynb notebook will show you how we built the
          matrix factorizaton model based on a UV decomposition and alternating least squares
          and show you how we swept through the parameters K and reg
        - matrix_factorization_all_params.json contains a json of key (K, reg) mapped to
          train_data MSE's and test_data MSE's
        - best_param_50_niter.npy contains a numpy array that contains test_data MSE from iteration 1
          to iteration 50 using the best tuned K, reg pair we found from matrix_factorization_all_params.json

5.  To understand how we built our neural network-based matrix factorization model go to
    1. Folder: NeuralNetworkModel
        - the nn_factorization.ipynb notebook will walk you through how the model is built
        - nn_history is the data of a model that we built
            - we use this in our EDA notebook to visualize the model and data
        - nn_model is a model we saved from one of the nn-based matrix model that we built
             - we use this in our EDA notebook to visualize the model and data
