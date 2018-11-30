Comparison of Three Recommender Systems on Goodreads Dataset
Jay Shi, William Su
-------------------------------------------------------------

Here's a guide to help you navigate through our files:

1. To understand and visualize our data, go to EDA.ipynb

2. To understand how we loaded and cleaned our raw data go to
    a) Folder: ExtractingMatrices
        - the extractThreeMatrices.ipynb notebook will show you how we
          converted a goodreads_interactions_fantasy_paranormal.csv file data
          into three sparse matrices
    b) Folder: ShrinkMatrices
        - the shrinkThreeMatricies.ipynb notebook will show you how 
          we shrunk our original 3 sparse matrices
        - we decided to shrink the matrices because they were too large
          and took too much computing power to run
          
3. To understand how we built and swept parameters for our UserUser model go to
    a) Folder: 
    
    
4. To understand how we built our neural network-based matrix factorization model go to
    a) Folder: NeuralNetworkModel
        - the nn_factorization.ipynb notebook will walk you through how the model is built
        - nn_history is the data of a model that we built
            - we use this in our EDA notebook to visualize the model and data
        - nn_model is a model we saved from one of the nn-based matrix model that we built
             - we use this in our EDA notebook to visualize the model and data
        