# Dynamic pricing strategy.

![Dynamic](https://github.com/Kamuthuj/Dynamic-pricing/assets/121629618/e0bb5bfc-7f30-4c21-b198-d22fb4dbef5f)

In this dynamic pricing strategy, I aimed to maximize revenue and profitability  at the right level that balances supply and demand dynamics.Using the dataset I obtained from Kaggle, I loaded it and performed data cleaning and several ETL processess. I was keen in observing features that would affect pricing and created a correlation matrix to observe the strength of different features. Features that had strong correlation inclueded ride duration, historical cost of ride, and also the number of riders and drivers.

![Correlation matrix](https://github.com/Kamuthuj/Dynamic-pricing/assets/121629618/e10301d8-c9ff-4893-9b0e-bd53a0ec336a)


I later implemented the dynamic pricing, to adjust ride cost dynamically based on demand and supply levels.This will capture high demand periods and low supply scenarios to increase prices, while low demand periods and high supply situations will lead to price reductions.I calculated the adjusted ride cost for dynamic pricing where it multiplied the historical cost of the ride by the maximum of the demand multiplier and a lower threshold,and also by the maximum of the supply multiplier and an upper threshold.This multiplication ensured that the adjusted ride cost captures the combined effect of demand and supply multipliers, with the thresholds serving as caps or floors to control the price adjustments.

![Ride profitability (Dynamic vs historical)](https://github.com/Kamuthuj/Dynamic-pricing/assets/121629618/8257ed65-ed6a-4e50-9002-0db7cf441398)

I preprocessed the data using a standard scaler, and dealt with outliers within the data. I also dealt with numerical missing data by filling with mean and categorical by mode. I used the decision tree regressor for model prediction to get the actual values and the predicted values.

![Actuals vs predictions](https://github.com/Kamuthuj/Dynamic-pricing/assets/121629618/ba2877e7-3c61-48f5-b81d-8e966cb2cb3d)
