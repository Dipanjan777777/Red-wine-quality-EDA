# Red Wine Quality Analysis - Exploratory Data Analysis (EDA)

## Project Overview

This project performs an extensive exploratory data analysis on the Red Wine Quality dataset from the Portuguese "Vinho Verde" wine. The goal is to analyze various physicochemical properties of red wine and understand their relationship with wine quality ratings.

## Dataset Information

### Source
The dataset contains red wine variants of the Portuguese "Vinho Verde" wine with physicochemical and sensory variables.

### Dataset Characteristics
- **Total Records**: 1599 wine samples 
- **Features**: 11 physicochemical input variables + 1 output variable (quality)
- **Missing Values**: None
- **Data Type**: Numerical data suitable for both classification and regression tasks

### Features Description

**Input Variables (Physicochemical Tests):**
1. **Fixed Acidity** - Non-volatile acids in wine
2. **Volatile Acidity** - Amount of acetic acid in wine (high levels can lead to unpleasant vinegar taste)
3. **Citric Acid** - Adds freshness and flavor to wines
4. **Residual Sugar** - Amount of sugar remaining after fermentation
5. **Chlorides** - Amount of salt in wine
6. **Free Sulfur Dioxide** - Prevents microbial growth and wine oxidation
7. **Total Sulfur Dioxide** - Amount of free and bound forms of SO2
8. **Density** - Density of wine (depends on alcohol and sugar content)
9. **pH** - Acidity/alkalinity level (0-very acidic, 14-very basic)
10. **Sulphates** - Wine additive that contributes to SO2 levels
11. **Alcohol** - Alcohol percentage in wine

**Output Variable (Sensory Data):**
- **Quality** - Wine quality score (0-10 scale, actual range: 3-8)

## Key Findings from EDA

### 1. Data Quality Assessment
- ✅ **No missing values** detected in the dataset
- ✅ **240 duplicate records** identified and removed
- ✅ **Clean dataset** with 1,359 unique wine samples after preprocessing

### 2. Quality Distribution Analysis
- **Imbalanced Dataset**: Most wines are rated as quality 5 and 6
- **Quality Range**: Actual quality scores range from 3 to 8 (not the full 0-10 scale)
- **Distribution**:
  - Quality 3: Very few samples (rare)
  - Quality 4: Low frequency
  - Quality 5: High frequency ⭐
  - Quality 6: Highest frequency ⭐⭐
  - Quality 7: Moderate frequency
  - Quality 8: Very few samples (rare)

### 3. Correlation Analysis
Key correlations discovered through heatmap analysis:

**Positive Correlations with Quality:**
- **Alcohol**: Strong positive correlation with wine quality
- **Sulphates**: Moderate positive correlation
- **Citric Acid**: Weak positive correlation

**Negative Correlations with Quality:**
- **Volatile Acidity**: Strong negative correlation (higher volatile acidity = lower quality)
- **Total Sulfur Dioxide**: Weak negative correlation
- **Density**: Negative correlation

**Other Notable Correlations:**
- Fixed Acidity ↔ Citric Acid: Positive correlation
- Fixed Acidity ↔ Density: Strong positive correlation
- Alcohol ↔ Density: Strong negative correlation
- Total SO2 ↔ Free SO2: Strong positive correlation

### 4. Distribution Patterns
- Most features show **approximately normal distributions** with some skewness
- **Alcohol content** shows interesting patterns related to quality
- **pH levels** are generally well-distributed around 3.2-3.4 (acidic wines)

### 5. Bivariate Analysis Insights
- **Alcohol vs Quality**: Higher alcohol content tends to correlate with better quality ratings
- **Volatile Acidity vs Quality**: Lower volatile acidity is associated with higher quality wines
- **Alcohol vs pH by Quality**: Scatter plot reveals quality patterns based on alcohol and pH combinations

## Visualization Summary

The analysis includes several key visualizations:

1. **Correlation Heatmap** - Shows relationships between all variables
2. **Quality Distribution Bar Chart** - Reveals the imbalanced nature of quality ratings
3. **Feature Histograms** - Distribution analysis for each physicochemical property
4. **Pairplot Matrix** - Comprehensive pairwise relationships
5. **Box Plots** - Quality vs Alcohol relationship analysis
6. **Scatter Plots** - Multi-dimensional analysis (Alcohol vs pH colored by Quality)

## Conclusions

### Primary Insights:
1. **Wine Quality Prediction**: Alcohol content and volatile acidity are the strongest predictors of wine quality
2. **Dataset Characteristics**: This is an imbalanced classification problem with most wines rated as average quality (5-6)
3. **Feature Importance**: Not all physicochemical properties are equally important for quality assessment

### Recommendations for Further Analysis:
1. **Feature Selection**: Focus on alcohol, volatile acidity, sulphates, and citric acid for modeling
2. **Classification Approach**: Consider grouping quality scores into categories (Low: 3-4, Medium: 5-6, High: 7-8)
3. **Outlier Detection**: Implement outlier detection to identify exceptional or poor wines
4. **Machine Learning**: The dataset is suitable for both regression and classification algorithms


## Technical Stack

- **Python Libraries Used**:
  - `pandas` - Data manipulation and analysis
  - `matplotlib` - Basic plotting and visualization
  - `seaborn` - Statistical data visualization
  - `numpy` - Numerical computing (implicit)

## Files in Repository

- `winequalityEDA.ipynb` - Alternative EDA notebook
- `winequality-red.csv` - Raw dataset
- `requirements.txt` - Python dependencies
- `pyproject.toml` - Project configuration
- `README.md` - Project documentation (this file)


