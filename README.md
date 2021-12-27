# UVA_AML_food21 - Flight delay prediction challenge repo on Kaggle for group 7

This challenge focuses on predicting flight delays. 

## Challenge

The goal in this challenge is to predict the flight delays. 

You should predict ARRIVAL_DELAY columns. Here there are explanations for some data rows: 

*   YEAR, MONTH, DAY, DAYOFWEEK: dates of the flight. 
*   AIRLINE: An identification number assigned by US DOT to identify a unique airline. 
*   ORIGINAIRPORT, DESTINATIONAIRPORT: code attributed by IATA to identify the airports. 
*   SCHEDULEDDEPARTURE, SCHEDULEDARRIVAL: scheduled times of take-off and landing.
*   Pariticipants have to submit their trained model along with trained weights. Immediately after the submission the AICrowd Grader picks up the submitted model and produces inference on the private test set using Cloud GPUs.
*   DEPARTURE_TIME: real times at which take-off took place.
*   DISTANCE: distance (in miles).

Submissions are evaluated using Mean Squared Error(MSE). For each row and id, you must submit your ARRIVAL_DELAY prediction. The formula is then:

<img src="https://render.githubusercontent.com/render/math?math=MSE=\frac{1}{N}\Sigma_{i=0}^{N-1}({delay_i}-\hat{delay_i})^2">

, where N is the number of rows in the test set, <img src="https://render.githubusercontent.com/render/math?math={delay_i}"> is the true ARRIVAL_DELAY for the i-th row, and <img src="https://render.githubusercontent.com/render/math?math=\hat{delay_i}"> is the predicted ARRIVAL_DELAY.

Your overall score should be at least around 0.0125, which is similar to assigning random labels to the images.

### Submission Format
You must submit a csv file with an id and name and the predicted ARRIVAL_DELAY. The file must have a header and should look like the following:

id,ARRIVAL_DELAY <br>
0, 1.0 <br> 
1, 2.5 <br> 
2, 5.0 <br>
... <br>
etc

## Data description

The dataset consists of 2325706 rows in the training set and 492847 rows for the test set.

### File descriptions

*   airlines.csv - extra description of airlines.
*   airports.csv - extra description of airports.
*   flights_test.csv - the training set with 2325706 rows.
*   flights_train.csv - the test set with 492847 rows.
*   submit_sample.csv - a sample for the submission file.
