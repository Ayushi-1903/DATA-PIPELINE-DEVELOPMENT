# DATA-PIPELINE-DEVELOPMENT

Company Name:CODTECH IT SOLUTIONS

Name: Ayushi Verma

Intern ID :CT6MTNYD

Domain: Data Science 

Durations: 6 months

Mentor:Muzammil Ahmed

# Description of the Task 1 Data Pipline Development:

### Task Description: ETL Data Pipeline with Visualization and Modeling

This task involves the development of a complete ETL (Extract, Transform, Load) pipeline applied to the UCI Adult Income dataset using Python. The objective is to preprocess data, visualize key insights, transform features, and evaluate a machine learning model—all while documenting the process with visual artifacts and flow diagrams.

#### 1. Data Extraction
The pipeline begins with the extraction of raw data from a CSV file (`adult.csv`). A function named `extract_data()` is responsible for reading the dataset into a Pandas DataFrame and confirming successful loading.

#### 2. Data Visualization
To explore the dataset, the `visualize_data()` function generates and saves:
* A count plot of the target variable (`income`) to show class distribution.
* A correlation heatmap for numeric features to assess relationships.
* A `plot_pairplot()` function that generates pairwise relationships between selected features.
* A `plot_class_pie()` function to create a pie chart of class distribution.

Inline exploratory data analysis (EDA) is also performed using Matplotlib to immediately inspect target balance and numeric feature correlations.

#### 3. Data Transformation
The `transform_data()` function prepares the dataset for machine learning:
* It separates features (X) and the target column (y).
* Numerical and categorical features are identified and processed separately using Scikit-learn pipelines:
  * Numerical pipeline: Mean imputation and standard scaling.
  * Categorical pipeline: Most frequent imputation and one-hot encoding.
* These pipelines are integrated via a ColumnTransformer.
* Data is split into training and test sets, then transformed using the pipelines.
* Transformed data is converted to DataFrames and returned for further use.

#### 4. Data Loading
The transformed training and test datasets, along with their target values, are saved as CSV files using the `load_data()` function for downstream modeling or inspection.

#### 5. ETL Process Visualization
Two visualization methods document the ETL flow:
* `create_etl_diagram()` creates a Graphviz flowchart showing each ETL stage.
* `draw_etl_flow_with_matplotlib()` draws a simplified ETL pipeline using NetworkX and Matplotlib.

#### 6. Model Training and Evaluation
A Random Forest Classifier is trained on the transformed training data. Predictions are made on the test set and evaluated using a classification report. The model’s feature importances are also visualized, highlighting the top 15 influential features.
#### 7. PCA Visualization
To understand how well the classes separate in reduced dimensions, PCA (Principal Component Analysis) is applied to the training data and visualized in 2D, colored by the target labels.
#### 8. Pipeline Structure Summary
Finally, the script prints a summary of the preprocessing pipeline’s structure using `print_pipeline_structure()`, detailing each transformer and its corresponding columns and operations.

![image](https://github.com/user-attachments/assets/34e6c234-9b51-413b-be29-e353cd42a5bc)



