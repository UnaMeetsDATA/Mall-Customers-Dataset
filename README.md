# Mall Customers Dataset - K-Means Clustering Analysis

## Overview
This project demonstrates customer segmentation using K-Means clustering on a mall customers dataset. The analysis identifies distinct customer groups based on their annual income and spending behavior, enabling data-driven insights for targeted marketing strategies.

## Dataset
The dataset contains customer information with the following key features:
- **Annual Income (k$)**: Customer annual income in thousands of dollars
- **Spending Score (1-100)**: A score assigned based on customer spending patterns and frequency

## Project Structure

### Key Analyses Performed

#### 1. **Data Loading & Exploration**
- Upload and load the dataset using pandas
- Perform exploratory data analysis (EDA)
- Check for missing values

#### 2. **Data Preprocessing**
- Extract relevant features: Annual Income and Spending Score
- Standardize features using `StandardScaler` for better clustering performance

#### 3. **K-Means Clustering (Initial)**
- Apply K-Means algorithm with 5 clusters
- Visualize clusters with scatter plots
- Display cluster centroids on the visualization

#### 4. **Clustering Quality Assessment**
- Calculate Silhouette Score to evaluate clustering quality
- Provide interpretive feedback:
  - **Silhouette Score > 0.5**: Good clustering structure
  - **Silhouette Score > 0.25**: Reasonable clustering
  - **Silhouette Score ≤ 0.25**: Poor clustering

#### 5. **Elbow Method**
- Test K values from 1 to 10 clusters
- Plot Within-Cluster Sum of Squares (WCSS) vs number of clusters
- Identify the optimal number of clusters by finding the "elbow" point

#### 6. **Optimized K-Means Clustering**
- Apply K-Means with the optimal number of clusters
- Create final customer segments with optimized cluster assignments
- Visualize optimized clusters with centroids

## Results Interpretation

### Customer Segments
The clustering identifies distinct customer profiles:
- **High Income, High Spending**: Premium customers with strong purchasing power
- **High Income, Low Spending**: Conservative affluent customers
- **Medium Income, Medium Spending**: Average customers
- **Low Income, High Spending**: Value-conscious deal seekers
- **Low Income, Low Spending**: Budget-conscious customers

## Technologies Used
- **Python 3.x**
- **Pandas**: Data manipulation and analysis
- **NumPy**: Numerical computations
- **Matplotlib**: Data visualization
- **Seaborn**: Statistical data visualization
- **Scikit-learn**: Machine learning algorithms
  - `StandardScaler`: Feature scaling
  - `KMeans`: Clustering algorithm
  - `silhouette_score`: Clustering evaluation

## Installation & Requirements

```bash
pip install pandas numpy matplotlib seaborn scikit-learn
```

## Usage

### Running in Google Colab
```python
from google.colab import files
uploaded = files.upload()
df = pd.read_csv(next(iter(uploaded)))
```

### Running Locally
```python
df = pd.read_csv('your_dataset.csv')
```

## Key Metrics

### Silhouette Score
- Measures how similar objects are to their own cluster compared to other clusters
- Range: -1 to 1
- Higher scores indicate better-defined clusters

### WCSS (Within-Cluster Sum of Squares)
- Measures the variance within clusters
- Lower values indicate tighter, more cohesive clusters
- Used to determine optimal number of clusters via the Elbow Method

## Visualizations

1. **K-Means Clustering Scatter Plot**: Shows customer segments based on Annual Income and Spending Score
2. **Cluster Centroids**: Red X markers indicate the center of each cluster
3. **Elbow Method Graph**: Helps identify the optimal number of clusters
4. **Optimized Clustering**: Final customer segmentation with refined cluster assignments

## Insights & Business Applications

- **Target Marketing**: Design campaigns tailored to each customer segment
- **Resource Allocation**: Prioritize marketing budget for high-value customers
- **Customer Service**: Customize service levels based on customer segment
- **Product Development**: Develop products that appeal to specific segments
- **Risk Management**: Identify and monitor at-risk customer segments

## Author
UnaMeetsDATA

## License
Please check your repository's license file for details.

## Contributing
Contributions are welcome! Please feel free to submit pull requests or open issues for discussion.

---

**Last Updated**: February 22, 2026