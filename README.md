
# Waves Prediction


The purpose of this project was to predict wave data from measured/calculated wave parameters collected by oceanographic wave measuring buoys anchored at Mooloolaba, [Kaggle](https://www.kaggle.com/datasets/jolasa/waves-measuring-buoys-data-mooloolaba). Preprocessing of the data was conducted to clean and prepare the data for model training. In this case, the model used was a Gated Recurrent Units (GRU) model, which enables capturing patterns across time series of the wave parameters.

The dataset features include:

- Date/Time: Date and time of the record. 
- Hs: Significant wave height, an average of the highest third of the waves in a record.
- Hmax: The maximum wave height in the record.
- Tz: The zero upcrossing wave period.
- Tp: The peak energy wave period.
- Peak Direction: Direction (related to true north) from which the peak period waves are coming from.
- SST: Approximation of sea surface temperature.


![Waves](/Images/dataset-cover.jpg "Waves")


## Methods Used

 - Machine Learning
 - Predictive Modeling
 - Data Visualization
 - Deep Learning


## Technologies

- Python3
- Numpy
- Pandas
- Seaborn
- Missingno
- Keras


## Needs of this project

- Data processing/cleaning
- Data exploration/descriptive statistics
- Statistical modeling

## Conclusions

In the first place, we observe that the GRU model exhibits lower mean absolute error compared to the other two models for the training data. Which justifies the addition of complexity to the model, because present a notorious benefit to the predictions.

On the other hand, for the test dataset, the GRU model also shows a lower mean absolute error for almost all features. However, for the feature related to surface water temperature, the GRU model exhibits a higher mean absolute error compared with the other models.

In conclusion, the best-performing model considering mean absolute error is the GRU model, which outperforms the basic models used as baselines. The only detail of the model is the feature related to surface water temperature, where it performs worse compared to the other two models.

![Predictions](/Images/Prediction_Test.png "Predictions")


## Challenges

One of the challenges of this project was handling the data, as dealing with time series required splitting multiple observations in order to predict a certain number of future timesteps.

Another significant challenge was selecting the best parameters for the GRU model, as minor modifications to these parameters resulted in significant differences in training and validation errors. Therefore, a significant portion of the work time was dedicated to this process.


## What else i might have done?

Another aspect I would have addressed is finding a way to recover or replace the spurious data. Because, in this case they represent only 0.63% of the dataset, but in futures works, these data points may be significant. Therefore, it could be useful to develop strategies for replacing these data points.


## Authors

- [@JavierValladaresCo](https://www.github.com/JavierValladaresCo)


