# 🌧️ Logistic Regression Model for Weather Prediction 🌞

## 📊 Overview

This repository contains a **Logistic Regression** model designed to predict whether it will rain tomorrow (`RainTomorrow`) based on various weather-related features from the `Weather_Australia.csv` dataset. The dataset includes parameters like temperature, humidity, wind speed, and rainfall, all of which are used to forecast the likelihood of rain. ☔

## 🛠️ Steps Performed

### 1. **🔧 Importing Required Libraries**
The necessary libraries for data manipulation, visualization, and machine learning were imported, including **Pandas**, **Numpy**, **Matplotlib**, **Seaborn**, and **Scikit-learn**.

### 2. **📂 Loading and Exploring the Dataset**
The dataset was loaded from an online URL. Initial exploration was performed to understand its structure, including:
- Viewing the first few rows.
- Checking for missing values.
- Summarizing the dataset's statistics.

### 3. **🔄 Handling Missing Values**
Missing values were handled using two techniques:
- **Numerical columns** (e.g., temperature, wind speed) were filled with their median values. 
- **Categorical columns** (e.g., wind direction, rain today) were filled with the mode (most frequent value).

### 4. **📉 Outlier Detection and Treatment**
Boxplots were used to visually identify outliers in various columns like **rainfall**, **evaporation**, and **wind speed**. The **Interquartile Range (IQR)** method was then applied to set upper and lower bounds, handling the outliers effectively.

### 5. **⚙️ Feature Engineering**
- The **Date** column was split into separate `Year`, `Month`, and `Day` columns to extract useful time-related features.
- **One-hot encoding** was applied to categorical features (e.g., Location, Wind Gust Direction) to convert them into numerical values.

### 6. **📊 Splitting Data into Training and Test Sets**
The dataset was split into **training** and **testing** sets using an **80-20** ratio. The training data was used to train the logistic regression model, while the test data was used to evaluate its performance.

### 7. **🔬 Training the Logistic Regression Model**
The **Logistic Regression** model was trained on the training data, predicting whether it will rain the next day based on the weather features.

### 8. **📈 Evaluating the Model**
The model's performance was evaluated using the following metrics:
- **Accuracy Score**: The proportion of correct predictions (both on the training and test datasets).
- **Confusion Matrix**: A matrix showing true positives, true negatives, false positives, and false negatives to evaluate the model's accuracy.

### 9. **🛡️ Handling Overfitting**
To address **overfitting**, the model was refitted with a **lower regularization parameter** (`C=0.01`) and an **L1 penalty**. This improved generalization and reduced complexity.

### 10. **🔍 Confusion Matrix & Classification Report**
The **Confusion Matrix** was used for further evaluation, and the **Classification Report** provided detailed metrics like precision, recall, and F1-score for both classes (rain/no rain).

---

## 📦 Dependencies

To run the code, you'll need the following Python libraries:

- **Python 3.x**
- **pandas**
- **numpy**
- **matplotlib**
- **seaborn**
- **scikit-learn**
