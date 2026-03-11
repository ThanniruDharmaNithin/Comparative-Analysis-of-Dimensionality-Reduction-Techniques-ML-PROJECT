# 🚢 Comparative Analysis of Dimensionality Reduction Techniques for Predicting Survival on the Titanic

**Author:** Thanniru Dharma Nithin  

---

## 📝 Overview
High-dimensional data can make machine learning models slow, hard to interpret, and prone to mistakes. Dimensionality reduction helps by compressing this data into a simpler form without losing important information.  

In this project, we compare **Principal Component Analysis (PCA)** and **Linear Discriminant Analysis (LDA)** to predict which passengers survived on the Titanic.  

- **🔹 PCA**: Unsupervised method that captures most of the data’s variance while reducing noise.  
- **🔹 LDA**: Supervised method that focuses on separating classes to improve prediction accuracy.  

We test these techniques with popular classifiers: **Logistic Regression, Random Forest, Decision Tree, and Support Vector Machine (SVM)**. The results show that LDA often gives better predictions because it uses information about the class labels.  

**Keywords:** PCA, LDA, dimensionality reduction, machine learning, Titanic dataset, classification, preprocessing, model evaluation.

---

## 🌟 Why This Study Matters
Working with high-dimensional data comes with challenges: models become slower, harder to interpret, and may overfit. By comparing PCA and LDA, this study helps identify which technique works best for improving model accuracy and interpretability.  

### 🎯 Goals
- Prepare and clean the Titanic dataset  
- Reduce dimensionality using PCA and LDA  
- Train multiple classifiers  
- Compare results using accuracy and other metrics  
- Provide guidance for choosing the right technique  

### 👥 Who Can Benefit
- Data scientists and machine learning practitioners  
- Students and educators in data science  
- Anyone working with complex datasets  

### 🌐 Applications
- **Healthcare:** Predicting patient outcomes  
- **Finance:** Risk analysis and predictive modeling  
- **Marketing:** Customer segmentation  
- **Bioinformatics:** Gene expression analysis  
- **Image Recognition:** Object detection and classification  

---

## 🛠 Data Preparation
Before modeling, the data needs cleaning and transformation:  

1. **Missing Values**  
   - Fill `Age` with the median  
   - Fill `Embarked` with the most common value  

2. **Irrelevant Columns**  
   - Drop `PassengerId`, `Name`, `Ticket`, `Cabin`  

3. **Encoding Categorical Data**  
   - Convert `Sex` and `Embarked` into numerical columns (one-hot encoding)  

### ⚡ Splitting and Scaling
- Split the dataset: **70% training, 30% testing**  
- Scale numerical features like `Age` and `Fare` using **StandardScaler**  

---

## 🧩 Model Training
We trained four classifiers to see how they perform after dimensionality reduction:  
- Logistic Regression  
- Random Forest Classifier  
- Decision Tree Classifier  
- Support Vector Machine (SVM)  

**Hyperparameter tuning** was done using **GridSearchCV** to get the best results.

---

## 📉 Dimensionality Reduction
- **PCA:** Reduced data to 2 components (easy to visualize)  
- **LDA:** Reduced to 1 component (maximizes class separation)  

We trained models on both PCA and LDA transformed data and visualized the decision boundaries to understand how well each technique separates survivors from non-survivors.

---

## 📊 Results

### PCA Performance
| Model | Accuracy |
|-------|---------|
| Logistic Regression | 64.93% |
| Random Forest | 69.40% |
| Decision Tree | 66.04% |
| SVC | 67.91% |

**Observation:** Random Forest gave the best results with PCA.

### LDA Performance
| Model | Accuracy |
|-------|---------|
| Logistic Regression | 80.97% |
| Random Forest | 77.99% |
| Decision Tree | 79.10% |
| SVC | 80.97% |

**Observation:** LDA clearly improves performance. Logistic Regression and SVC did the best here.  

---

## 📈 Insights
- LDA consistently improves model accuracy compared to PCA  
- Logistic Regression improved from **64.93% → 80.97%**  
- Random Forest improved from **69.40% → 77.99%**  
- Decision Tree improved from **66.04% → 79.10%**  
- SVC improved from **67.91% → 80.97%**  

**Takeaway:** Using class information (as in LDA) really helps classifiers make better predictions.

---

## 🏁 Conclusion
- **PCA:** Good for reducing noise and exploring data  
- **LDA:** Better for classification tasks, higher accuracy, clearer class separation  
- **Best Combination:** Logistic Regression with LDA (80.97% accuracy)  

**Future Work:**  
- Explore hybrid approaches like PCA + LDA, t-SNE, or autoencoders  
- Use these techniques in deep learning pipelines  
- Investigate non-linear methods for more complex data  

---
