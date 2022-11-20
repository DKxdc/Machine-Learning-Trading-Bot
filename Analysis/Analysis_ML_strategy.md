## Initial Model (4/100 rolling windows, 3 month training data)

The initial model utilized a 4 period short window and 100 period long window. The data used to train the model was a 3 month period. The overall accuracy of the model was only 0.55 and as we can see in the image below, the strategy slightly overperformed against the actual returns. The stragies retuurns accumalated to a 50.8% increase over the time period whereas the actual returns were a 41.8% increase, therefore roughly a 9% outperformance using the strategy.

![SVC_model_initial](https://user-images.githubusercontent.com/109942609/202880632-669832cc-9ac9-462d-8f76-18853b3eded7.png)


## Longer Training Set (4/100 rolling windows, 12 month training data)

In order to try make the model more accurate, the training dataset was increased from a 3 month period to a 12 month period. Both the short and long windows stayed at the values used in the initial model (4 & 100 respectively). The accuracy of the model improved slightly to 0.56. The strategy actually performed the exact same as the actual returns with a 56.8% increase for both.

![SVC_model_12month_offset](https://user-images.githubusercontent.com/109942609/202880646-bf6d6a57-8d92-49f3-ad9f-4f9cf7fc9229.png)


## Longer Rolling Windows (50/200 rolling windows, 3 month training data)

In this model, the values of the short and long rolling windows were changed to 50 and 200 respectively. The training dataset was reverted back to the inital models value of 3 months. 
The accuracy of the model decreased to 0.54, and the strategy underperformed against the actual returns by 8.1%

![SVC_model_50_200MA](https://user-images.githubusercontent.com/109942609/202880651-de10e85b-ceaa-4cc2-a138-67e3d7f9ee6e.png)


## Longer Rolling Windows and Training Set (50/200 rolling windows, 12 month training data)

This model uses a 12 month training set, with a 50 period short window and 200 period long window. The accuracy of the model decreased to 0.49 - the most innacurate model out of all 4. The strategy actually returned 59.7% over the time period, although it was underperforming the actual returns for most of the time. From the image below, we might infer that this strategy does very well during high volatility periods such as teh COVID-19 2020 crash, as we see the strategy provide massive gains whilst the actaul returns performance plummets.

![SVC_model_50_200MA_12month_offset](https://user-images.githubusercontent.com/109942609/202880658-a0d8919e-9866-4adc-b8d3-35ac59db158b.png)


## Logistic Regression Model

In this section, the strategy was re run, but this time using a Logistic Regression Model, rather than SVC. The windows and training data period was reset to the values used in the Initial Model.
The accuracy of the model comes out to 0.52 and the total return of the strategy is a 23.1% increase, compared to the actual return gain of 41.9%. Whilst this model still provides some gains, the initial SVC model wouuld be better to use as it has greater accuracy, a greater return and also outperforms the benchmark actual returns.

![Logistic_model_strategy](https://user-images.githubusercontent.com/109942609/202880663-e8fa9327-3737-44b6-9137-bcb489dd9b39.png)

