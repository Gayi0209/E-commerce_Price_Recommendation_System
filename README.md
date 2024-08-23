# E-commerce_Price_Recommendation_System

This project focuses on building a price recommendation system for an e-commerce platform using machine learning. The system analyzes various factors such as present price, web traffic, units sold, customer ratings, and stock status to recommend optimal pricing strategies.

## Project Overview
The E-commerce Price Recommendation System is designed to assist online retailers in optimizing their pricing strategies based on data-driven insights. The system predicts whether a product is likely to be purchased or left in the cart, and then recommends price adjustments accordingly.

## Features
- **Upload CSV Data**: Users can upload their sales data in CSV format.
- **Price Recommendation**: The system recommends price adjustments based on predicted cart status.
- **Download Processed File**: Users can download the processed file with recommendations.

## Technologies Used
- **Python**: For data processing and model building.
- **Flask**: For building the web interface.
- **HTML/CSS**: For frontend development.
- **Scikit-learn**: For machine learning model development.
- **Pandas/Numpy**: For data manipulation and analysis.
- **Joblib**: For saving and loading machine learning models.

## Dataset
The dataset should include the following columns:
- `Present Price`
- `Web Traffic`
- `Units Sold`
- `Customer Ratings`
- `Stock Status`
- `Cart Status` (Target variable)

## Model Training
The machine learning model used in this project is a RandomForestClassifier. The model is trained using the following features:
- `Present Price`
- `Web Traffic`
- `Units Sold`
- `Customer Ratings`
- `Stock Status`

The target variable is `Cart Status`, which indicates whether the item was purchased or left in the cart.

## Evaluation
The model's performance is evaluated using a classification report, which includes precision, recall, F1-score, and accuracy for each class.

## Results
After training and evaluation, the system predicts the cart status for each item and recommends price adjustments:
- **Increase price by 10%** for items likely to be purchased.
- **Decrease price by 10%** for items likely to be left in the cart.

## Flask Application
The Flask application provides a user interface for uploading CSV files, processing the data to generate price recommendations, and downloading the processed file.

### Routes
- `/`: Displays the homepage with the file upload form.
- `/upload`: Handles file uploads, processes the data, and generates price recommendations.
- `/processed/<filename>`: Allows users to download the processed file.

### Key Functions
- `price_recommendation(row)`: A helper function that takes a row of data, predicts the cart status using the trained model, and returns the recommended price adjustment.
- `upload_file()`: Handles the file upload, processes the data, and saves the processed file.
- `download_file(filename)`: Serves the processed file for download.


## Contributing
Contributions are welcome! Please fork this repository and submit a pull request for any features, bug fixes, or enhancements.

