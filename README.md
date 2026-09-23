# 🍽️ Zomato Restaurant Clustering – Unsupervised Machine Learning

## 📌 Project Overview

This project analyzes **Zomato restaurant reviews and restaurant metadata** to understand customer behavior, restaurant characteristics, and customer sentiment using **Exploratory Data Analysis (EDA), Sentiment Analysis, and Unsupervised Machine Learning techniques**.

The project applies multiple clustering algorithms to identify meaningful groups within the dataset and evaluates their performance using the **Silhouette Score**.

The main objective is to extract useful business insights that can support **customer segmentation, targeted marketing, personalization, and restaurant-level decision making**.

---

## 🎯 Problem Statement

The objective of this project is to analyze restaurant reviews and customer-related data to:

* Understand customer ratings and restaurant characteristics
* Analyze customer review sentiment
* Identify patterns and relationships in the data
* Segment similar records using unsupervised machine learning
* Compare different clustering algorithms
* Identify the clustering approach that provides meaningful customer/restaurant segments

---

## 📊 Dataset

The project uses two datasets:

### 1. Zomato Restaurant Reviews Dataset

Contains information such as:

* Restaurant Name
* Reviewer Name
* Review Text
* Rating
* Reviewer Metadata
* Review Time
* Number of Pictures

### 2. Zomato Restaurant Metadata Dataset

Contains information such as:

* Restaurant Name
* Restaurant Link
* Cost for Two
* Collections
* Cuisines
* Timings

The two datasets were merged using the **restaurant name** after standardizing the names.

---

## 🛠️ Technologies & Libraries Used

### Programming Language

* Python

### Data Manipulation

* Pandas
* NumPy

### Data Visualization

* Matplotlib
* Seaborn

### Natural Language Processing

* NLTK
* TextBlob
* Stopwords
* WordNet Lemmatizer

### Machine Learning

* Scikit-learn

### Machine Learning Algorithms

* K-Means Clustering
* Hierarchical / Agglomerative Clustering
* DBSCAN

### Dimensionality Reduction

* PCA

### Evaluation Metric

* Silhouette Score
* Davies-Bouldin Score

---

## 🔄 Project Workflow

```text
Dataset Collection
       ↓
Data Loading
       ↓
Data Understanding
       ↓
Data Cleaning & Preprocessing
       ↓
Exploratory Data Analysis
       ↓
Data Visualization
       ↓
Text Preprocessing
       ↓
Sentiment Analysis
       ↓
Feature Engineering
       ↓
Feature Scaling
       ↓
PCA
       ↓
Clustering Models
       ↓
Model Evaluation
       ↓
Hyperparameter Tuning
       ↓
Model Comparison
       ↓
Business Insights
```

---

## 🧹 Data Cleaning & Preprocessing

The following preprocessing steps were performed:

* Standardized restaurant names
* Removed unnecessary spaces
* Converted restaurant names to lowercase
* Merged the reviews and restaurant metadata datasets
* Converted the `Cost` column into numeric format
* Removed commas from cost values
* Handled missing cost values using the median
* Filled missing review values
* Filled missing collection and timing values
* Checked duplicate records
* Prepared a clean dataset for further analysis

These steps improved the quality and consistency of the dataset before performing analysis and machine learning.

---

## 📈 Exploratory Data Analysis

Multiple visualizations were created to understand the dataset.

Some of the analyses include:

* Distribution of customer ratings
* Distribution of restaurant cost
* Most reviewed restaurants
* Restaurant characteristics
* Cuisine-related analysis
* Customer review patterns
* Sentiment distribution
* Relationships between numerical and categorical variables
* Multivariate analysis

The project follows the **UBM approach**:

* **U – Univariate Analysis**
* **B – Bivariate Analysis**
* **M – Multivariate Analysis**

---

## 💬 Sentiment Analysis

Customer reviews were analyzed using **TextBlob**.

A sentiment polarity score was generated for each review.

The sentiment was classified into three categories:

```text
Positive
Negative
Neutral
```

The project calculates sentiment polarity and converts the resulting scores into sentiment labels.

### Business Use

Sentiment analysis can help identify:

* Positive customer experiences
* Negative customer feedback
* Potential service issues
* Frequently discussed customer concerns
* Reviews that may be useful for promotional analysis

---

# 🤖 Machine Learning

## 1. K-Means Clustering

K-Means clustering was initially implemented with:

```text
Number of clusters (K) = 3
```

The model was trained using scaled features.

PCA was subsequently used for visualizing the clusters.

The **Silhouette Score** was used to measure the quality of clustering.

### Hyperparameter Tuning

Different values of K from **2 to 8** were tested.

The best result obtained during tuning was:

```text
K = 5
Silhouette Score ≈ 0.408
```

This showed improved cluster separation compared with the initial configuration.

---

## 2. Hierarchical Clustering

Agglomerative / Hierarchical Clustering was also implemented.

Different linkage methods were evaluated, including:

* Ward
* Complete
* Average

Different numbers of clusters were also tested.

The project reports that **complete and average linkage with 2 clusters produced a Silhouette Score of approximately 0.86**.

---

## 3. DBSCAN

DBSCAN was implemented using:

```text
eps = 0.5
min_samples = 5
```

DBSCAN was evaluated using the Silhouette Score after excluding noise points from the score calculation.

### Hyperparameter Tuning

Different `eps` values were tested:

```text
0.3
0.5
0.7
1.0
```

The project reports an improvement from approximately:

```text
Initial Silhouette Score = 0.19
Best tuned score = 0.58
```

with the best reported result occurring at `eps = 1.0`.

---

## 📊 Model Comparison

| Model                   | Tuning / Configuration               |    Reported Result |
| ----------------------- | ------------------------------------ | -----------------: |
| K-Means                 | K = 5                                | Silhouette ≈ 0.408 |
| Hierarchical Clustering | Complete/Average linkage, 2 clusters |  Silhouette ≈ 0.86 |
| DBSCAN                  | eps = 1.0                            |  Silhouette ≈ 0.58 |

The project identifies **Hierarchical Clustering** as the final selected model based on the reported Silhouette Score and the resulting cluster separation.

---

## 📏 Evaluation Metric

### Silhouette Score

The Silhouette Score measures:

* How well data points fit within their assigned clusters
* How clearly different clusters are separated

A higher score indicates stronger cluster separation.

In this project, Silhouette Score was used to compare clustering configurations and support model selection.

---

## 💡 Business Insights

The analysis provides several potential business applications:

### Customer Segmentation

Clustering can help identify groups of customers or restaurant records with similar characteristics.

### Targeted Marketing

Different customer segments can potentially receive different offers and promotional campaigns.

### Personalization

Restaurant preferences and customer behavior can be used to support personalized recommendations.

### Customer Experience

Sentiment analysis can help identify positive and negative customer feedback.

### Restaurant Strategy

Restaurant cost, ratings, cuisines, and customer feedback can provide insights into restaurant positioning and customer preferences.

---

## 📌 Key Skills Demonstrated

This project demonstrates practical knowledge of:

* Python
* Pandas
* NumPy
* Data Cleaning
* Data Preprocessing
* Exploratory Data Analysis
* Data Visualization
* Natural Language Processing
* Sentiment Analysis
* Feature Engineering
* Feature Scaling
* PCA
* K-Means Clustering
* Hierarchical Clustering
* DBSCAN
* Hyperparameter Tuning
* Model Evaluation
* Business Insights

---



> Add the CSV datasets to the repository only if their licensing/redistribution terms allow it. Otherwise, provide instructions for obtaining the datasets.

---

## 🚀 How to Run the Project

### 1. Clone the repository

```bash
git clone https://github.com/SaimaheshGangisetty/Zomato-Restaurant-Clustering-Unsupervised-ML.git
```

### 2. Navigate to the project folder

```bash
cd Zomato-Restaurant-Clustering-Unsupervised-ML
```

### 3. Install required libraries

```bash
pip install pandas numpy matplotlib seaborn scikit-learn nltk textblob
```

### 4. Open the Jupyter Notebook

```bash
jupyter notebook
```

Open:

```text
Zomato_Restaurant_Clustering_Unsupervised_ML.ipynb
```

### 5. Run the notebook

Make sure the required datasets are available at the paths expected by the notebook.

---

## 🔗 Google Colab

The notebook contains a Google Colab integration for opening the project directly in Colab.

---

## 👨‍💻 Author

**Sai Mahesh Gangisetty**

Machine Learning / Data Science Project

---

## ⭐ Project Highlights

```text
✔ Data Cleaning & Preprocessing
✔ Exploratory Data Analysis
✔ 15+ Data Visualizations
✔ Customer Review Sentiment Analysis
✔ Feature Engineering
✔ Feature Scaling
✔ PCA
✔ K-Means Clustering
✔ Hierarchical Clustering
✔ DBSCAN
✔ Hyperparameter Tuning
✔ Silhouette Score Evaluation
✔ Business Insights
```
