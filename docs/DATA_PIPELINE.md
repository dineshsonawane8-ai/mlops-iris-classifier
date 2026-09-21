# Data Pipeline Documentation

## Pipeline Flow

collect -> preprocess -> features -> validate

## 1. Collect

Input:
- Iris dataset from sklearn

Output:
- data/raw/iris_raw.csv

Purpose:
- Collects the Iris dataset and stores it as a raw CSV file.

## 2. Preprocess

Input:
- data/raw/iris_raw.csv

Output:
- data/processed/iris_preprocessed.csv

Purpose:
- Removes duplicate rows and prepares the dataset for feature engineering.

## 3. Features

Input:
- data/processed/iris_preprocessed.csv

Output:
- data/processed/iris_features.csv

Purpose:
- Performs feature engineering and generates the required features.

## 4. Validate

Input:
- data/processed/iris_features.csv

Output:
- Validation result

Purpose:
- Checks the dataset for expected rows, columns and valid values.

## DVC Pipeline

The pipeline is managed by DVC using dvc.yaml.

Pipeline dependency graph:

collect -> preprocess -> features -> validate