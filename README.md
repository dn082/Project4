# Project4

## INTRODUCTION
In this project, I aim to explore a dataset that has recipes and ingredients to uncover natural groupings of recipes based on their ingredient profiles. The main problem is that with recipes available online, it’s hard to discover dishes that are similar, especially when they don’t share the same title or cuisine label.

By using/applying clustering techniques, I want to answer questions like:
- What types of recipes tend to use similar ingredient combinations?
- Can we discover hidden “families” of recipes that aren’t labeled by cuisine?
- Are there clusters that correspond to dietary patterns (e.g., vegetarian, low-carb, comfort food)?

## WHAT IS CLUSTERING AND HOW DOES IT WORK?
It is an unsupervised machine learning method that does grouping of data points without knowing the group, therefore, clusters.
- K-means is the idea of choosing the number of clusters (k), usually based on inertia, and then it picks starting centroids, and then each data point is assigned to the nearest centroid. Then, the centroids are recalculated by taking the mean of all points in each cluster. It overall gets put to whatever centriod is closest, and it does it till the point doesn't move.
- Agglomerative clustering is a type of hierarchical clustering that

## DATA INTRODUCTION
For this project, I will be using a dataset from Kaggle, the link is https://www.kaggle.com/datasets/pes12017000148/food-ingredients-and-recipe-dataset-with-images. The dataset has **13,582 rows** and has **6 columns**, where one column is just the row number info, and has **5 columns** with information. Column nameas are
- **Unnamed: 0**: The row number/index.
- **Title**: The name of the food dish.
- **Ingredients**: The raw list of ingredients scraped from the website.
- **Instructions**: The step-by-step cooking instructions.
- **Image_Name**: The file name used to map the recipe to its corresponding image.
- **Cleaned_Ingredients**: A processed and cleaned list of ingredients, which is usually better for analysis.

## DATA UNDERSTANDING/VISUALIZATION
To explore the data, I used:
- Elbow plot so I can see how it looks on a plot and be able to get the optimal number of clusters that is ideal for my project
- After Agglo clustering, I used a way so I can see the hierarchical merging of recipes with the Dendrogram
- To see the top ingredients for each cluster, I used a bar chart to highlight which ingredients are most defining for that cluster, and that specific visualization makes it easy to see the main ingredient used for each cluster
- I also made a PCA cluster scatter plot to show the cluster of recipes, which could show the similarity and differences in ingredients, along with which cluster each recipe belongs to. Also, to get a general idea of whether my clusters make sense.

## PREPROCESSING

## MODELING
For this project, I applied both K Means and Agglomerative Clustering

## STORYTELLING/EVALUATION

## IMPACT


## REFERENCES
- https://www.kaggle.com/datasets/pes12017000148/food-ingredients-and-recipe-dataset-with-images
- https://scikit-learn.org/stable/modules/generated/sklearn.feature_extraction.text.TfidfVectorizer.html 
