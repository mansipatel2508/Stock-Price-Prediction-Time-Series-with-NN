# Stock-Price-Prediction-Time-Series-with-NN

# Stock Price Prediction using NN,LSTM & CNN
The project predicts the closing stock price based on the last 7 days' data includes opening stock price, highest stock price of the day, lowest stock price of the day, stock volume and closing stock price.
# 1.Problem Statement
This project aims handle the sequential data of stock market, predicting the closing stock pride every 7 days calculating previously sequential values into account towards predicting the every 7th record in the sequential dataset.

**Time Series Dataset | Closing Stock Price Prediction | Sequential Data as Image Representation | Regression Chart**

Models : Fully-Connected Neural Networks (FCNN) | Convolutional Neural Networks (CNN) | Long Short Term Memory (LSTM)

Project attemps to learn:
* Applying and comparing FCNN,CNN & LSTM to Time series data
* Visualizing the output feature - closing stock prices
* Visualizing sequential data to 4D image to feed in the CNN model
* Visualizing sequential data to 3D image to feed in the LSTM model
* Parameter tuning all the models to get the best results
* Regression Chart or Lift Chart
* Previous N days' best value
* Applying Bi-directional LSTM model 
* Applying best models got for totally another sequential dataset - google company's stock prediction

# 2. Dataset
The dataset has following 7 features:
Date, Open, High, Low, Close, Adj_Close, Volume

* Removed date and adj_close columns, not using them for prediction
* Preprocessed the data, dropped the rows with null values, unnecessary columns
* Normalized numeric data with zscore normalization
* Normalized the output features as seperate column while used the same which fed as train_y and y_true
# Data Visualization
* The flow of value of closing stock price which we intend to predict
![](https://github.com/mansipatel2508/Stock-Price-Prediction-Time-Series-with-NN/blob/master/Images/Visual.png)
# Neural models
## FCNN
![](https://github.com/mansipatel2508/Stock-Price-Prediction-Time-Series-with-NN/blob/master/Images/FCNN.png)
![](https://github.com/mansipatel2508/Stock-Price-Prediction-Time-Series-with-NN/blob/master/Images/FCNN1.png)

## LSTM
![](https://github.com/mansipatel2508/Stock-Price-Prediction-Time-Series-with-NN/blob/master/Images/LSTM.png)
![](https://github.com/mansipatel2508/Stock-Price-Prediction-Time-Series-with-NN/blob/master/Images/LSTM1.png)

## CNN
![](https://github.com/mansipatel2508/Stock-Price-Prediction-Time-Series-with-NN/blob/master/Images/CNN.png)
![](https://github.com/mansipatel2508/Stock-Price-Prediction-Time-Series-with-NN/blob/master/Images/CNN1.png)

# Comparison
![](https://github.com/mansipatel2508/Stock-Price-Prediction-Time-Series-with-NN/blob/master/Images/Comp.png)

# 1.Best value of N
## LSTM
![](https://github.com/mansipatel2508/Stock-Price-Prediction-Time-Series-with-NN/blob/master/Images/BestLSTM.png)

## CNN
![](https://github.com/mansipatel2508/Stock-Price-Prediction-Time-Series-with-NN/blob/master/Images/BestCNN.png)

# 2.Bidirectional LSTM Model
* Tried with different layers and parameter tuning but end up with more RMSE than the regular LSTM
* Observed that the less layers has relatively less RMSE than the deep layer Bidirectional LSTM
* Did not work for this problem

RMSE : LSTM - 3.006859064102173  **|** Bidirectional LSTM -  4.965034008026123
# 3.Best Models applying to different dataset (Google)

* Prior performing best FCNN,CNN & LSTM models applying for another dataset to observe the results  
## RMSE

FCNN - 4.5739

LSTM -  52.1711

CNN - 18.1740

# Conclusion
* Different dataset may have different time series flow causes applying different models on that particular dataset, not the best models for likewise dataset.
* Bidirectional LSTM should have worked well with time series although the performance increases by minor error rate, need to observe more combinations with it.
* As we considering previous N days' data to predict the next closing stock value for CNN & LSTM, same approach should have been applied to FCNN to get the fair result, although in this project FCNN beats the others from the first place.

Mini Project 4

Mansi Patel

March 27, 2019

Prof: H.Chen

CSC 215 
