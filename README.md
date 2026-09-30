# Bank Customer Segmentation

Customer segmentation on mixed-type banking data (numerical and categorical features), developed as a business case for the Fintech course at Politecnico di Milano.

📊 **[Project presentation (PDF)](docs/Client-Segmentation-Slides.pdf)**

## Approach
- **Preprocessing**: Min-Max scaling for numerical features and One-Hot Encoding (without dropping categories) to keep Jaccard/Dice similarities meaningful
- **Hybrid distances** for mixed data: Manhattan + Dice / Jaccard, compared against Gower distance
- **Non-linear visualization** with t-SNE and UMAP, with perplexity tuning
- **Clustering comparison**: K-Prototypes, K-Medoids, Agglomerative Clustering and DBSCAN, with internal validation through Silhouette, Calinski-Harabasz and Davies-Bouldin scores
- **Bayesian extension**: Beta priors with univariate and bivariate updates to dynamically refine cluster profiles as new customers arrive

## Results
The final model (Agglomerative Clustering, Dice-Manhattan distance, k = 4) identifies four interpretable segments, translated into customer personas for differentiated business strategies:
- Senior conservative traditionalists
- Wealth-accumulating families
- Disengaged and wary customers
- Affluent, digitally active customers

## Tech stack
Python, pandas, NumPy, scikit-learn, UMAP, matplotlib, seaborn

## Notes
The dataset was provided during the course and is not included in this repository.


