# Stock-Price-Prediction-with-basic-LSTM-model
Using LSTM model to predict the stock price and checking if it's possible or feasible to do so.

## 1. Google Stock Price prediction on close price
Using basic LSTM model, trying Stock price prediction on Close price using Single-step-prediction and Multi-step-prediction.

### Losses plot
![losses](https://user-images.githubusercontent.com/88196035/134039836-b2f1e930-7d29-41e7-b98f-3128b072d233.png)

### Prediction Plot
#### a) Single-Step Prediction:-
![single-close](https://user-images.githubusercontent.com/88196035/134038226-f3102d66-dff5-4e0a-851d-57ce440c1e86.png)

#### b) Multi-Step Prediction:-
![multi-close](https://user-images.githubusercontent.com/88196035/134038283-62872afe-7cbd-4146-a56c-c04e675e13d2.png)

The two graphs generated in Single step prediction just differ by a time step, for multi-step prediction the the prediction goes to down and after a while the prediction goes to almost constant value and continue that way. For single step the prediction just approximates the last value for the original graph and gives that as prediction.


## 2. Return Prediction on Close price
Trying Return prediction on Close price using basic LSTM model on Single-step-prediction and Multi-step-prediction.

### Losses plot
![return_loss](https://user-images.githubusercontent.com/88196035/134041113-f06affc9-d594-47c1-a807-f8c8c9917963.png)

### Prediction Plot
#### a) Single-Step Prediction:-
![return_single](https://user-images.githubusercontent.com/88196035/134041924-6f412e31-f487-461d-8469-14e211d5a14f.png)

#### b) Multi-Step Prediction:-
![return_multi](https://user-images.githubusercontent.com/88196035/134041938-892d4ef2-95c6-4059-b599-c35d3dbbca5d.png)

So, Even the prediction of return is not feasible with the LSTM model. The graphs show the same trend as in the first notebook. Also, the result for the single-step prediction is even worse in this case.

## 3. Positive and Negative Return Classification.
try to classify the return value in Positive or Negative return using LSTM model but we observe that Val Accuracy is not on either extremes it is in between which is near about 50%. That states that model can not classify the positive or negative return too. 

So in total we can't predict the Stock Price or Return using LSTM only as they depend on many other factors too. It's not as easy as to just observe the pattern in them and make a future prediction.


## Time Series Generator
This class takes in a sequence of data-points gathered at equal intervals, along with time series parameters such as stride, length of history, etc., to produce batches for training/validation.

## Dataset
Data set contains all the relevant data about the Google stock from 2004 to 2020.

dataset is available into this repository as GOOGL.csv
