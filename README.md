# COST_lecture

This project contains Python notebooks to generate chemistry learning data and learn ML models on simple 0D homogeneous reactors problems. These reactors are here computed using the *CANTERA* software. The objective is to replace the call to the CVODE solver used in *CANTERA* with an Artificial Neural Network (ANN).

Description of notebooks:

+ *0D_database_generation.ipynb*: in this notebook we generate a database of 0D reactors (at identical pressure), and process them to build a training database for ML models. It includes the pre-processing of the data: scaling and potentially logarithm transform of the data.

+ *0D_ann_learning.ipynb*: in this notebook we train and test neural networks to replace the CVODE solver for 0D reactors computations. The notebook is split in two main parts:
    - Learning of a baseline model
    - Learning of a model with soft physical constraints

+ *0D_database_clustering.ipynb*: In this notebook we illustrate the clustering of a database generated in the notebook *0D_database_generation.ipynb* based on the K-Means algorithm from the scikit-learn library.