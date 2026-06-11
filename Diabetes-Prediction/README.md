Diabetes Prediction Using Support Vector Machine (SVM)

Project Overview

This machine learning project predicts whether a person is diabetic or non-diabetic using the PIMA Indians Diabetes Dataset. The model is built using the Support Vector Machine (SVM) algorithm and achieves predictions based on several medical attributes.

Dataset

The project uses the PIMA Indians Diabetes Dataset, which contains medical diagnostic measurements for female patients.

Features

- Pregnancies
- Glucose
- BloodPressure
- SkinThickness
- Insulin
- BMI (Body Mass Index)
- DiabetesPedigreeFunction
- Age

Target Variable

- 0 → Non-Diabetic
- 1 → Diabetic

Technologies Used
- Python
- NumPy
- Pandas
- Scikit-learn

Project Workflow

1. Data Collection and Analysis

- Load the dataset using Pandas
- Explore dataset structure
- Check statistical summaries
- Analyze class distribution

2. Data Preprocessing

- Separate features and target labels
- Standardize feature values using `StandardScaler`
- Handle missing values (if present)

3. Train-Test Split

The dataset is split into:

- 80% Training Data
- 20% Testing Data

Using:

python
train_test_split(
    X_train,
    Y_train,
    test_size=0.2,
    stratify=Y_cleaned,
    random_state=2
)

4. Model Training

A linear Support Vector Machine classifier is used:

python
classifier = svm.SVC(kernel='linear')
classifier.fit(X_train, Y_train)


5. Model Evaluation

Model performance is evaluated using Accuracy Score on:

- Training Data
- Testing Data

python
accuracy_score(predictions, actual_labels)


6. Prediction System

The trained model can predict whether a new patient is diabetic based on input medical values.

Example:

python
input_data = (
    1,
    5,
    166,
    72,
    19,
    175,
    25.8,
    0.587,
    51
)



Installation

Clone the repository:

bash
git clone https://github.com/your-username/ML-Projects.git


Navigate to the project directory:

bash
cd ML-Projects

Install dependencies:

bash
pip install numpy pandas scikit-learn


Running the Project

Place the `diabetes.csv` dataset in the project directory and run:

bash
python diabetes_prediction.py


Sample Output

Training Accuracy: 0.78
Testing Accuracy: 0.77

Prediction: Diabetic


*(Results may vary depending on dataset version and train-test split.)*

 Future Improvements

- Hyperparameter tuning
- Feature selection
- Compare multiple machine learning algorithms
- Deploy as a web application using Flask or Streamlit
- Add visualizations and performance metrics

Author

Mohammed Sameewullah

Machine Learning Project – Diabetes Prediction using Support Vector Machine (SVM)
