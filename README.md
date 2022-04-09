# ERCOT-Real-DayAhead-Price-Prediction

My analysis and prediction of ERCOT Real Time and Day Ahead prices. ERCOT is the name of the energy grid in the state of Texas 
in the United States. Highlights include
</br>
**(1)** Using tabular data augmentation to generalize onto the test exceptionally well
</br>
**(2)** Using ideas from representation-learning to capture the dynamics of the historical data and predict prices with fewer variables
than those available to us in the historical data.

## About:
For trading in power, predicitng the Day Ahead and Real Time prices well in advance are of prime importance. Herein I do analysis
of historical data between October 2021 and March 2022 for the power grid in the state of Texas aka ERCOT.
  1) RealPrice+FullInfo.ipynb performs EDA and tries to gain model insights albeit in a hypothetical realm where true energy demand and production are known to predict the real time prices.
  2) DayAhead.ipynb uses the well performing models and techniques of RealPrice+FullInfo.ipynb to predict the less volatile Day Ahead prices
  3) RealTime+PartialInfo.ipynb uses a special technique which uses ideas from representation learning to predict the more volatile real time prices using only the forecasts. 
 The highlight is that pretraining on the historical data (which includes both the forecasts and the real demands) helps the model almost halve the MAE as compared to
 using only the forecasts to predict the real time prices in a regular train-test way.

## Disclaimer:
While the analysis has been done by me, the data is not owned by me. Hence the data is not being made public.

