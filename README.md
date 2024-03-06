<h1>
  Lung cancer preliminary risk assessment with decision trees
</h1>


🫁 Classify indiviual's lifestyle choice and health indicators to assess the risk of lung cancer.
<br> 📈 Investigate the performance of different models: Decision Trees, Random Forests, XGBoost, and LightGBM.

[![Python](https://img.shields.io/static/v1?message=Python&logo=python&labelColor=5c5c5c&color=3776AB&logoColor=white&label=%20)](https://www.python.org/)
[![Jupyter](https://img.shields.io/static/v1?message=Jupyter&logo=jupyter&labelColor=5c5c5c&color=F37626&logoColor=white&label=%20)](https://jupyter.org/)
[![NumPy](https://img.shields.io/static/v1?message=NumPy&logo=numpy&labelColor=5c5c5c&color=013243&logoColor=white&label=%20)](https://numpy.org/)
[![Pandas](https://img.shields.io/static/v1?message=Pandas&logo=pandas&labelColor=5c5c5c&color=150458&logoColor=white&label=%20)](https://pandas.pydata.org/)
[![scikit-learn](https://img.shields.io/static/v1?message=scikit-learn&logo=scikit-learn&labelColor=5c5c5c&color=F7931E&logoColor=white&label=%20)](https://scikit-learn.org/)

<u>Note</u>: I provided all codes used in this project on the Jupyter Notebook [here](https://github.com/phanuphatsrisukhawasu/lung-cancer-preliminary-risk-assessment/blob/main/lung-cancer-classification.ipynb).

<h2>
  🔎 Motivation
</h2>

Analyzing the risk of lung cancer based on lifestyle choices and health is beneficial for individuals who want to assess their health in the preliminary stages without meeting with experts. This project aims to utilize machine learning to predict the risk based on just the user's age and personal information measured in binarized format (having a "no" or "yes" choice).
<h2>
  🛠️ Methods
</h2>

In this project, I investigate the performance of different machine learning models in assessing the risk of lung cancer. First, I would like to extend my sincere gratitude to the author of the dataset utilized in this project, Shreyas Paraj-patil (the dataset is available on Kaggle [here](https://www.kaggle.com/datasets/shreyasparaj1/lung-cancer-dataset/data)). I used this dataset for all experiments.

In brief, I train Decision Tree, Random Forest, XGBoost, and LightGBM by first tuning them on the training set with 5-fold cross-validation. To ensure that I found the best parameters, I used `RandomizedSearchCV` to search for them. The dataset is imbalanced and small. However, I set the scope of this project as a model-centric approach.

<h2>
  📊 Summarized Results
</h2>
  
I evaluated the performance of each model based on the classification accuracy, precision, recall, and F1 Score. From the table below, I found that using a simple model like a decision tree acquired the best performance among other models. Its high precision and recall indicate its potential for accurately identifying lung cancer risk.

| Model | Accuracy | Precision | Recall | F1 Score |
| --- | --- | --- | --- | --- |
| Decision Tree | 0.9355 | 0.9630 | 0.9630 | 0.9630 |
| Random Forest | 0.9032 | 0.9138 | 0.9815 | 0.9464 |
| XGBoost | 0.9032 | 0.9138 | 0.9815 | 0.9464 |
| LightGBM | 0.9298 | 0.9815 | 0.9550 | 0.9464 |

Although this method sounds promising, one should note that the prediction relies on a very imprecise measurement of an individual's activities. Incorporating data with more precise categories for each feature is a great direction.

<h2>
  🧑🏻‍🏫 References
</h2>

*Lung cancer dataset*. (2024, February 23). Kaggle. https://www.kaggle.com/datasets/shreyasparaj1/lung-cancer-dataset/data
