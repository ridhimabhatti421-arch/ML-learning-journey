# ML Learning Journey

A collection of notebooks documenting my path of learning Machine Learning and Data Science, one concept at a time.


## 📊 Univariate Analysis

Univariate analysis is the simplest form of Exploratory Data Analysis (EDA): examining **one variable at a time** to understand its distribution, spread, and shape.

The notebook uses the **Titanic** dataset ('train.csv') and is organised by data type.

### 1. Categorical Data
- Countplot – frequency of each category (`Embarked`, `Survived`)
- Pie chart – percentage share of categories (`Sex`)

### 2. Numerical Data
- **Histogram** – distribution of `Age` across bins
- **Displot / KDE plot** – smooth density estimate of `Age`
- **Boxplot** – median, quartiles, and outliers in `Age`
- **Summary statistics** – min, max, and skewness of `Age` (min 0.42, max 80, skew ≈ 0.39, slightly right-skewed)

## 🛠️ Tech Stack

- Python 3
- NumPy
- Pandas
- Matplotlib
- Seaborn
- Jupyter Notebook


## 📚 Dataset

[Titanic – Machine Learning from Disaster](https://www.kaggle.com/competitions/titanic) from Kaggle. Key columns: `Survived`, `Pclass`, `Sex`, `Age`, `SibSp`, `Parch`, `Fare`, `Embarked`.
