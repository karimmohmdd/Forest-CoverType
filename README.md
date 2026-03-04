# 🌲 Forest Cover Type Prediction

## 📖 Overview
This project aims to predict the forest cover type (the predominant kind of tree cover) from strictly cartographic variables. The project utilizes machine learning models to classify 7 different forest cover types based on a dataset containing 54 features (elevation, slope, soil type, wilderness area, etc.).

## 📊 Dataset
- **Source:** [Covertype Data Set - UCI Machine Learning Repository](https://archive.ics.uci.edu/ml/datasets/covertype)
- **Instances:** 581,012
- **Features:** 54 (10 numerical, 44 categorical/one-hot encoded)
- **Classes:** 7 Forest Cover Types

## 🛠️ Technologies & Libraries Used
- **Python 3.x**
- **Pandas & NumPy** (Data manipulation)
- **Scikit-Learn** (Data preprocessing, Random Forest, Evaluation metrics)
- **XGBoost** (Advanced gradient boosting classification)
- **Matplotlib & Seaborn** (Data visualization & Confusion Matrix)

## 🚀 Project Pipeline
1. **Data Preprocessing:** - Loaded the Covertype dataset.
   - Applied `StandardScaler` to the first 10 numerical features to ensure all models train efficiently.
2. **Modeling & Training:** - Trained a **Random Forest Classifier** as a strong baseline model.
   - Trained an **XGBoost Classifier** (using `tree_method='hist'`) for optimized performance on large data.
3. **Evaluation:**
   - Compared both models using `Accuracy` and `F1-Score`.
   - Generated a **Classification Report** to analyze precision and recall for minority classes.
   - Visualized the **Confusion Matrix** to identify misclassifications between specific tree types.

## 📈 Results
*Note: Run the main script to see the exact accuracy on your machine.*
- **Random Forest:** Provided robust accuracy with minimal tuning.
- **XGBoost:** Generally yielded higher accuracy and better handling of complex patterns after adjusting the class labels (0-indexed).
