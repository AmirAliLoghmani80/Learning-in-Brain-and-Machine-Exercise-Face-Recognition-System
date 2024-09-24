# Learning in Brain and Machine: Face Recognition System Using Various Feature Selection Methods and Classification Models

This project explores the development of a face recognition system using different feature selection techniques and classification models. The goal is to find the most optimal combination of feature selectors and classifiers that provide the best accuracy on the ORL face dataset.

## Project Overview

The dataset used in this project is the **ORL Collection of Faces**, consisting of 400 images from 40 individuals (10 images per person). The dataset is split into a training set of 5 images per person (200 samples) and a test set of 5 images per person (200 samples). The project involves the following steps:

1. **Feature Extraction**: Principal Component Analysis (PCA) is applied to reduce the dimensionality of the data, retaining the top 50 principal components.
2. **Feature Selection**: Three different feature selection methods are used:
   - Sequential Floating Forward Selection (SFFS)
   - Mutual Information (MI)
   - Correlation Coefficients
3. **Classification**: Five classification models are tested on the selected features:
   - k-Nearest Neighbor (k-NN)
   - Support Vector Machine (SVM)
   - Decision Tree
   - Logistic Regression
   - Parzen Window

### Key Objectives
- Develop and compare different classification models for face recognition.
- Examine how different feature selection methods impact the performance of classification models.
- Evaluate the models under various conditions, including noisy and altered brightness test sets.

## Methods

### 1. Principal Component Analysis (PCA)
PCA is used to extract the top 50 principal components, providing a reduced feature set that captures the maximum variance in the data.

### 2. Feature Selection Methods
- **Sequential Floating Forward Selection (SFFS)**: Iteratively adds and removes features to maximize classification accuracy.
- **Mutual Information (MI)**: Measures the dependency between features and class labels.
- **Correlation Coefficients**: Evaluates the linear relationships between features, allowing the removal of redundant features.

### 3. Classification Models
- **k-NN**: Uses the nearest neighbors to classify an image based on a majority vote.
- **SVM**: Finds an optimal hyperplane for separating different classes.
- **Logistic Regression**: A probabilistic model used for binary classification.
- **Decision Tree**: Splits data into decision nodes based on feature values.
- **Parzen Window**: A non-parametric technique for estimating probability density functions.

## Results

The accuracies of the models combined with different feature selection techniques on the test set are summarized below:

| Classification Model  | PCA  | PCA + SFFS | PCA + MI | PCA + Correlation Coefficients |
|-----------------------|------|------------|----------|-------------------------------|
| k-NN                  | 0.86 | 0.91       | 0.855    | 0.705                         |
| Logistic Regression    | 0.82 | 0.87       | 0.895    | 0.72                          |
| Decision Tree         | 0.375| 0.495      | 0.35     | 0.30                          |
| Parzen Window         | 0.86 | —          | 0.855    | 0.705                         |
| SVM                   | 0.915| 0.90       | 0.885    | 0.735                         |
| Bayes                 | 0.425| 0.425      | 0.465    | 0.315                         |

The best accuracy (91.5%) was achieved using **SVM** with PCA. However, **k-NN** combined with **SFFS** also provided competitive results.

### Testing Under Different Conditions
1. **Noisy Test Set**: The models were tested on images with salt-and-pepper noise, where 2% of pixels were randomly altered. The k-NN model with SFFS performed best under this condition.
2. **Decreased Brightness**: Images with 50% reduced brightness were used for testing, and again, k-NN combined with SFFS showed the best accuracy.
3. **Varying Number of PCA Components**: The models were evaluated with different numbers of principal components (35, 50, 60, and 70). SVM with SFFS consistently performed well.

### Effect of Training Set Size
The accuracy of models improved with larger training set sizes. For example, when using 320 training samples, the SVM model achieved 95% accuracy with PCA.

## Conclusion

This project demonstrates the effectiveness of combining **SFFS** feature selection with **k-NN** and **SVM** classification models for face recognition tasks. These combinations provided the highest accuracy across various conditions, including noisy and darkened images. The results indicate that careful selection of features and classifiers can significantly improve model performance in face recognition applications.

## Instructions

1. **Run the Code**: The MATLAB or Python scripts are provided for feature extraction (PCA), feature selection (SFFS, MI, Correlation), and classification (k-NN, SVM, etc.).
2. **Train the Models**: Train the models using the training set and evaluate them using the test set.
3. **Test with Different Conditions**: Test the trained models under noisy and altered brightness conditions to assess their robustness.

---

This README provides an overview of the project and instructions for running the models. Let me know if you'd like to modify or add anything!Here is a README file based on the content of the report you uploaded:

---

# Face Recognition System Using Various Feature Selection Methods and Classification Models

This project explores the development of a face recognition system using different feature selection techniques and classification models. The goal is to find the most optimal combination of feature selectors and classifiers that provide the best accuracy on the ORL face dataset.

## Project Overview

The dataset used in this project is the **ORL Collection of Faces**, consisting of 400 images from 40 individuals (10 images per person). The dataset is split into a training set of 5 images per person (200 samples) and a test set of 5 images per person (200 samples). The project involves the following steps:

1. **Feature Extraction**: Principal Component Analysis (PCA) is applied to reduce the dimensionality of the data, retaining the top 50 principal components.
2. **Feature Selection**: Three different feature selection methods are used:
   - Sequential Floating Forward Selection (SFFS)
   - Mutual Information (MI)
   - Correlation Coefficients
3. **Classification**: Five classification models are tested on the selected features:
   - k-Nearest Neighbor (k-NN)
   - Support Vector Machine (SVM)
   - Decision Tree
   - Logistic Regression
   - Parzen Window

### Key Objectives
- Develop and compare different classification models for face recognition.
- Examine how different feature selection methods impact the performance of classification models.
- Evaluate the models under various conditions, including noisy and altered brightness test sets.

## Methods

### 1. Principal Component Analysis (PCA)
PCA is used to extract the top 50 principal components, providing a reduced feature set that captures the maximum variance in the data.

### 2. Feature Selection Methods
- **Sequential Floating Forward Selection (SFFS)**: Iteratively adds and removes features to maximize classification accuracy.
- **Mutual Information (MI)**: Measures the dependency between features and class labels.
- **Correlation Coefficients**: Evaluates the linear relationships between features, allowing the removal of redundant features.

### 3. Classification Models
- **k-NN**: Uses the nearest neighbors to classify an image based on a majority vote.
- **SVM**: Finds an optimal hyperplane for separating different classes.
- **Logistic Regression**: A probabilistic model used for binary classification.
- **Decision Tree**: Splits data into decision nodes based on feature values.
- **Parzen Window**: A non-parametric technique for estimating probability density functions.

## Results

The accuracies of the models combined with different feature selection techniques on the test set are summarized below:

| Classification Model  | PCA  | PCA + SFFS | PCA + MI | PCA + Correlation Coefficients |
|-----------------------|------|------------|----------|-------------------------------|
| k-NN                  | 0.86 | 0.91       | 0.855    | 0.705                         |
| Logistic Regression    | 0.82 | 0.87       | 0.895    | 0.72                          |
| Decision Tree         | 0.375| 0.495      | 0.35     | 0.30                          |
| Parzen Window         | 0.86 | —          | 0.855    | 0.705                         |
| SVM                   | 0.915| 0.90       | 0.885    | 0.735                         |
| Bayes                 | 0.425| 0.425      | 0.465    | 0.315                         |

The best accuracy (91.5%) was achieved using **SVM** with PCA. However, **k-NN** combined with **SFFS** also provided competitive results.

### Testing Under Different Conditions
1. **Noisy Test Set**: The models were tested on images with salt-and-pepper noise, where 2% of pixels were randomly altered. The k-NN model with SFFS performed best under this condition.
2. **Decreased Brightness**: Images with 50% reduced brightness were used for testing, and again, k-NN combined with SFFS showed the best accuracy.
3. **Varying Number of PCA Components**: The models were evaluated with different numbers of principal components (35, 50, 60, and 70). SVM with SFFS consistently performed well.

### Effect of Training Set Size
The accuracy of models improved with larger training set sizes. For example, when using 320 training samples, the SVM model achieved 95% accuracy with PCA.

## Conclusion

This project demonstrates the effectiveness of combining **SFFS** feature selection with **k-NN** and **SVM** classification models for face recognition tasks. These combinations provided the highest accuracy across various conditions, including noisy and darkened images. The results indicate that careful selection of features and classifiers can significantly improve model performance in face recognition applications.
