# Music Genre Classification Using Machine Learning

## 1. Project Overview

Music Genre Classification is a supervised machine learning project that predicts the genre of a music sample using extracted audio features.

The project explores and compares multiple classification algorithms to identify the model that performs best on the given dataset.

## 2. Problem Statement

Music can be categorized into different genres based on characteristics such as rhythm, frequency distribution, and timbral properties. The objective of this project is to use extracted audio features to classify music samples into one of ten genres.

## 3. Dataset

The project uses an extracted-feature music dataset containing approximately 10,000 audio segments and 58 input features, along with a filename and genre label.

The dataset includes the following genres:

- Blues
- Classical
- Country
- Disco
- Hip-hop
- Jazz
- Metal
- Pop
- Reggae
- Rock

The notebook uses `features_3_sec.csv`.

**Dataset setup:** Download the dataset from its original source and place `features_3_sec.csv` inside the `data/` directory. The dataset files are not included in this repository.

## 4. Machine Learning Models

The following supervised machine learning algorithms were implemented and evaluated:

1. Logistic Regression
2. K-Nearest Neighbors (KNN)
3. Decision Tree
4. Support Vector Machine (SVM)
5. Random Forest
6. Perceptron

## 5. Methodology

The project follows these steps:

1. Load and inspect the dataset.
2. Perform exploratory data analysis and visualize genre distribution.
3. Check for missing values and duplicate records.
4. Separate input features and target labels.
5. Split the data into training and testing sets while keeping segments from the same original song together.
6. Standardize the input features where required.
7. Train and evaluate six supervised learning models.
8. Compare model accuracies and evaluate the best-performing model using a confusion matrix.
9. Predict the genre of individual test samples.

## 6. Results

The best-performing model in the current experiments was **Random Forest**, with a test accuracy of **70.77%**.

| Model | Test Accuracy |
|---|---:|
| Logistic Regression | 68.07% |
| K-Nearest Neighbors | 65.72% |
| Decision Tree | 50.85% |
| Support Vector Machine | 67.37% |
| Random Forest | **70.77%** |
| Perceptron | 53.40% |

Random Forest was selected as the final model because it achieved the highest test accuracy among the six evaluated algorithms.

## 7. Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- Jupyter Notebook

## 8. Project Structure

```text
Music_genre_classification/
├── data/
│   └── features_3_sec.csv
├── notebooks/
│   └── 01_data_exploration.ipynb
├── results/
│   └── genre_distribution.png
├── src/
├── README.md
└── requirements.txt
```

The dataset is stored locally and is not committed to the repository. The `src/` directory is currently reserved for additional source code.

## 9. How to Run the Project

### Prerequisites

Install Python and Jupyter Notebook.

### Installation

Clone the repository:

```bash
git clone https://github.com/Deepthinreddy/Music_genre_classification.git
cd Music_genre_classification
```

Install the required libraries:

```bash
pip install -r requirements.txt
```

Place the downloaded `features_3_sec.csv` file in the `data/` directory.

Open the notebook:

```bash
jupyter notebook
```

Navigate to `notebooks/01_data_exploration.ipynb` and run the cells in order.

**Note:** The dataset path in the notebook must match the actual location of the CSV file.

## 10. Conclusion

This project demonstrates the application of supervised machine learning to music genre classification using extracted audio features. Six classification algorithms were implemented and compared. Random Forest achieved the highest test accuracy of 70.77% and was selected as the final model.

The project also demonstrates exploratory data analysis, preprocessing, model evaluation, confusion matrix analysis, and genre prediction on individual test samples.
