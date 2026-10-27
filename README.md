# 🚦 TrafficIQ: Traffic Demand Prediction Using Machine Learning

### AI-Based Traffic Analysis and Prediction

TrafficIQ is a machine learning mini-project that predicts traffic demand using historical traffic data. It uses a Random Forest Regression algorithm to analyze traffic conditions and estimate traffic demand in Passenger Car Units per hour (PCU/hr).

The project demonstrates how machine learning can support intelligent transportation systems by analyzing vehicle counts, traffic density, queue lengths, vehicle speeds, and other traffic-related parameters.

---

## 📌 Project Overview

Traditional traffic management systems often rely on fixed assumptions and predefined traffic patterns. TrafficIQ uses machine learning to identify relationships between traffic conditions and traffic demand.

The trained model predicts traffic demand based on the supplied input features. The project also provides data visualization, model evaluation, feature importance analysis, and prediction results.

## 🎯 Objectives

* Analyze traffic data using Python.
* Preprocess categorical and numerical features.
* Train a Random Forest Regression model.
* Predict traffic demand in PCU/hr.
* Evaluate model performance using regression metrics.
* Visualize traffic patterns and prediction results.
* Identify important features influencing traffic demand.
* Save the trained model for future predictions.

## 🛠️ Technologies Used

| Technology   | Purpose                              |
| ------------ | ------------------------------------ |
| Python       | Programming language                 |
| Pandas       | Dataset processing and analysis      |
| NumPy        | Numerical computations               |
| Matplotlib   | Data visualization                   |
| Seaborn      | Statistical visualization            |
| Scikit-learn | Machine learning and evaluation      |
| Joblib       | Saving and loading the trained model |
| JupyterLab   | Development environment              |

## 🧠 Machine Learning Algorithm

**Random Forest Regression**

Random Forest Regression combines predictions from multiple decision trees to estimate a continuous numerical value. It can model nonlinear relationships between traffic conditions and traffic demand.

### Model Configuration

* Number of estimators: 120
* Maximum tree depth: 14
* Minimum samples for splitting: 4
* Minimum samples per leaf: 2
* Random state: 42
* Training and testing split: 80:20

The model uses a Scikit-learn Pipeline containing a `ColumnTransformer`, `OneHotEncoder` for the categorical road feature, and `StandardScaler` for numerical features.

## 📊 Dataset Description

The dataset is stored in `traffic_dataset.csv`.

### Input Features

| Feature             | Description                            |
| ------------------- | -------------------------------------- |
| `road`              | Road or traffic direction              |
| `vehicle_count`     | Number of vehicles                     |
| `traffic_density`   | Traffic density                        |
| `queue_length`      | Length of the traffic queue            |
| `avg_speed`         | Average vehicle speed                  |
| `hour_of_day`       | Hour of the day                        |
| `day_of_week`       | Day of the week                        |
| `is_weekend`        | Indicates whether the day is a weekend |
| `prev_waiting_time` | Previous waiting time                  |

### Target Variable

`traffic_demand` — estimated traffic demand measured in PCU/hr.

The actual dataset size and data quality should be checked before training.

## ⚙️ Project Workflow

1. Load the traffic dataset.
2. Inspect columns and missing values.
3. Clean records with missing required values.
4. Visualize traffic demand and vehicle counts.
5. Separate input features and the target variable.
6. Split the data into training and testing sets.
7. Encode categorical data and scale numerical features.
8. Train the Random Forest Regression model.
9. Evaluate the model on the test set.
10. Visualize actual versus predicted traffic demand.
11. Analyze feature importance.
12. Save the trained model and evaluation metadata.

## 📈 Model Evaluation

The model is evaluated using the following metrics:

* **Mean Absolute Error (MAE):** Measures the average absolute difference between actual and predicted traffic demand.
* **Mean Squared Error (MSE):** Measures the average squared prediction error.
* **Root Mean Squared Error (RMSE):** Measures prediction error in the target variable's units.
* **R² Score:** Measures how well the model explains variation in the target variable.

The actual evaluation values are generated when the model is trained. They should be reported from the program's output rather than assumed in advance.

## 📁 Project Structure

```text
TrafficIQ/
│
├── traffic_dataset.csv
├── traffic_prediction.ipynb
├── models/
│   ├── traffic_rf_model.joblib
│   └── model_metadata.json
│
└── README.md
```

The notebook filename is an example; use the actual name of your notebook.

## 🚀 Installation and Execution

### 1. Install Python Libraries

Run the following command in a JupyterLab cell:

```python
%pip install pandas numpy matplotlib seaborn scikit-learn joblib
```

### 2. Prepare the Dataset

Place `traffic_dataset.csv` in the directory accessible to your JupyterLab notebook and update the dataset path if necessary.

### 3. Run the Notebook

Open your notebook and execute all cells in order.

The notebook will load the dataset, visualize traffic patterns, train the model, evaluate performance, generate predictions, and save the trained model.

### 4. Generated Files

After successful execution, the project generates:

* `traffic_rf_model.joblib` — trained machine learning pipeline.
* `model_metadata.json` — model configuration, evaluation metrics, feature importance, and training timestamp.

## 🔮 Future Scope

* Integrate real-time traffic data from sensors or cameras.
* Develop a Streamlit dashboard for interactive predictions.
* Extend the model to short-term traffic forecasting.
* Integrate adaptive traffic signal timing optimization.
* Explore traffic congestion detection and vehicle classification.
* Evaluate the model using real-world traffic datasets.

## 🎓 Applications

* Intelligent Transportation Systems
* Urban traffic analysis
* Traffic demand estimation
* Smart city research
* Traffic management decision support

## 👩‍💻 Academic Project

**Project Name:** TrafficIQ: Traffic Demand Prediction Using Machine Learning

**Project Type:** Machine Learning Mini-Project

**Department:** Computer Engineering

**Development Environment:** JupyterLab

## 📜 Conclusion

TrafficIQ demonstrates the application of machine learning to traffic demand prediction. By analyzing traffic-related features and applying Random Forest Regression, the project estimates traffic demand and evaluates prediction performance. Its modular pipeline also enables the trained model to be saved and reused for future predictions.

The project provides a foundation for further development in intelligent traffic analysis and adaptive traffic management.

---

**Keywords:** Machine Learning, Random Forest Regression, Traffic Prediction, Python, Scikit-learn, Data Visualization, Intelligent Transportation Systems, TrafficIQ.
