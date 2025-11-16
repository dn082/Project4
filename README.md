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
- Agglomerative clustering is a type of hierarchical clustering that groups by similarity, like there is one item, and it will keep on merging as pairs of clusters till there is one large cluster.

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
- Dropped Irrelevant Columns - this is useful as I got to remove parts of the data that are not useful for clustering.
- Cleaned up text - this was useful as it simplified the list of ingredients. I did a type check, lowercasing, number removal, and stop word removal, filtered characters, normalized whitespace, removed single letters and short words, etc.
- TF‑IDF vectorization - this was useful as it converted the cleaned text into a numerical representation for clustering.
  
## MODELING
For this project, I applied both K Means and Agglomerative Clustering. I used K‑Means as it would assign recipes to a cluster that aligns, and it would give me an efficient way to group a large recipe dataset. It would group ingredient lists and the recipe itself and put them into clusters that share similar ingredient patterns. It was a solid way to show a cluster of recipes based on ingredients. For Agglomerative, it can build a hierarchy of recipes and group them, showing how recipes merge step by step, which can help view ingredient similarities.

## STORYTELLING/EVALUATION
Through this clustering project, it allowed me to see groupings in the recipe patterns of similarity, such as, for example, some groups were dominated by staple seasoning bases like onion, garlic, cilantro, thyme, etc, while others leaned toward baking ingredients such as eggs, vanilla extract, cream, and cinnamon. Meaning that recipes are organized into clusters ranging from sweet goods to seasoning-heavy foods. I think you can discover hidden families based on data, but through this project, I learned that finding groupings based on specific cuisines is more niche since each cuisine could have its own specific ingredients that are specific to that cuisine, so finding hidden families wasn't really ideal for clustering, as it could be mixed up with other things that can be unrelated. I think the same logic can be applied to dietary patterns and restrictions, since they often require specific ingredients to be removed, and clustering in that context is more challenging because the specificness of restrictions can be niche. Like you might identify patterns of certain ingredients that align with dietary needs, but it would be harder to form broad recipe clusters.

## IMPACT
I think for just general impact for a project like this is how it could help with discovery and being more accessible to find certain things based on ingredients that can be preferred and align recipes that match their ideal preferences, dietary needs, etc, and help with filtering and recommending things based on food choices. I think for a negative impact, it could highly recommend popular cuisines if the same naming conventions are used that are over-represented in the data.

## REFERENCES
- https://www.kaggle.com/datasets/pes12017000148/food-ingredients-and-recipe-dataset-with-images
- https://scikit-learn.org/stable/modules/generated/sklearn.feature_extraction.text.TfidfVectorizer.html 
