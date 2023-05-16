# Sampling-

This project aims to develop a credit card fraud detection system using machine learning techniques. The goal is to identify fraudulent transactions in a dataset and improve the accuracy of detection by applying resampling techniques.

## Dataset

The dataset used in this project is stored in the file `Creditcard_data.csv`. It contains transaction data, including various features and a target variable indicating whether a transaction is fraudulent or not.

## Data Preprocessing

To prepare the data for analysis, the following steps are performed:

- Loading the dataset using pandas and examining the first 10 rows.
- Checking the information of the dataset, including data types and missing values.
- Visualizing missing values using a heatmap.
- Applying MinMaxScaler to scale the numerical features.

## Resampling Techniques

To address the class imbalance issue in the dataset, two resampling techniques are applied:

- SMOTE (Synthetic Minority Over-sampling Technique): It generates synthetic samples for the minority class (fraudulent transactions) to balance the class distribution.
- ADASYN (Adaptive Synthetic Sampling): It focuses on generating samples in regions where the density of minority class examples is low.

The resampled datasets (`df_smote` and `df_adasyn`) are created by combining the generated samples with the original dataset.

## Model Selection and Evaluation

Several machine learning models are used to train and evaluate the fraud detection system. The following models are employed:

- Logistic Regression
- Random Forest Classifier
- Gaussian Naive Bayes
- Decision Tree Classifier
- Support Vector Classifier

The accuracy scores of each model are computed using train-test split on the resampled datasets.

## Sampling Techniques

Different sampling techniques are implemented to create different subsets of the balanced dataset for evaluation purposes.

- Simple Random Sampling: A random subset of the balanced dataset is selected.
- Systematic Sampling: Samples are selected at fixed intervals from the balanced dataset.
- Stratified Sampling: Samples are selected from each class proportionally to their occurrence in the balanced dataset.
- Cluster Sampling: Samples are selected based on random clusters from the balanced dataset.
- Snowball Sampling: Initial samples are selected from the minority class, and subsequent samples are added based on referrals from the initial participants.

Accuracy scores are calculated for each sampling technique using the selected samples.

## Usage

To run the project, perform the following steps:

1. Clone the repository to your local machine.
2. Install the required dependencies and libraries specified in the project.
3. Run the Python script or Jupyter Notebook to execute the code and generate the results.

## Dependencies

The project requires the following libraries:

- NumPy
- pandas
- seaborn
- scikit-learn
- imbalanced-learn

Please make sure to install these dependencies before running the code.

## License

This project is licensed under the MIT License. You can find more details in the `LICENSE` file.

## Acknowledgments

- The credit card fraud dataset used in this project is sourced from [Kaggle](https://www.kaggle.com/mlg-ulb/creditcardfraud).
- The resampling techniques are implemented using the `imbalanced-learn` library.
- The machine learning models are from scikit-learn.


