# 🤖 Hotel Booking Cancellation Classification

**Artificial Intelligence Course Final Project**  
Contributors: Yehia Hany SHORIM, Ahmed Osama, Omar Alaa, Belal Ahmed, Malak Mowaffak  

---

## Project Overview
This project implements a machine learning system to predict **hotel booking cancellations**. It demonstrates practical AI skills including **data preprocessing, feature engineering, model training, and evaluation** using Python and Scikit-learn.

The goal is to handle real-world tabular data, deal with class imbalance, optimize features, and compare multiple ML models to identify the most effective solution.

---

## Key Steps

### 1. Data Preprocessing & Cleaning
- Handled missing values (e.g., children → 0, country → mode, agent/company → -1).  
- Fixed data types (dates converted to numeric formats).  
- Removed duplicates and extreme outliers using IQR.  
- Encoded categorical variables with **Label Encoding** and **One-Hot Encoding**.

### 2. Exploratory Data Analysis (EDA)
- Analyzed **cancellation distribution**, **seasonal trends**, **weekly patterns**, **city-wise bookings**, and **ADR correlation**.  
- Identified patterns such as higher cancellation rates for expensive bookings and longer lead times.

### 3. Feature Engineering
- Created meaningful features: `arrival_weekday`, `arrival_week`, `arrival_season`, `total_stay`, `total_guests`, `is_family`, `adr_per_person`, `long_lead_time`.  
- Dropped irrelevant or highly correlated features to prevent leakage.

### 4. Handling Data Imbalance
- Split data into **train and test sets**.  
- Applied **oversampling** on the minority class (canceled bookings) in the training set to achieve a balanced 50/50 distribution.

### 5. Feature Selection with Genetic Algorithm
- Used **GAFeatureSelectionCV** with Logistic Regression to select an optimal subset of features.  
- Hyperparameters: population = 10, generations = 5, mutation probability = 0.2, crossover probability = 0.5.  
- Evaluated fitness with 5-fold cross-validation and accuracy metric.

### 6. Model Building
- **K-Nearest Neighbors (KNN)** — optimized `k` through hyperparameter tuning.  
- **Decision Tree** — tested multiple depths to avoid overfitting.  
- **Multi-Layer Perceptron (MLP)** — experimented with different architectures using Adam optimizer and ReLU activation.

### 7. Performance Evaluation
- Compared models on **accuracy, precision, recall, and F1 score**.  
- Used **confusion matrices** to analyze model strengths and weaknesses.  
- Selected the **best model** based on F1 score for robust performance on unseen data.

---

## Technologies Used
- **Python**, **Scikit-learn**, **Pandas**, **NumPy**, **Matplotlib/Seaborn**  

---

## Project Documentation
📄 [View Full Documentation PDF](https://github.com/Yehiahany2005/Hotel-Booking-Cancellation-Classification/blob/5d8c95583175fe726051a513bba9e70790354064/AI%20documentation%20pdf.pdf)
