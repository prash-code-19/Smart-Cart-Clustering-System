# SmartClusteringSystem

An exploratory customer-segmentation project for an e-commerce business. The Jupyter notebook prepares customer data, engineers useful features, explores dimensionality reduction, and compares clustering approaches to identify groups with similar customer profiles.

## Project contents

| File | Description |
| --- | --- |
| `smartcart.ipynb` | Notebook containing data preparation, analysis, visualizations, and clustering |
| `smartcart_customers.csv` | Customer demographics, household information, purchase behavior, and campaign-response data used by the notebook |

## Analysis workflow

The notebook:

1. Loads the customer data and checks its shape and missing values.
2. Fills missing income values with the median and engineers age, customer tenure, total spending, and total children features.
3. Groups education and marital-status categories, removes identifier and source columns that are not used as model inputs, and filters unusually high ages and incomes.
4. One-hot encodes education and living arrangement, then standardizes the model features.
5. Uses principal component analysis (PCA) to visualize the data and provide a three-component representation for clustering.
6. Explores cluster counts with the elbow method and silhouette scores, then applies K-Means and agglomerative clustering with four clusters.
7. Visualizes and summarizes the resulting customer groups.

Cluster IDs are labels, not rankings; a cluster number does not imply better or worse customers. The profiles should be interpreted using the feature summaries and plots.

## Requirements

- Python 3
- Jupyter Notebook or JupyterLab
- pandas
- matplotlib
- seaborn
- scikit-learn
- kneed

Install the packages with pip:

```bash
python -m pip install jupyter pandas matplotlib seaborn scikit-learn kneed
```

## Run the notebook

1. Clone or download this project folder.
2. Install the requirements above.
3. Start Jupyter from this folder:

   ```bash
   jupyter notebook
   ```

4. Open `smartcart.ipynb` and run the cells in order. Keep `smartcart_customers.csv` in the same folder as the notebook so its relative file path resolves.

## Notes

- This is a notebook-based analysis project; it does not currently provide a web application, command-line interface, or trained model export.
- The notebook contains exploratory analysis and visualizations. Results can vary if the input data or preprocessing changes.

