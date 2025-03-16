Car Price Prediction

Overview

This project aims to predict the selling price of used cars using machine learning models. The dataset contains information about various cars, including their year of manufacture, present price, kilometers driven, fuel type, seller type, transmission, and owner details.

Dataset

The dataset used is car data.csv, which contains the following attributes:

Car_Name: Name of the car (not used in prediction)

Year: Manufacturing year of the car

Selling_Price: Price at which the car is being sold

Present_Price: Current price of the car (showroom price)

Kms_Driven: Distance driven by the car in kilometers

Fuel_Type: Type of fuel used (Petrol/Diesel/CNG)

Seller_Type: Whether the seller is a dealer or an individual

Transmission: Type of transmission (Manual/Automatic)

Owner: Number of previous owners

Dependencies

To run this project, you need to install the following Python libraries:

pip install pandas numpy scikit-learn matplotlib

Data Preprocessing

Checked for missing values and data types.

Encoded categorical variables (Fuel_Type, Seller_Type, Transmission) using LabelEncoder.

Separated independent variables (x) and dependent variable (y).

Split data into training (90%) and testing (10%) sets.

Model Training

1. Linear Regression

Trained using train_x and train_y.

Achieved an R² score of:

Test Data: 0.8311

Train Data: 0.8806

2. Lasso Regression

Used alpha=0.1, max_iter=2000, and tol=0.01.

Achieved an R² score of:

Test Data: 0.8597

Train Data: 0.8702

Model Evaluation

Compared actual vs predicted prices for both models.

Visualized results using scatter plots.

Lasso Regression performed slightly better than Linear Regression.

Visualization

A scatter plot was generated to compare actual and predicted prices:

plt.xlabel('Actual Price', color='blue')
plt.ylabel('Predicted Price', color='red')
plt.scatter(test_y, test_y, color='blue', label='Actual Price')
plt.scatter(test_y, reg.predict(test_x), color='red', label='Predicted Price')
plt.legend()
plt.show()

Conclusion

Both models performed well, with Lasso Regression having a slight edge.

Future improvements can include:

Feature engineering (e.g., creating new features from existing ones).

Trying other regression models (e.g., Random Forest, XGBoost).

Hyperparameter tuning for better optimization.

How to Run the Project

Clone this repository.

Ensure car data.csv is in the same directory.

Run car_price_prediction.py to train and evaluate the models.
