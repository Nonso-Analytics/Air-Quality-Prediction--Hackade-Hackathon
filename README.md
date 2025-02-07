# HACKADE - Air Quality Prediction Hackathon
# Air Quality Prediction from Low-Cost IoT devices : 4th Place Solution
 By_Chinonso Okonkwo

# Description

Carbon emissions significantly contribute to climate change, and monitoring these emissions is essential for mitigating environmental impact. However, existing high-accuracy reference meters are prohibitively expensive. Chemotronix, a company developing low-cost sensors, seeks to build machine learning models that can accurately map sensor readings to CO2 levels measured by reference meters. This will enable affordable and scalable solutions for tracking carbon emissions globally.

# Goal

The objective is to develop a machine learning model that accurately predicts CO2 levels using data from Chemotronix’s low-cost sensors. By achieving this, participants will help bridge the gap between affordability and precision in carbon emission tracking, enabling widespread adoption of low-cost monitoring technologies.

An accurate prediction model will allow Chemotronix to manufacture low-cost sensors that rival the performance of expensive reference meters. This breakthrough has the potential to:

- Democratize access to environmental monitoring tools.
- Assist governments and organizations in implementing data-driven policies to curb carbon emissions.
- Promote sustainability by making emission tracking affordable for communities and industries worldwide.

# Objectives

- **Data Analysis:** Delve into the dataset through comprehensive exploratory data analysis. Identify outliers and gain a deep understanding of the data's underlying characteristics.

- **Model Building:** Employ advanced machine learning algorithms to construct predictive models. Strive for models that offer exceptional accuracy in predicting CO2 levels.

- **Model Evaluation:** Rigorously evaluate model performance using appropriate metric RMSE. Through meticulous evaluation, select the most effective and precise predictive model.

- **Interpretability:** Unearth the influential factors that shape CO2 levels.

- **Business Impact:** Translate model insights into actionable strategies that can allow Chemotronix to manufacture low-cost sensors that rival the performance of expensive reference meters.

# Installation

To get started with the Chemotronix Air Quality Predictive Modeling Hackathon, follow these installation steps:

1. Clone the Repository: Begin by cloning this repository to your local machine using the following command:


```python
git clone https://github.com/Nonso-Analytics/HACKADE-AIR-QUALITY-HACKATHON.git
```

2. Navigate to the Directory: Move into the project directory:


```python
cd HACKADE-AIR-QUALITY-HACKATHON
```

3. Create a Virtual Environment (Optional): While not mandatory, it's recommended to create a virtual environment to isolate the project dependencies. You can create a virtual environment using venv or conda. For venv, execute:


```python
python -m venv venv
```

Activate the virtual environment



*   On Windows



```python
venv\Scripts\activate
```



*   On MacOS and Linux




```python
source venv/bin/activate
```

4. Install Dependencies: Install the required Python packages using pip:


```python
pip install pandas numpy scikit-learn catboost seaborn matplotlib
```

5. Run the Jupyter Notebook: Launch the Jupyter Notebook to explore the provided dataset and participate in the hackathon:


```python
jupyter notebook
```

6. Open the Notebook: In your web browser, navigate to http://localhost:8888 to access the Jupyter Notebook interface.

That's it! You're all set to dive into the Chemotronix air quality Hackathon.

# Data Description and EDA

This dataset contains valuable information sensor readings by 3 IOT devices, including the temperature reading from the device of the environment where the reading was taken,The Humidity reading from the device of the environment where the reading was taken, The raw output value from the MQ7 sensor , The raw output value from the MQ9 sensor, The raw output value from the MG811 sensor, The raw output value from the MQ135 sensor and their corresponding value of CO2 in ppm from a reference instrument.

## Data Overview

*  Number of Entries (Train): 7,307
*  Features:  Temperature, Humidity, MQ7_analog,
MQ9_analog, MG811_analog, MQ135_analog, device_name
*  Target Variable: CO2

## Data Analysis Highlights

In our exploratory data analysis (EDA), we delved into various aspects of the dataset to understand its characteristics and relationships. Here are some key insights:

- The distribution features is explored using sns pairplots, revealing trends and possible outliers.
- The distribution of C02 is analyzed, highlighting positive skewness and the presence of outliers.
- Missing values were not identified
- Correlation analysis showcases the relationships between features and the target variable ( CO2), guiding feature selection for modeling.

# Data Preprocessing and Feature Engineering

* Added binary indicator variables 'is_alpha','is_beta' and 'is_charlie' to capture device name effects.

* Created new features 'temperature_humidity_ratio' and 'mq7_mq9_ratio' to capture temperature humidity and sensor insights.

* Log transformed 'CO2' column to normalize skewed data



# Machine Learning Workload

## Model Building
* Utilized RandomForestRegressor with RMSE as the loss function for predicting CO2 levels.

Achieved RMSE score of 604 indicating i should consider tuning hyperparameters to allow the model generalize well by;
Reducing max_depth,
Increasing min_samples_split,
Reducing n_estimators, and
Using max_features='sqrt'

* Leaderboard (LB) score of 4.59 for performance on the competition's test dataset (4th Place Score).

## Features Importance
* Top three important features: "Humidity," "MG811_analog"," and "mq7_mq9_ratio" (14.81%, 17.20%, 16.59%).

* Significant contributions from "MQ7_analog" (13.19%), "MQ9_analog" (10.59%) and "Temperature" (8.46%).

* "MQ135_analog", "is_alpha", "is_beta", "is_charlie" and "temperature_humidity_ratio" have relatively lower importance scores.


```python

```
"# Air-Quality-Prediction--Hackade-Hackathon" 
