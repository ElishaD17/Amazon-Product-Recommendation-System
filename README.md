# Amazon Product Recommendation System

  ![mv](rs.png) 
  
# README for Amazon Product Reviews Recommender System

## Overview
This project involves building a recommender system using Amazon product reviews. The dataset is processed and analyzed using various data science techniques, including exploratory data analysis (EDA), collaborative filtering, and matrix factorization. The primary goal is to recommend products to users based on their past ratings.

## Project Structure
1. **Data Preparation**
2. **Exploratory Data Analysis**
3. **Collaborative Filtering**
4. **Model-Based Collaborative Filtering**
5. **Recommendation System**

## Technologies
- **Python**: Primary programming language
- **Pandas**: Data manipulation and analysis
- **NumPy**: Numerical operations
- **Seaborn & Matplotlib**: Data visualization
- **Scipy & Statsmodels**: Statistical analysis
- **Scikit-learn**: Machine learning
- **Surprise**: Collaborative filtering algorithms
- **Plotly & Cufflinks**: Interactive visualizations

## Detailed Steps

### 1. Data Preparation
- **Import Libraries**: Load necessary libraries for data manipulation, visualization, and modeling.
- **Load Data**: Download and extract the dataset using Kaggle API, and load it into a Pandas DataFrame.
- **Sample Data**: Take a sample of the dataset to optimize performance during analysis.

### 2. Exploratory Data Analysis
- **Data Overview**: Observe data structure, handle missing values, and drop unnecessary columns.
- **Descriptive Analysis**: Understand the relationship between features, and visualize the distribution of ratings.
- **User and Product Statistics**: Analyze the number of ratings per user and per product.

### 3. Collaborative Filtering
- **Surprise Library**: Utilize the Surprise library to implement collaborative filtering techniques.
- **Train-Test Split**: Split the data into training and testing sets.
- **KNN-Based Collaborative Filtering**: Apply KNN-based collaborative filtering (user-based and item-based).

### 4. Model-Based Collaborative Filtering
- **Data Transformation**: Pivot the data to create a user-item interaction matrix.
- **Matrix Decomposition**: Use Singular Value Decomposition (SVD) to decompose the interaction matrix.
- **Correlation Matrix**: Calculate the correlation matrix to identify similar products.

### 5. Recommendation System
- **Similarity Calculation**: Use the correlation matrix to recommend products.
- **Top-N Recommendations**: Generate the top-N product recommendations for users.

## How to Use
1. **Setup Environment**: Ensure all required libraries are installed.
   ```bash
   pip install kaggle pandas numpy seaborn matplotlib scikit-learn plotly cufflinks surprise
   ```
2. **Kaggle API Configuration**: Setup Kaggle API to download the dataset.
   ```python
   !mkdir -p ~/.kaggle
   !cp kaggle.json ~/.kaggle/
   !chmod 600 ~/.kaggle/kaggle.json
   !kaggle datasets download -d irvifa/amazon-product-reviews
   ```
3. **Run the Script**: Execute the provided Python script to perform the analysis and generate recommendations.

## Conclusion
This project demonstrates the use of various data science techniques to build a recommender system. By analyzing user-product interactions, the system can recommend products that are likely to be of interest to users, thereby enhancing the user experience and potentially increasing sales.

## References
- [Surprise Library Documentation](https://surprise.readthedocs.io/)
- [Scikit-learn Documentation](https://scikit-learn.org/)
- [Kaggle Datasets](https://www.kaggle.com/)

## License
This project is licensed under the Apache 2.0 License. See the LICENSE file for more details.
