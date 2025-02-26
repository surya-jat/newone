## Data Collection Process

For our model, we used data from three batteries labeled B0005, B0006, and B0007. We extracted impedance parameters (Re and Rct) over time, along with capacity value from discharge cycle that were used to derive the actual SoH values. This provided us with a comprehensive dataset to train and validate our model.

## Correlation Analysis

While analyzing our data, we observed strong negative correlations between impedance parameters and SoH. Specifically, Re versus SoH showed a correlation of -0.85, while Rct versus SoH showed a correlation of -0.88.

These strong correlations validate our approach, confirming that increase in Re and Rct, decreases battery health. This relationship forms the foundation of our machine learning model.

## Data Processing & Model Training

Our methodology involved several steps:
1. We extracted Re and Rct values from impedance measurements
2. Used these features as inputs to our machine learning models
3. Split the data into an 80-20 train-test ratio
4. Evaluated performance using metrics like Mean Absolute Error (MAE), Root Mean Square Error (RMSE), and R-squared (R²)

We also created a heatmap showing predicted SoH across the parameter space of Re and Rct, which highlights regions of high and low SoH. This visualization helps us understand the relationship between these parameters and battery health.

## Model Performance

We evaluated several machine learning models:
- Ensemble model 
- Linear regression
- SVR
- Neural Network 

The ensemble model achieved the best performance with a Mean Absolute Error of 2.50% and an R² value of 0.87. Other models performed as follows:
- SVR: MAE = 2.58%, R² = 0.87
- Neural Network: MAE = 2.88%, R² = 0.85
- Linear Regression: MAE = 3.57%, R² = 0.77

These results demonstrate that machine learning can effectively predict SoH from impedance parameters, with our ensemble model showing particularly strong performance.

## Validation Results

To ensure our model's robustness, we validated it on unseen test data. The results were promising:
- Mean error of 3.40%
- Maximum error of 4.9%
- Error standard deviation of 3.53%

The heatmap of predicted SoH shows how our model maps the relationship between impedance parameters and battery health across different operating conditions. This validation confirms that our approach provides reliable SoH estimates across a range of scenarios.

## Nyquist Plot Evolution

First of all Nyquist plots are the way to visualize complex impedance, with the real part on the x-axis and the imaginary part on the y-axis. The semicircle patterns we see represent different electrochemical processes occurring in the battery, and their size and position change as the battery ages.

We can see how impedance changes with battery degradation. These plots clearly show the increase in Re and Rct as SoH levels decrease.



## Future Aspects

Looking ahead, we are planning for a:

hybrid models that combine time-domain data (current, voltage) with frequency-domain data (impedance), which could provide a more comprehensive degradation model.

After that, we have planned to incorporate temperature effects. We could create adaptive models that adjust for different thermal environments and cycling conditions, leading to thermal management strategies based on real-time SoH and temperature data.

And lastly, exploring full impedance spectrum and battries other impedences analysis could extract more information from EIS data and help us better understand the correlation between specific frequency ranges and different degradation mechanisms.

## Potential Impact

The advantages of our impedance-based SoH predictions are:
- It provides faster assessment compared to traditional methods
- it Enables real-time battery health monitoring in critical applications like EVs and renewable energy storage
- Offers non-invasive SoH estimation 
- Demonstrates high accuracy with robust validation results

The broader implications include:
- Reduced downtime and maintenance costs for battery systems
- Enhanced reliability and safety of energy storage systems
- Potential for integration with existing BMSs

