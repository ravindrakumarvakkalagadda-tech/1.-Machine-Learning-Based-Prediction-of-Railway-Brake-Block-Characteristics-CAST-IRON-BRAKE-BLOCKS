Machine Learning-Based Prediction of Cast Iron Railway Wheel Brake Blocks Characteristics
1. Project Overview
This project explores the application of Machine Learning (ML) techniques to analyse and predict the friction coefficient of cast iron railway brake blocks under different braking conditions (Brake load, wheel tread speed and initial braking speeds).
The frictional behaviour of railway brake blocks is influenced by several operating parameters, including brake load, wheel tread speed and initial braking speed. Understanding the relationship between these parameters and the friction coefficient is important for evaluating braking performance and to use the model in developing a train running model. 
The present work develops a non-linear regression model using Polynomial Ridge Regression to establish the relationship between braking parameters and the friction coefficient of cast iron brake blocks.
The project demonstrates the integration of mechanical engineering knowledge, experimental data interpretation and machine learning techniques for a practical railway engineering application.
The experimental results were taken from own publication of the Author M R K Vakkalagadda et. al. (2015) from Vakkalagadda, M. R. K., Srivastava, D. K., Mishra, A., & Racherla, V. (2015). Performance analyses of brake blocks used by Indian Railways. Wear, 328–329, 64–76. https://doi.org/10.1016/j.wear.2015.01.044. These were experimental results of brake blocks under dry conditions. 
2. Engineering Background and Problem Definition
Railway brake blocks play an important role in railway braking systems by generating friction against the wheel tread during braking.
The coefficient of friction between the brake block and wheel tread is not constant. It varies with operating conditions, particularly (i) Brake load applied to the brake block, (ii) Instantaneous wheel tread speed, (iii) Initial braking speed and (iii) Reduction in speed during the braking process.
The objective of this project is to develop a machine learning model capable of estimating the friction coefficient based on these braking parameters.
Target variable:
•	Friction coefficient (μb)
Input variables:
•	Brake load (kN)
•	Tread speed (km/h)
•	Initial braking speed (km/h)
•	Speed reduction (km/h)
3. Dataset Description
The dataset contains 170 observations representing the frictional behaviour of cast iron railway brake blocks under different braking conditions.
These experimental results were taken from own publication of the Author M R K Vakkalagadda et. al. (2015) from Vakkalagadda, M. R. K., Srivastava, D. K., Mishra, A., & Racherla, V. (2015). Performance analyses of brake blocks used by Indian Railways. Wear, 328–329, 64–76. https://doi.org/10.1016/j.wear.2015.01.044. These were experimental results of brake blocks under dry conditions. 
Operating conditions considered:
•	Brake loads: 25, 30 and 35 kN per brake block.
•	Initial braking speeds: 50, 80, 120 and 140 km/h.
•	Target response: Friction coefficient (μb).
(i) A separate experimental condition involving 35 kN brake load after 20 minutes of drag braking was excluded from the main dataset because it represents a different operating condition, only stop braking situations are included. 
(ii) Sliding distance and braking time were not included because corresponding data were unavailable.
4. Machine Learning Methodology
Polynomial Ridge Regression was selected to capture the non-linear relationship between braking parameters and the friction coefficient.
 

5. Model Performance and Results
5.1 Calibration Performance
The fourth-degree Polynomial Ridge Regression model was trained using all 170 observations.
The resulting in-sample calibration performance was:
Performance metric	Value
R²	0.9900
MAE	0.0054
RMSE	0.0069
These results indicate a close agreement between the experimental digitised observations and the model predictions on the calibration dataset.
5.3 Visualisation
The project includes a calibration figure comparing digitised observations with predicted friction coefficient curves for:
•	Initial braking speeds of 50, 80, 120 and 140 km/h.
•	Brake loads of 25, 30 and 35 kN.
The figure provides a visual representation of the non-linear frictional behaviour captured by the regression model.
 
6. Limitations of the Study
The following limitations should be considered when interpreting the results:
1. A separate experimental condition involving 35 kN brake load after 20 minutes of dragging was excluded from the main dataset because it represents a different operating condition.
2. Sliding distance and braking time were not included because corresponding data were unavailable.
7. Future Scope
The following extensions are proposed to improve the reliability and applicability of the model:
•	Development of a larger dataset using  experimental measurements.
•	Investigation of additional machine learning algorithms, including Random Forest, Support Vector Regression, Gradient Boosting and Artificial Neural Networks.
•	Comparison of three-input and four-input formulations to assess the influence of mathematically dependent variables.
•	Hyperparameter optimisation and systematic model selection.
•	Further validation using independent experimental datasets.
•	Residual analysis and uncertainty quantification.
•	Development of a user-friendly prediction interface for estimating friction coefficients under specified braking conditions.
•	Extension of the methodology to composite railway brake blocks.
8. Conclusion
This project demonstrates the application of Polynomial Ridge Regression to analyse and estimate the friction coefficient of cast iron railway brake blocks under different braking conditions.
The fourth-degree polynomial calibration model achieved an in-sample R² of approximately 0.99. The best evaluated configuration also achieved a pooled cross-validation R² of 0.8140.
Nevertheless, group-wise validation revealed limitations in predicting friction behaviour for certain unseen initial braking speed conditions.
The study provides a practical demonstration of how machine learning can be integrated with mechanical engineering research to investigate complex non-linear relationships in railway braking systems.
9. Technologies and Libraries
The project was developed using Python in Google Colab.
•	Python
•	Google Colab
•	Pandas
•	NumPy
•	Matplotlib
•	Seaborn
•	Scikit-learn
•	OpenPyXL
10. Repository Contents
•	Cast_Iron_Brake_Block_ML_Ready_Dataset.xlsx – Prepared dataset used for model development.
•	Cast_Iron_Calibration_Figure.png – Calibration plot comparing observations and predictions.
•	Cast_Iron_Regression_Results.xlsx – Regression coefficients, calibration predictions, residuals and model performance.
•	Python Jupyter Notebook (.ipynb) – Data processing, model development, calibration, visualisation and result generation.
11. Author
Dr. V. M. Ravindra Kumar
Mechanical Engineering | Railway Brake Block Research | Machine Learning Applications
12. Disclaimer
This repository is intended for educational, research and portfolio demonstration purposes. The dataset consists of approximate digitised observations extracted from published experimental plots and should not be treated as the original raw experimental dataset. The developed model is exploratory and requires further validation using independent experimental measurements before engineering or operational application.

