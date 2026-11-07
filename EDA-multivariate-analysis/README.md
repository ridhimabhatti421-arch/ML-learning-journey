# ML Learning Journey

A collection of notebooks documenting my path of learning Machine Learning and Data Science, one concept at a time.



## 📊 Notebook

### 1. Univariate Analysis (`univariate-analysis.ipynb`)

Examines **one variable at a time** to understand its distribution, spread, and shape, using the Titanic dataset.

- **Categorical data:** countplot (`Embarked`, `Survived`) and pie chart (`Sex`)
- **Numerical data:** histogram, displot/KDE plot, and boxplot of `Age`
- **Summary statistics:** min, max, and skewness of `Age`

### 2. Multivariate Analysis (`multivariate-analysis.ipynb`)

Explores **relationships between variables** using Seaborn, organised by the type of variables being compared.

| # | Plot | Variable Types | Dataset | Variables |
|---|------|----------------|---------|-----------|
| 1 | Scatterplot | Numerical – Numerical | Tips | `total_bill` vs `tip`, coloured by `sex`, styled by `smoker` |
| 2 | Bar plot | Numerical – Categorical | Titanic | `Age` by `Pclass`, split by `Sex` |
| 3 | Box plot | Numerical – Categorical | Titanic | `Age` by `Sex`, split by `Survived` |
| 4 | Heatmap | Categorical – Categorical | Titanic | Crosstab of `Pclass` and `Survived` |
| 5 | Clustermap | Categorical – Categorical | Titanic | Crosstab of `Parch` and `Survived` |
| 6 | Pairplot | Multiple numerical | Iris | All numeric features, coloured by `species` |
| 7 | Lineplot | Numerical – Numerical (time) | Flights | `passengers` over `year` |
| 8 | Clustermap | Pivot table | Flights | `passengers` by `month` and `year` |

**Key takeaways**
- Adding `hue` and `style` lets a 2D plot show 3 or 4 variables at once.
- `pd.crosstab()` turns two categorical columns into a table that heatmaps and clustermaps can plot.
- A pairplot gives a quick overview of every pairwise relationship in a dataset.
- Lineplots reveal trends over time; the Flights data shows a clear upward trend in passengers.

## 🛠️ Tech Stack

- Python 3
- NumPy
- Pandas
- Matplotlib
- Seaborn
- Jupyter Notebook



## 📚 Datasets

| Dataset | Source | Used in |
|---------|--------|---------|
| Titanic (`train.csv`) | [Kaggle](https://www.kaggle.com/competitions/titanic) | Both notebooks |
| Tips | Seaborn built-in | Multivariate |
| Flights | Seaborn built-in | Multivariate |
| Iris | Seaborn built-in | Multivariate |

