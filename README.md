# Content-Based Recommender System for Skincare Products

This project implements a content-based recommendation system for skincare products using machine learning techniques. It was developed as part of a final bachelor thesis at Faculty of Eeltrical Engineering and Computing, Zagreb.

## Overview

The goal of the project is to recommend skincare products similar to those previously used or preferred by a user. The recommendations are generated based on product features such as ingredients, skin type suitability, price, and average rating.

## Dataset

- Source: [Kaggle – Sephora skincare products](https://www.kaggle.com/datasets/dominoweir/skincare-product-ingredients)
- Total products: 1472
- Features include: `name`, `brand`, `price`, `rank`, `skin type`, `ingredients`, and `category`

## Preprocessing

- **Ingredient Standardization**: Used FuzzyWuzzy for fuzzy matching based on Levenshtein distance to reduce 6670 unique ingredients to 736.
- **Dimensionality Reduction**: Applied three techniques:
  - PCA (Principal Component Analysis)
  - t-SNE
  - UMAP (with a parametric neural network using Keras & TensorFlow)

## Algorithms Used

1. **Cosine Similarity**
   - Measures similarity between feature vectors
   - Recommended top 5 products based on highest similarity score

2. **K-Means Clustering**
   - Grouped products into clusters
   - Recommendations based on cluster proximity using Euclidean distance

## Evaluation

- Performed qualitative evaluation by manually analyzing the similarity of recommended products
- Compared overlap in recommendations from both methods
- Both systems showed high agreement (4 out of 5 products received the same recommendations)

## Conclusion

The content-based recommendation system proved effective for skincare product suggestions. While UMAP provided the best results among dimensionality reduction techniques, future improvements could include incorporating chemical composition for more precise similarity measurement.

## Tools & Libraries

- Python
- pandas, scikit-learn, FuzzyWuzzy, TensorFlow, Keras

## References

For a full list of references, see the literature section in the thesis pdf.
