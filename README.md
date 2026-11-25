
# Estimating Human Ratings from Face Images

### Machine Learning Project | Neural Ninjas | Batch A3

## 1. Project Overview

This project uses classical machine learning techniques to estimate
the average human rating associated with a face image.

The project uses the SCUT-FBP5500 dataset and treats the task as
a supervised regression problem.

The predicted score represents an aggregate human rating. It is
not an objective measure of beauty, personal worth, or suitability.

## 2. Dataset

- Dataset: SCUT-FBP5500
- Number of images: 5,500
- Ratings per image: 60
- Rating scale: 1 to 5
- Task: Regression
- Target: Mean human rating

The dataset is not included in this repository. Users must obtain
it separately and follow its applicable terms of use.

## 3. Feature Extraction

Two handcrafted image representations were explored:

- HOG (Histogram of Oriented Gradients): 8,100 features
- RGB Colour Histogram: 96 features

HOG features were more effective for the final model.

## 4. Machine Learning Models

The following classical regression approaches were compared:

- Linear Regression
- Ridge Regression
- Random Forest Regressor
- Support Vector Regression (SVR)
- Dummy Regressor as a baseline

PCA and feature selection were also compared.

No deep learning models were used.

## 5. Final Model

The selected model is Support Vector Regression (SVR)
using HOG features and PCA dimensionality reduction.

## 6. Final Evaluation Results

Evaluation on the predefined 2,200-image test set:

| Metric | Result |
|---|---:|
| MAE | 0.3442 |
| RMSE | 0.4500 |
| R2 Score | 0.5599 |
| Median Absolute Error | 0.2695 |

Five-fold cross-validation results:

- Mean MAE: 0.3412
- Mean RMSE: 0.4496
- Mean R2 Score: 0.5726

## 7. Running the Project

1. Download the SCUT-FBP5500 dataset separately.
2. Open the Jupyter notebook in Google Colab.
3. Install the required Python libraries if necessary.
4. Set the dataset path according to the notebook.
5. Run the notebook cells in order.

The saved model can also be used through the prediction
function provided in the notebook.

## 8. Limitations and Responsible Use

- Human ratings are subjective and may vary between raters.
- The model may overestimate lower ratings and underestimate
  higher ratings.
- Generalisation to images outside this dataset is not established.
- Subject identity groups were not available for a verified
  subject-wise split.
- Fairness across demographic groups has not been established.
- The model must not be used for decisions about individuals.

This project is an educational machine learning experiment only.
Its predictions should not be treated as objective judgements.

## 9. Technologies Used

- Python
- NumPy
- Pandas
- Matplotlib
- Seaborn
- Scikit-learn
- Scikit-image
- OpenPyXL
- Joblib
- Google Colab

## 10. Team

Neural Ninjas - Batch A3
