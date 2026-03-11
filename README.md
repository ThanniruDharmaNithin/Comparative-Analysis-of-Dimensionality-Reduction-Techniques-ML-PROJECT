# Comparative Analysis of Dimensionality Reduction Techniques for Predicting Survival on the Titanic

**Author:** Thanniru Dharma Nithin

## Abstract
Dimensionality reduction techniques play a crucial role in enhancing the efficiency and interpretability of machine learning models by transforming high-dimensional data into lower-dimensional representations. This project compares **Principal Component Analysis (PCA)** and **Linear Discriminant Analysis (LDA)** for predicting survival on the Titanic dataset.  

- **PCA**: An unsupervised technique that captures maximum variance and reduces noise.  
- **LDA**: A supervised method that maximizes class separability to improve classification accuracy.  

We evaluate the impact of these techniques using classifiers such as **Logistic Regression, Random Forest, Decision Tree, and Support Vector Machine (SVM)**. The results highlight that LDA often outperforms PCA in classification tasks due to its utilization of class-specific information.

**Keywords:** PCA, LDA, dimensionality reduction, machine learning, classification, Titanic dataset, data preprocessing, model evaluation.

---

## Introduction
Dimensionality reduction is essential for improving model performance and interpretability, especially in high-dimensional datasets. This study aims to explore and compare PCA and LDA in predicting Titanic passenger survival, evaluating their impact on multiple classifiers.

### Scope
The study focuses on:  
- Exploring PCA and LDA, including theoretical principles.  
- Applying these techniques to the Titanic dataset.  
- Training and evaluating classifiers: Logistic Regression, Random Forest, Decision Tree, SVM.  
- Visualizing decision boundaries in reduced dimensions.  
- Drawing insights on the strengths and limitations of each method.

### Prime Beneficiaries
- Data scientists and machine learning practitioners working with high-dimensional data.  
- Educators and students in data science and machine learning.  

### Application Areas
- **Bioinformatics**: Gene expression analysis.  
- **Image Recognition**: Object classification and detection.  
- **Finance**: Predictive modeling and risk assessment.  
- **Healthcare**: Patient outcome prediction.  
- **Marketing**: Customer segmentation and targeting.  

### Motivation
High-dimensional datasets increase computational complexity, risk of overfitting, and reduce interpretability. This study identifies which dimensionality reduction technique improves classification performance most effectively.

### Objective
- Preprocess the Titanic dataset.  
- Apply PCA and LDA for dimensionality reduction.  
- Train and evaluate multiple classifiers.  
- Compare model performance with accuracy, precision, recall, and F1-score.  
- Provide practical insights for selecting appropriate dimensionality reduction techniques.  

---

## Literature Survey
### Dimensionality Reduction Techniques
Techniques reduce input variables, simplify models, reduce computation, and mitigate overfitting. PCA and LDA are feature extraction methods widely applied in various domains.

### Principal Component Analysis (PCA)
- Transforms correlated variables into uncorrelated **principal components**.  
- Captures maximum variance with fewer components.  
- Widely used in **image processing, genomics, and finance**.  

### Linear Discriminant Analysis (LDA)
- Finds linear combinations of features that best separate classes.  
- Supervised method considering class labels.  
- Applied in **pattern recognition, face recognition, and marketing**.  

### Comparative Insights
- **LDA** generally outperforms PCA in classification tasks.  
- **PCA** is effective for noise reduction and data exploration.  
- The choice depends on the dataset and application.  

---

## Data Preprocessing
1. **Handle Missing Values**  
   - Fill missing `Age` with median.  
   - Fill missing `Embarked` with mode.  
2. **Drop Irrelevant Columns**  
   - Remove `PassengerId`, `Name`, `Ticket`, `Cabin`.  
3. **Encode Categorical Variables**  
   - One-hot encode `Sex` and `Embarked`.  

### Data Splitting and Scaling
- Split dataset into **training (70%)** and **testing (30%)**.  
- Scale numerical features (`Age`, `Fare`) using **StandardScaler**.  

---

## Model Training and Evaluation
### Models Used
- **Logistic Regression**  
- **Random Forest Classifier**  
- **Decision Tree Classifier**  
- **Support Vector Machine (SVC)**  

### Parameter Tuning
- Hyperparameters optimized using **GridSearchCV**.  

---

## Dimensionality Reduction
- **PCA**: Reduced to 2 components for visualization.  
- **LDA**: Reduced to 1 component for better class separation.  

### Evaluation
- Models trained on PCA and LDA transformed data.  
- Decision boundaries visualized to assess class separation.  

---

## Results

### PCA Performance
| Model | Accuracy |
|-------|---------|
| Logistic Regression | 0.6493 |
| Random Forest | 0.6940 |
| Decision Tree | 0.6604 |
| SVC | 0.6791 |

**Observation:** Random Forest performed best with PCA.

### LDA Performance
| Model | Accuracy |
|-------|---------|
| Logistic Regression | 0.8097 |
| Random Forest | 0.7799 |
| Decision Tree | 0.7910 |
| SVC | 0.8097 |

**Observation:** Logistic Regression performed best with LDA. LDA consistently improves class separation and model accuracy.

---

## Model Performance Analysis
- **Logistic Regression**: Accuracy improved from 64.93% (PCA) to 80.97% (LDA).  
- **Random Forest**: Accuracy improved from 69.40% (PCA) to 77.99% (LDA).  
- **Decision Tree**: Accuracy improved from 66.04% (PCA) to 79.10% (LDA).  
- **SVC**: Accuracy improved from 67.91% (PCA) to 80.97% (LDA).  

**Insight:** LDA consistently enhances classification performance by leveraging class-specific information.

---

## Conclusion
- PCA is ideal for noise reduction and exploratory analysis.  
- LDA is more effective for classification tasks, achieving higher accuracy and better class separation.  
- Logistic Regression with LDA achieved the highest accuracy (80.97%).  
- The study demonstrates the importance of selecting the right dimensionality reduction technique based on the dataset and task.

---

## References
1. Pearson, K. (1901). On lines and planes of closest fit to systems of points in space.  
2. Fisher, R.A. (1936). The use of multiple measurements in taxonomic problems.  
3. Jolliffe, I. (2002). Principal Component Analysis.  
4. Martinez, A., & Kak, A.C. (2001). PCA vs LDA for face recognition.  
