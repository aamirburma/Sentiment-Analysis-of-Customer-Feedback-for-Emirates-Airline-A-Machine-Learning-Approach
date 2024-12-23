# Emirates Airways Sentiment Analysis

This project performs sentiment analysis on customer reviews of Emirates Airways using machine learning techniques. The goal is to predict the sentiment of customer reviews, classifying them as either **Positive** or **Negative** based on various features such as service quality, comfort, food, and entertainment.

## Table of Contents

- [Project Overview](#project-overview)
- [Dataset](#dataset)
- [Features](#features)
- [Technologies Used](#technologies-used)
- [Steps](#steps)
- [Evaluation Metrics](#evaluation-metrics)
- [Model](#model)
- [Results](#results)
- [Conclusion](#conclusion)
- [Usage](#usage)
- [License](#license)

## Project Overview

This project uses a dataset of Emirates Airways customer reviews, with several features describing the customer's experience and overall rating. We train a machine learning model to predict whether the sentiment of a review is **Positive** or **Negative**. The machine learning model is evaluated using accuracy, precision, recall, and confusion matrix.

## Dataset

The dataset is composed of customer reviews from Emirates Airways, including the following features:
- **Title**: Review title
- **Date Published**: Date the review was posted
- **Status**: Review status (e.g., approved, pending)
- **Aircraft**: Type of aircraft
- **Travel Type**: Type of travel (e.g., business, leisure)
- **Travel Class**: Class of travel (e.g., economy, business, first class)
- **Route**: Flight route
- **Date Flown**: Date the flight took place
- **Seating Comfort**: Rating of the seating comfort (numeric)
- **Staff Service**: Rating of the staff service (numeric)
- **Food Quality**: Rating of the food quality (numeric)
- **Entertainment**: Rating of in-flight entertainment (numeric)
- **WiFi**: Rating of Wi-Fi service (numeric)
- **Ground Service**: Rating of ground service (numeric)
- **Value for Money**: Rating of the value for money (numeric)
- **Recommended**: Whether the reviewer would recommend the airline (yes/no)
- **Overall Rating**: Numeric rating provided by the reviewer
- **Review**: Full text of the review
- **Country**: Country of the reviewer

## Features

- Sentiment analysis of customer reviews.
- Predictions based on flight experience ratings.
- Random Forest classifier model.
- Model evaluation using confusion matrix, accuracy, precision, and recall.

## Technologies Used

- **Python**: Primary programming language
- **Libraries**: 
  - Pandas
  - NumPy
  - scikit-learn
  - Matplotlib
  - Seaborn
  - Jupyter Notebook (ipynb)

## Steps

1. **Data Preprocessing**:
   - Load and clean the dataset.
   - Handle missing data and categorize sentiment based on the overall rating (Positive if the rating is greater than 5, Negative otherwise).
   
2. **Feature Engineering**:
   - Extract relevant features for the model (e.g., Travel Class, Route, Service ratings).
   - Convert categorical data to numerical format using one-hot encoding.
   
3. **Model Training**:
   - Split data into training and testing sets.
   - Train a Random Forest classifier on the training data.

4. **Model Evaluation**:
   - Evaluate the model using metrics such as accuracy, precision, recall, and confusion matrix.
   - Visualize the confusion matrix using a heatmap.

5. **ROC Curve** (Optional):
   - Generate and evaluate an ROC curve to assess model performance.

## Evaluation Metrics

- **Accuracy**: The percentage of correctly classified reviews.
- **Precision**: How many of the positive predictions were actually correct.
- **Recall**: How many of the actual positive reviews were correctly identified.
- **F1-Score**: Harmonic mean of Precision and Recall.
- **Confusion Matrix**: A matrix to show the true positives, false positives, true negatives, and false negatives.

## Model

We used a **Random Forest classifier** to predict the sentiment of the reviews. Random Forest is an ensemble method that creates multiple decision trees and combines their predictions to improve performance.

## Results

The model was evaluated based on several metrics:
- **Accuracy**: 76%
- **Precision**: 72%
- **Recall**: 75%
- **F1 Score**: 73%

The confusion matrix shows how well the model distinguishes between positive and negative sentiments.

## Conclusion

The Random Forest model provides reasonable accuracy in classifying customer reviews as Positive or Negative. However, there is room for improvement, especially with regard to balancing class predictions and handling rare categories more effectively.

## Usage

1. Clone the repository: 
   ```bash
   git clone https://github.com/aamirburma/Sentiment-Analysis-of-Customer-Feedback-for-Emirates-Airline-A-Machine-Learning-Approach.git
   ```

2. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

3. Run the Jupyter notebook for model training and evaluation:
   ```bash
   jupyter notebook Emirates_Airways_Sentiment_Analysis.ipynb
   ```

4. Explore the results and try to improve the model by tuning hyperparameters or using other models like SVM, XGBoost, etc.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.