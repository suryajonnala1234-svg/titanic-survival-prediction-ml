# Titanic Survival Prediction 🚢

A Machine Learning web application that predicts whether a passenger would survive the Titanic disaster based on passenger details.

## 📌 Project Overview

This project uses a trained machine learning model to predict passenger survival on the Titanic dataset.
The model is integrated with a Flask web application where users can enter passenger information and receive a prediction.

## 🧠 Machine Learning Model

The prediction is done using a **Decision Tree Classifier** from Scikit-Learn.

### Prediction Pipeline

The model follows these steps before making a prediction:

1. **Handling Missing Values**

   * Missing values in Age and Embarked are filled using `SimpleImputer`.

2. **Feature Engineering**

   * Some features are transformed using `FunctionTransformer`.

3. **Categorical Encoding**

   * Categorical features like **Sex** and **Embarked** are converted into numerical values using **One Hot Encoding**.

4. **Feature Scaling**

   * Numerical features are normalized using **MinMaxScaler**.

5. **Feature Selection**

   * Important features are selected using **SelectKBest**.

6. **Model Training**

   * The final model used for prediction is a **Decision Tree Classifier**.

After preprocessing, the trained pipeline predicts whether the passenger:

* **Survived**
* **Did Not Survive**

The trained pipeline is saved using **pickle** and loaded in the Flask application.

## 🛠️ Technologies Used

* Python
* Scikit-Learn
* Flask
* Pandas
* NumPy
* HTML
* CSS

## 📂 Project Structure

```
titanic-survival-prediction-ml
│
├── app.py
├── requirements.txt
├── data
│   └── train.csv
├── jupyter
│   └── model.ipynb
├── models
│   ├── df.pkl
│   └── pipe.pkl
├── static
│   └── styles.css
├── templates
│   └── index.html
```

## ▶️ How to Run the Project

1. Clone the repository

git clone https://github.com/yourusername/titanic-survival-prediction-ml.git

2. Navigate to the project folder

cd titanic-survival-prediction-ml

3. Create a virtual environment

python -m venv venv

4. Activate the environment

venv\Scripts\activate

5. Install dependencies

pip install -r requirements.txt

6. Run the Flask app

python app.py

7. Open in browser

http://127.0.0.1:5000

## 📊 Output

The application predicts whether the passenger **Survived** or **Did Not Survive** based on the provided passenger information.

## 👨‍💻 Author

Teja Surya Jonnala
