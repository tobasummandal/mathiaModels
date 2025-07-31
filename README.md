# Mathia Learning Analytics Project

This project contains machine learning models for predicting three learning outcomes: **Metacognition**, **Math Learning**, and **Motivation** based on student behavioral data.

## 📋 Table of Contents

- [Project Overview](#project-overview)
- [Installation](#installation)
- [File Structure](#file-structure)
- [Running the Models](#running-the-models)
- [Model Details](#model-details)
- [Output Files](#output-files)

## 🎯 Project Overview

The project consists of three separate models, each predicting different learning outcomes:

1. **Meta Model**: Predicts `Post3Meta` (Metacognition Assessment)
2. **Math Model**: Predicts `PostMath` (Math Learning Outcomes)  
3. **Motivation Model**: Predicts `PostMotivation3` (Motivation Scores)

Each model uses behavioral features extracted from student interaction data and workspace summaries.

## 🚀 Installation

### 1. Recommended - Create virtual/conda environment

### 2. Install Required Libraries

```bash
# Install all required packages
pip install -r requirements.txt
```

## 3. Running the Models

**RECOMMENDED: Only make required changes to test notebooks and run on pre-trained uploaded models**
**IMPORTANT: Follow the exact order below for each model type**

### **Step 1: Meta Model (Metacognition)**

#### 1.1 Train Meta Model
```bash
# Run the training notebook
jupyter notebook meta_model_team2.ipynb
```

**REQUIRED FILE PATH REPLACEMENTS (Preprocessing Section):**

In the **preprocessing section** of `meta_model_team2.ipynb`, replace:

```python
# REPLACE THESE PATHS WITH YOUR ACTUAL DATA LOCATIONS
df_main = pd.read_csv("./raw_data/training_set_with_formatted_time.csv")
df_ws = pd.read_csv("./raw_data/workspace_summary_train.csv")
df_scores = pd.read_csv("./raw_data/student_scores_train.csv")

# REPLACE THESE OUTPUT PATHS
df_main.to_csv('preprocessed_data/df_main_allws.csv', index=False)
df_ws.to_csv('preprocessed_data/df_ws_allws.csv', index=False)

# REPLACE THESE OUTPUT PATHS
df_main.to_csv("preprocessed_data/df_main.csv", index=False)
df_ws.to_csv("preprocessed_data/df_ws.csv", index=False)
df_scores.to_csv("preprocessed_data/df_scores.csv", index=False)
df_cleaned_meta.to_csv("preprocessed_data/df_cleaned_meta.csv", index=False)
```

#### 1.2 Test Meta Model
```bash
# Run the test notebook
jupyter notebook meta_test_team2.ipynb
```

**REQUIRED FILE PATH REPLACEMENTS (Preprocessing Section):**

In the **preprocessing section** of `meta_test_team2.ipynb`, replace:

```python
# REPLACE THESE PATHS WITH YOUR ACTUAL TEST DATA LOCATIONS
df_main = pd.read_csv("./raw_data/training_set_with_formatted_time.csv")
df_ws = pd.read_csv("./raw_data/workspace_summary_train.csv")
df_scores = pd.read_csv("./raw_data/student_scores_train.csv")

# REPLACE THESE OUTPUT PATHS
df_main.to_csv('preprocessed_data/df_main_allws.csv', index=False)
df_ws.to_csv('preprocessed_data/df_ws_allws.csv', index=False)

# REPLACE THESE OUTPUT PATHS
df_main.to_csv("preprocessed_data/df_main.csv", index=False)
df_ws.to_csv("preprocessed_data/df_ws.csv", index=False)
df_scores.to_csv("preprocessed_data/df_scores.csv", index=False)
df_cleaned_meta.to_csv("preprocessed_data/df_cleaned_meta.csv", index=False)
```

### **Step 2: Math Model (Math Learning)**

#### 2.1 Train Math Model
```bash
# Run the training notebook
jupyter notebook math_model_team2.ipynb
```

**🔧 REQUIRED FILE PATH REPLACEMENTS (Preprocessing Section):**

In the **preprocessing section** of `math_model_team2.ipynb`, replace:

```python
# REPLACE THESE PATHS WITH YOUR ACTUAL DATA LOCATIONS
df_main = pd.read_csv("./raw_data/training_set_with_formatted_time.csv")
df_ws = pd.read_csv("./raw_data/workspace_summary_train.csv")
df_scores = pd.read_csv("./raw_data/student_scores_train.csv")

# REPLACE THESE OUTPUT PATHS
df_main.to_csv('preprocessed_data/df_main_allws.csv', index=False)
df_ws.to_csv('preprocessed_data/df_ws_allws.csv', index=False)

# REPLACE THESE OUTPUT PATHS
df_main.to_csv("preprocessed_data/df_main.csv", index=False)
df_ws.to_csv("preprocessed_data/df_ws.csv", index=False)
df_scores.to_csv("preprocessed_data/df_scores.csv", index=False)
df_cleaned_math.to_csv("preprocessed_data/df_cleaned_math.csv", index=False)
```

#### 2.2 Test Math Model
```bash
# Run the test notebook
jupyter notebook math_test_team2.ipynb
```

**REQUIRED FILE PATH REPLACEMENTS (Preprocessing Section):**

In the **preprocessing section** of `math_test_team2.ipynb`, replace:

```python
# REPLACE THESE PATHS WITH YOUR ACTUAL TEST DATA LOCATIONS
df_main = pd.read_csv("./raw_data/training_set_with_formatted_time.csv")
df_ws = pd.read_csv("./raw_data/workspace_summary_train.csv")
df_scores = pd.read_csv("./raw_data/student_scores_train.csv")

# REPLACE THESE OUTPUT PATHS
df_main.to_csv('preprocessed_data/df_main_allws.csv', index=False)
df_ws.to_csv('preprocessed_data/df_ws_allws.csv', index=False)

# REPLACE THESE OUTPUT PATHS
df_main.to_csv("preprocessed_data/df_main.csv", index=False)
df_ws.to_csv("preprocessed_data/df_ws.csv", index=False)
df_scores.to_csv("preprocessed_data/df_scores.csv", index=False)
df_cleaned_math.to_csv("preprocessed_data/df_cleaned_math.csv", index=False)
```

### **Motivation Model**

#### 3.1 Train Motivation Model
```bash
# Run the training notebook
jupyter notebook motivation_model_team2.ipynb
```

**REQUIRED FILE PATH REPLACEMENTS (Preprocessing Section):**

In the **preprocessing section** of `motivation_model_team2.ipynb`, replace:

```python
# REPLACE THESE PATHS WITH YOUR ACTUAL DATA LOCATIONS
df_main = pd.read_csv("./raw_data/training_set_with_formatted_time.csv")
df_ws = pd.read_csv("./raw_data/workspace_summary_train.csv")
df_scores = pd.read_csv("./raw_data/student_scores_train.csv")

# REPLACE THESE OUTPUT PATHS
df_main.to_csv('preprocessed_data/df_main_allws.csv', index=False)
df_ws.to_csv('preprocessed_data/df_ws_allws.csv', index=False)

# REPLACE THESE OUTPUT PATHS
df_main.to_csv("preprocessed_data/df_main.csv", index=False)
df_ws.to_csv("preprocessed_data/df_ws.csv", index=False)
df_scores.to_csv("preprocessed_data/df_scores.csv", index=False)
df_cleaned_map.to_csv("preprocessed_data/df_cleaned_map.csv", index=False)
df_cleaned_se.to_csv("preprocessed_data/df_cleaned_se.csv", index=False)
```

#### 3.2 Test Motivation Model
```bash
# Run the test notebook
jupyter notebook motivation_test_team2.ipynb
```

**REQUIRED FILE PATH REPLACEMENTS (Preprocessing Section):**

In the **preprocessing section** of `motivation_test_team2.ipynb`, replace:

```python
# REPLACE THESE PATHS WITH YOUR ACTUAL TEST DATA LOCATIONS
df_main = pd.read_csv("./raw_data/training_set_with_formatted_time.csv")
df_ws = pd.read_csv("./raw_data/workspace_summary_train.csv")
df_scores = pd.read_csv("./raw_data/student_scores_train.csv")

# REPLACE THESE OUTPUT PATHS
df_main.to_csv('preprocessed_data/df_main_allws.csv', index=False)
df_ws.to_csv('preprocessed_data/df_ws_allws.csv', index=False)

# REPLACE THESE OUTPUT PATHS
df_main.to_csv("preprocessed_data/df_main.csv", index=False)
df_ws.to_csv("preprocessed_data/df_ws.csv", index=False)
df_scores.to_csv("preprocessed_data/df_scores.csv", index=False)
df_cleaned_map.to_csv("preprocessed_data/df_cleaned_map.csv", index=False)
df_cleaned_se.to_csv("preprocessed_data/df_cleaned_se.csv", index=False)
```

## Model Details

### **Meta Model (Classification)**
- **Target**: `Post3Meta` (Metacognition Assessment)
- **Models**: RandomForest, GradientBoosting, XGBoost
- **Evaluation**: Quadratic Weighted Kappa (QWK)
- **Features**: Learning behavior patterns, help-seeking behavior
- **Output**: `meta_model.pkl` (model, label_encoder, feature_columns)

### **Math Model (Regression)**
- **Target**: `PostMath` (Math Learning Outcomes)
- **Model**: ExtraTreesRegressor (single model)
- **Evaluation**: R², RMSE, MAE
- **Features**: Workspace completion, error rates, skills mastery
- **Output**: `math_model.pkl` (model, feature_columns)

### **Motivation Model (Classification)**
- **Target**: `PostMotivation3` (Average of PostSE and PostMAP)
- **Models**: RandomForest, GradientBoosting
- **Evaluation**: Quadratic Weighted Kappa (QWK)
- **Features**: MAP-specific and SE-specific behavioral patterns
- **Output**: `motivation_model.pkl` (model, feature_columns)

## Output Files

### **Trained Models**
- `meta_model.pkl` - Trained metacognition model
- `math_model.pkl` - Trained math model  
- `motivation_model.pkl` - Trained motivation model

### **Predictions**
- `meta_predictions.csv` - Metacognition predictions
- `math_predictions.csv` - Math predictions
- `motivation_predictions.csv` - Motivation predictions

### **Preprocessed Data**
- `df_main_allws.csv` - Main interaction data (all workspaces)
- `df_ws_allws.csv` - Workspace data (all workspaces)
- `df_main.csv` - Main interaction data (filtered)
- `df_ws.csv` - Workspace data (filtered)
- `df_scores.csv` - Student scores
- `df_cleaned_math.csv` - Cleaned math scores
- `df_cleaned_meta.csv` - Cleaned metacognition scores
- `df_cleaned_map.csv` - Cleaned MAP scores
- `df_cleaned_se.csv` - Cleaned SE scores

## Important Notes

1. **File Paths**: Always replace the file paths in the preprocessing sections with your actual data locations
2. **Order**: Train models before testing them
3. **Data Requirements**: Ensure all required CSV files are present in the correct directories
4. **Model Files**: Trained models (.pkl files) must be in the same directory as the test notebooks
5. **Memory**: Some notebooks may require significant memory for large datasets

## Troubleshooting

### Common Issues:
- **FileNotFoundError**: Check that all file paths are correctly specified
- **MemoryError**: Consider using smaller datasets or increasing system memory
- **ImportError**: Ensure all required libraries are installed via `requirements.txt`

### Getting Help:
If you encounter issues, check:
1. All file paths are correctly specified
2. All required libraries are installed
3. Data files are in the correct format
4. Sufficient system resources are available
