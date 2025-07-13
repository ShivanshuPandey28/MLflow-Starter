# MLflow-Starter Summary 

## Overview
This repository contains a collection of Jupyter notebooks demonstrating the use of MLflow for machine learning experiment tracking, model management, and deployment. The project includes examples of setting up a local MLflow tracking server, logging experiments, hyperparameter tuning, and model inference using various datasets such as Iris and California Housing.

## Key Notebooks
- **get-startted.ipynb**: Demonstrates the basic setup of an MLflow tracking server on localhost[](http://127.0.0.1:5000) and logs simple metrics (e.g., "Shiva" and "Anya") to the "Check Localhost Tracking URI" experiment.
- **housepricepredict.ipynb**: Implements a RandomForestClassifier to predict house prices using the California Housing dataset. It includes data preprocessing, train-test splitting, hyperparameter tuning with GridSearchCV, and logging metrics (e.g., MSE) and parameters to MLflow.
- **gettingstartedd.ipynb**: Provides a comprehensive guide to MLflow, including installation, setting up a tracking server, training a LogisticRegression model on the Iris dataset, logging hyperparameters and accuracy (93.33%), registering the model ("tracking-quickstart"), and performing inference.

## Key Features
- **Experiment Tracking**: Logs metrics, parameters, and models to MLflow experiments for reproducibility.
- **Model Management**: Registers models (e.g., "tracking-quickstart") with versioning support.
- **Hyperparameter Tuning**: Uses GridSearchCV to optimize RandomForestClassifier hyperparameters (e.g., n_estimators, max_depth).
- **Inference**: Loads and predicts using logged models via MLflow’s pyfunc flavor.

## Datasets
- **Iris**: Used for LogisticRegression classification with features like sepal length and petal width.
- **California Housing**: Used for house price prediction with features like median income and house age.

## Installation
- Install dependencies: `pip install mlflow pandas scikit-learn`
- Start MLflow server: `mlflow server --host 127.0.0.1 --port 5000`

## Usage
1. Run the notebooks in sequence to set up the tracking server and execute experiments.
2. View results in the MLflow UI at http://127.0.0.1:5000.
3. Load and test models using the provided URIs (e.g., `runs:/<run_id>/iris_model` or `models:/tracking-quickstart/latest`).
