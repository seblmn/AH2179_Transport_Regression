# AH2179_Transport_Regression
Assignment task: Regression Modeling in Transport

Bus : the model used every features except the ids (line and stop was always the same and the bus_id wasn’t relevant, no difference between busses based on the correlation matrix). Data was already cleaned, I normalized the data, removed features that didn’t add value, and split the dataset. I tuned the model using grid search and cross-validation. On the test data, the model got an RMSE of 14.65, MAE of 10.77, and R² of 0.99, showing it predicts delays very well.

Bike : I also didn’t remove much features (only ids) and chose to let the model decide itself if a feature is important or not (results shown in the feature importance graph). This time, I didn’t normalize the data as XGBoost handles perfectly non-normalized data. I also decided to split data into three categories : train, test (before June 2012) and oot (out-of-time, after June 2012) in order to see the evolution on a time period and check possible overfitting. The results show great results for both test (RMSE of 5.62, MAE of 3.26 and R² of 0.99) and oot data (RMSE of 12.43, MAE of 6.07 and R² of 0.99), even though we argue that, considering the slightly better results of the test predictions, there is a small overfitting.

I learned that XGBoost is truly powerful, especially for non linear regressions as in the bike rentals. The difference was very substantial on the second set of data. These regression techniques can be adapted for predicting passenger flows or occupancy for example.
