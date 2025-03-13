# DAI-Assignment1

This repository contains a data analysis pipeline that covers data cleaning, exploratory data analysis (EDA), and visualization. The project demonstrates how to handle missing values, detect and remove outliers, and analyze relationships between variables using statistical and visual techniques.

# Project Structure

# Tasks Performed

# 1. Data Cleaning:

Handling missing values (imputation for numerical, categorical fill-in): : Missing values in numerical columns are replaced using median imputation because the median is robust to outliers and prevents skewing the distribution.Missing values in categorical columns are filled with a placeholder, such as 'Unknown', to maintain consistency. If categorical features have a dominant category, mode imputation (filling with the most frequent category) is also considered.

Removing duplicate records : Duplicate rows are identified and removed to avoid biased results in analysis.

Detecting and treating outliers using IQR method : Outliers can significantly impact the results of an analysis. We use the Interquartile Range (IQR) method to detect and remove extreme values.

Filtering Outliers:

df = df[(df['age'] >= Q1 - 1.5 * IQR) & (df['age'] <= Q3 + 1.5 * IQR)]

This removes extreme values beyond 1.5 times the IQR range.


Standardizing categorical values : Categorical variables sometimes have typos, inconsistent capitalization, or mixed formats. We standardize them to maintain uniformity.


# 2. Exploratory Data Analysis (EDA):

Univariate Analysis: This step involves analyzing each variable independently to understand its distribution and statistical properties.

Summary Statistics for Numerical Variables

Compute mean, median, variance, skewness, and other statistical measures.

Example Interpretation:

If the mean and median differ significantly, it indicates skewness.

A high standard deviation suggests the data has large variability.

Frequency Distributions for Categorical Variables

Count occurrences of each category using a bar plot.

Example Interpretation:

If one category is dominant, it might influence other variables disproportionately.

Visualizing Distributions

Histograms (for continuous variables)

Box Plots (for identifying outliers)

Example Interpretation:

If a boxplot shows long whiskers or extreme outliers, further investigation is needed.

Bivariate Analysis: This step examines relationships between two variables, either numerical or categorical.

Correlation Matrix (Numerical Variables)

Computes the correlation coefficient between all numerical columns.

Example Interpretation:
A correlation near 1 or -1 indicates a strong relationship.

A correlation near 0 suggests no relationship.

Scatter Plots (Continuous Variable Relationships)

Shows how two numerical variables interact.

Example Interpretation:

If points form a trend, the variables may have a linear relationship.

If scattered randomly, the variables are likely independent.

Comparing Categorical and Numerical Variables

Bar Plots (categorical vs. numerical)

Violin Plots (to see distribution differences)

Example Interpretation:

If the violin plot is wider in one region, that category has more observations in that range.

Multivariate Analysis: This step explores how multiple features interact.

Pair Plots (Relationships Between Multiple Variables)

Creates scatter plots for all numerical variables against each other.

Example Interpretation:

Diagonal elements show the distribution of each variable.

Off-diagonal elements show relationships between variables.

Heatmap (Visualizing Correlations Among Multiple Variables)

Highlights strong and weak correlations in a dataset.

Example Interpretation:

Bright colors indicate strong correlations between variables.

Grouped Comparisons (Analyzing Interactions Between Features)

Box Plot Comparing Survival Rate by Class

Example Interpretation:

Higher-class passengers tend to pay higher fares and have a higher survival rate.

# Expected Outcome

✅ Learn to clean and preprocess real-world datasets.

✅ Understand and visualize distributions of numerical and categorical variables.

✅ Identify and interpret relationships between features.

✅ Apply multivariate techniques to analyze complex interactions.


