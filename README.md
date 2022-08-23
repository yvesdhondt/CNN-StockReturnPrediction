# Predicting Stock Returns Through CNN

This repository explores whether stock returns can be accurately predicted based on CNN image classification.

# Code location

All code is located in the /stock_return_cnn folder.

# Necessary packages

The following packages are required to run all the code from this repository:

- pandas
- os
- PIL
- matplotlib
- random
- datetime
- gc
- pyts (to construct the GADF images)
- numpy
- optuna (to perform the hpo)
- torch (the models are trained using the Pytorch framework)
- torchvision
- pickle (to save intermediare results)
- sklearn (for the benchmark model)

# Data

The data used for this project is made available under CC0 and can be found at: https://www.kaggle.com/datasets/borismarjanovic/price-volume-data-for-all-us-stocks-etfs

To ensure that the project runs correctly, download the data from the above link and populate the `stock_return_cnn/Data` folder so that it contains the `ETFs` and `Stocks` folders from the downloaded data.

# Sample Data

The notebooks are numbered in the order that they should be executed. Notebooks 0 and 1 have to do with turning the raw data into image files and performing some basic EDA. As this is a step that takes a lot of time (depending on the machine a few hours to a full day), a folder with already processed images is provided.

- The folder "ModelData", contains the .csv files that outline where the train, test, & validation data can be found as well as the labels.
- The folder "stock_return_cnn/SampleData.zip", contains all the area chart and GADF image files. If you decide to skip over running notebooks 0 & 1 than you simply have to **UNZIP AND THEN RENAME /SampleData to /Charts** and then you should be able to run notebooks 2 and beyond without issue.

# Hyperparameter Tuning

Notebooks 2_a and 2_b contain the code for the hyperparameter tuning. Again, this code takes a long time to run (On my machine it took around 12 hours). Therefore, these notebooks can be skipped as the result of the hyperparameter tuning is already incorporated into notebooks 3_a and 3_b.

# Model Training

Notebooks 3_a and 3_b contain the code to train the final area chart and GADF image models and perform some analysis on the trianing and results.

# Benchmark Model Training

Lastly, notebook 4 contains the code to train the benchmark model.