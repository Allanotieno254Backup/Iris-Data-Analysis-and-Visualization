# Iris Dataset Analysis and Visualization

## 📌 Project Overview
This project focuses on loading, analyzing, and visualizing the famous Iris dataset using Python. The dataset consists of various measurements of iris flowers and is commonly used in machine learning and data science.

---

## 📂 Dataset Information
**Dataset Name:** IRIS.csv  
**Columns:**
- `sepal_length` (cm)
- `sepal_width` (cm)
- `petal_length` (cm)
- `petal_width` (cm)
- `species` (Setosa, Versicolor, Virginica)

---

## 📌 Objectives
- Load and explore the dataset using Pandas
- Perform basic statistical analysis
- Handle missing values (if any)
- Create visualizations using Matplotlib and Seaborn
- Identify trends and insights

---

## 📦 Requirements
Before running the code, ensure you have the following Python libraries installed:
```bash
pip install pandas numpy matplotlib seaborn
```

---

## 🛠️ Implementation
### 1️⃣ Load and Explore the Dataset
```python
import pandas as pd
# Load the dataset
df = pd.read_csv('IRIS.csv')
# Display first few rows
df.head()
```
**Output:**
| sepal_length | sepal_width | petal_length | petal_width | species  |
|-------------|------------|-------------|------------|---------|
| 5.1         | 3.5        | 1.4         | 0.2        | setosa  |
| 4.9         | 3.0        | 1.4         | 0.2        | setosa  |

### 2️⃣ Basic Data Analysis
```python
# Checking data types and missing values
df.info()
```
**Output:**
```
<class 'pandas.core.frame.DataFrame'>
RangeIndex: 150 entries, 0 to 149
Data columns (total 5 columns):
```

```python
# Summary statistics
df.describe()
```
**Output:**
|        | sepal_length | sepal_width | petal_length | petal_width |
|--------|-------------|------------|-------------|------------|
| count  | 150.0       | 150.0      | 150.0       | 150.0      |
| mean   | 5.84        | 3.05       | 3.76        | 1.20       |

---

## 📊 Data Visualizations
### 3️⃣ Line Chart - Sepal Length Over Index
```python
import matplotlib.pyplot as plt
plt.plot(df.index, df['sepal_length'], label='Sepal Length')
plt.title('Sepal Length Trends')
plt.xlabel('Index')
plt.ylabel('Sepal Length (cm)')
plt.legend()
plt.show()
```
![linechart](https://github.com/user-attachments/assets/9166d668-19b2-49f1-964a-6998875db02f)

### 4️⃣ Bar Chart - Average Petal Length per Species
```python
import seaborn as sns
sns.barplot(x='species', y='petal_length', data=df)
plt.title('Average Petal Length per Species')
plt.show()
```
![barplot](https://github.com/user-attachments/assets/d0464513-1f2b-4494-a6ad-224a4538f9b4)

### 5️⃣ Histogram - Sepal Width Distribution
```python
plt.hist(df['sepal_width'], bins=10, color='blue', alpha=0.7)
plt.title('Distribution of Sepal Width')
plt.xlabel('Sepal Width (cm)')
plt.ylabel('Frequency')
plt.show()
```
![histogram](https://github.com/user-attachments/assets/5a085afe-f8c2-49bf-85dc-026aa7c31e77)

### 6️⃣ Scatter Plot - Sepal Length vs Petal Length
```python
sns.scatterplot(x='sepal_length', y='petal_length', hue='species', data=df)
plt.title('Sepal Length vs Petal Length')
plt.show()
```
![scatter](https://github.com/user-attachments/assets/9ebc3f5a-04ed-482a-88c9-71c88e826dec)

---

## 📈 Key Findings
- **Setosa species** tend to have shorter petals and sepals.
- **Virginica species** generally have the longest petal length.
- **Positive correlation** between sepal length and petal length.
- Sepal width has a more **normal distribution**, as seen in the histogram.

---

## 🚀 How to Run
1. Clone this repository:
```bash
git clone https://github.com/yourusername/Iris-Data-Analysis-and-Visualization.git
```
2. Navigate to the project folder:
```bash
cd Iris-Data-Analysis-and-Visualization
```
3. Run the Jupyter Notebook or Python script:
```bash
jupyter notebook Iris_Analysis.ipynb
```
OR
```bash
python iris_analysis.py
```

---

## 📜 License
This project is under the [MIT License](LICENSE).

---

## 🙌 Acknowledgments
- [UCI Machine Learning Repository](https://archive.ics.uci.edu/ml/datasets/iris)
- [Matplotlib](https://matplotlib.org/)
- [Seaborn](https://seaborn.pydata.org/)
- [Pandas Documentation](https://pandas.pydata.org/docs/)

---

### 📬 Have any suggestions? Feel free to contribute!
Pull requests are welcome. 😃

