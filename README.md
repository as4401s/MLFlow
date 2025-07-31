# MLFlow

# Housing Price Prediction with ML Experiment Tracking using MLflow

This project demonstrates a machine learning workflow for predicting housing prices using various regression models. A key focus of this repository is to showcase the use of **MLflow** for robust experiment tracking, model management, and results comparison.

We explore three different regression models to solve this problem:
1.  **Linear Regression**
2.  **Random Forest Regressor**
3.  **XGBoost Regressor**

The scripts are written in Python and utilize popular data science libraries such as Pandas, Scikit-learn, and Matplotlib.

## What is MLflow and Why is it Important?

MLflow is an open-source platform for managing the end-to-end machine learning lifecycle. It tackles the challenges that arise when you move from a single notebook to a more structured machine learning project.

In any serious ML project, you will run many experiments. You'll change models, tweak hyperparameters, and modify features. Keeping track of which combination of code, data, and parameters produced which result becomes incredibly difficult. MLflow solves this by providing tools for:

1.  **Tracking Experiments**: Log parameters, code versions, metrics, and output files for each run.
2.  **Packaging Code**: Package ML code in a reusable, reproducible form.
3.  **Managing Models**: Manage and deploy models from various ML libraries to a variety of serving systems.

By integrating MLflow, we ensure our work is **reproducible**, **organized**, and **easy to compare**.

## Project in Action: The MLflow UI

The true power of MLflow is visualized in its UI. After running our experiments, we can launch the MLflow UI to see a comprehensive dashboard of our work.

### Centralized Model Registry

All the models we train are logged and versioned in one central place. This makes it easy to see which models have been trained, when they were created, and which experiment run they belong to.

![MLflow Models View](https://i.imgur.com/8FzWJtq.png)

### Comparing Performance Metrics

MLflow provides powerful visualization tools to compare the performance of different models. We can easily plot key metrics like `r2_score`, `mae`, `mse`, and `rmse` across all our runs to identify the best-performing model at a glance.

![MLflow Metrics Comparison](https://i.imgur.com/k6lWqV2.png)

### Tracking Hyperparameters

Reproducibility is critical. MLflow automatically logs all the hyperparameters for each run. If we discover that a particular model performed well, we can always go back and see the exact configuration that produced it. This eliminates guesswork and makes our results verifiable.

![MLflow Parameters View](https://i.imgur.com/00A9S7L.png)

## How to Run This Project

1.  **Clone the repository:**
    ```bash
    git clone [https://github.com/as4401s/MLFlow.git](https://github.com/as4401s/MLFlow.git)
    cd MLFlow
    ```

2.  **Install the required libraries:**
    ```bash
    pip install -r requirements.txt
    ```
    *(Note: You may need to create a `requirements.txt` file with pandas, scikit-learn, matplotlib, mlflow, and xgboost)*

3.  **Start the MLflow UI:**
    Open a terminal and run the following command. This will start a local tracking server.
    ```bash
    mlflow ui
    ```
    You can then access the UI by navigating to `http://127.0.0.1:5000` in your web browser.

4.  **Run the experiment scripts:**
    Open another terminal and run any of the Python scripts to train a model and log the results to MLflow.
    ```bash
    python linear_regression_with_mlflow.py
    python random_forest_with_mlflow.py
    python xgboost_with_mlflow.py
    ```

After running the scripts, refresh the MLflow UI in your browser to see the new runs, parameters, metrics, and models.
