<img src="smartphones_image.jpg" alt="image" width="800" height="400"/>


# Smartphone Price Predictor

## Problem Statement
Smartphone pricing is a critical challenge for businesses and consumers alike. With thousands of models launched every year, retailers often struggle to set competitive, data-driven prices, while consumers find it difficult to evaluate whether a device is worth its cost. This mismatch leads to inefficient pricing strategies, revenue loss for businesses, and poor decision-making for buyers.

To solve this business problem, I built the Smartphone Price Predictor, a machine learning solution that leverages smartphone specifications (RAM, storage, battery, processor, camera, etc.) to predict prices with accuracy. The model provides:

📊 Actionable insights for businesses to optimize pricing strategies and remain competitive in the market.

🛒 Confidence for consumers in identifying fair prices and making smarter purchase decisions.

By aligning product specifications with real market value, this project demonstrates how data science can directly impact pricing strategy, customer trust, and overall business performance

## Table of Contents
1. [Dataset Description](#dataset-description)
2. [Project Objectives](#project-objectives)
3. [Setup and Installation](#setup-and-installation)
4. [Data Preprocessing](#data-preprocessing)
5. [Exploratory Data Analysis (EDA)](#exploratory-data-analysis-eda)
6. [Model Training and Evaluation](#model-training-and-evaluation)
7. [Results](#results)

The dataset contains 1953 rows and 30 columns, capturing various attributes of smartphones, including:
- **mobile_name**: smartphone’s name.
- **brand**: Brand of the smartphone.
- **price**: The price of the smartphone in INR.
- **avg_rating**: The average customer rating.
- **5g_or_not**: A Boolean value representing if the phone has 5G support or not.
- **nfc**:boolean whether nfc supported or not.
- **ir_blaster**: ir_blaster or not(having 0/1 values).
- **processor_brand**: The brand of the processor used in the smartphone.
- **Processor_name**: name of the processor used in the smartphone.
- **num_cores**: The number of cores in the smartphone's processor.
- **processor_speed**: The clock speed of the processor in GHz.
- **battery_capacity**: The battery capacity of the smartphone in mAh.
- **fast_charging_available**: Indicates whether the phone supports fast charging (1 for yes, 0 for no).
- **fast_charging**: The wattage of the fast charging feature (if available).
- **ram**: The amount of RAM in GB.
- **memory**: The internal storage capacity of the smartphone in GB.
- **screen_size**: The diagonal screen size in inches.
- **refresh_rate**: The screen refresh rate in Hz.
- **Punct_Hole**: display info.
- **Notch**: whether display is of Notch type.
- **num_rear_cameras**: The number of rear cameras on the smartphone.
- **os**: The operating system of the smartphone (e.g., Android, iOS).
- **primary_camera**: The resolution of the primary rear camera in megapixels.
- **front_camera**: The resolution of the front camera in megapixels.
- **num_rear_camera**:total number of rear cameras.
- **num_front_camera**:total number of front camera.
- **Extra_storage_supported**: Indicates whether the phone supports expandable storage (1 for yes, 0 for no).
- **Extra_storage(GB)**:how much extra storage available.
- **resolution_height**: The height of the screen resolution in pixels.
- **resolution_width**: The width of the screen resolution in pixels.

## Project Objectives
1. **Data Preprocessing**: Cleaning the data to get it into useful form and preprocess the dataset to handle missing values, outliers, and categorical data.
2. **Exploratory Data Analysis (EDA)**: Visualize and analyze the relationships between features and price of smartphone.
3. **Model Training**: Train machine learning models to predict smartphone price.
4. **Model Evaluation**: Compare the performance of different models and identify the most effective ones.

## Setup and Installation
1. Clone this repository:
   ```bash
   git clone (https://github.com/Akash3710/Smartphone-Price_Predictor)
   ```
2. Navigate to the project directory:
   ```bash
   cd Smartphone-Price_Predictor
   ```

3. Run the Main.py file in folder main:
   ```bash
   Data_preprocessing_Model_building.py
   ```

## Data Preprocessing
In this project, the dataset underwent several preprocessing steps to ensure data quality and suitability for analysis. These steps included:

- Initial Data Exploration: Gaining insights into the dataset's structure, content, and potential issues by examining its shape, descriptive statistics, data types, and missing values.
- Data Cleaning:
  - Dropping irrelevant columns.
  - Extracting multiple information into seperate columns
  - resolving shifting issues
  - tidiness issues.
- Outlier Handling: Identifying and addressing outliers in each column to prevent them from skewing the analysis. This involved checking for negative values and other anomalies.
- Missing Value Imputation: Filling in missing values using appropriate strategies such as mean, median depeding on what is type of null values based on the column's characteristics.
- Duplicate Removal: Removing duplicate entries based on the model column to ensure data uniqueness and prevent redundancy in the analysis.
- 
## Exploratory Data Analysis (EDA)
Exploratory Data Analysis (EDA) focused on uncovering key insights and trends in the smartphone dataset using various visualizations:

- Price Analysis
   - Explored correlations between price and other features with correlation bar plots.
   - Visualized price distributions and compared pricing for smartphones with and without 5G.

- Rating Insights
   - Examined the distribution of average ratings and their relationship with price to understand how customer satisfaction aligns with cost.

- Brand Analysis
   - Displayed brand distributions to highlight the most common brands.
   - Analyzed average price and ratings by brand, with pie charts illustrating features like 5G and fast charging adoption across brands.
   - Investigated brand trends for rear camera counts and visualized their averages.

- Model Highlights
   - Compared the most expensive and highest-rated models side by side to identify standout devices.
   - Used pie charts to show 5G and memory availability distributions across models.
   - Created visual comparisons for pricing trends among 5G and non-5G smartphones.

  ## Model Training and Evaluation

In this project, multiple machine learning models are trained and evaluated on a dataset to predict smartphone price. The following models are used:

- **Random Forest Regressor**
- **Decision Trees**
- **XGBoost Regressor**
- **Gradient Boosting Regressor**

Each model is trained on the same dataset. The dataset is preprocessed using one-hot encoding and frequency encoding.
The models are evaluated based on the following metrics:
- **RMSE (root Mean Squared Error)**
- **Adjusted R2 score**
- **R2 (R-squared)**

The training results for model are reported both **before** and **after** hypertuning.

## Results

### Training LinearRegression:
| Metric | Scores |
|--------|--------|
| R2    | 0.7424   |
|  Adjusted R2     |0.7388|

### Training Random Forest:
| Metric | Scores |
|--------|--------|
| RMSE    | 9998.606481169798  |
| R2    | 0.894997238990165    |
|  Adjusted R2     |0.8872192566931403 |

### Training Gradient Boosting:
| Metric | Scores |
|--------|--------|
| RMSE    |9908.281512472238 |
| R2    | 0.8968858084369594    |
|  Adjusted R2     |0.8892477201730304 |

### Decision Tree
| Metric | Scores |
|--------|--------|
| RMSE    |14821.49291832784 |
| R2    | 0.7692691486849267    |
|  Adjusted R2     |0.7521779745134398 |

### XGBoost Regressor (Best Permoring Model)
| Metric | Scores |
|--------|--------|
| RMSE    |9550.346933700199 |
| R2    | 0.9042012011996108    |
|  Adjusted R2     |0.9042012011996108|

## futher improvements
- Expand the dataset with more recent smartphone data.
- Integrate additional features such as market demand or customer reviews and other more price impacting features.
- Explore advanced models for improved prediction accuracy like LightGBM ,Catboost.
