Abstract

The goal of this project was to build a model that could differentiate between a New York Times article and an Onion article to prevent someone from accidentally citing a satire site instead of a new site.  Data was pulled from Kaggle.  The project focused on EDA, Pre-Processing, Dimensionality Reduction, Topic Modeling, and Clustering.  Supervised learning was used to do classication to build a final model.

Design

The design of this project was mostly around working with evaluating different NLP approaches to building a predictive model.  The Onion and New York Times data was readily available through Kaggle.  Both article titles and content were evaluated although the focus moved to evaluation of content relatively quickly.  Through an iterative process different types of pre-processing as well as dimensionality reduction and topic modeling were tried out.  Each different approach was then compared using accuracy, precision, recall, and f1 through different machine learning classification models.  The final model was then evaluated.

Data

Data was sourced from Kaggle at https://www.kaggle.com/datasets/undefinenull/satirical-news-from-the-onion and https://www.kaggle.com/datasets/tmishinev/nyt-headlines-20102021.  The data included about 40,000 rows of data from the NYT and about 7000 from the Onion.  Each row of data included a target column based on where or not it came from the Onion as well as a title column and a content column.  During the pre-processing stage, additional columns were added for cleaned, tokenized, and then vectorized data.  These columns were then reduced using dimensionality reduction (PCA) and topic modeling (LSA, NMF, and LDA).  Finally, K-means clustering was attempted on the different types of reduced data.

  
Algorithms

The following algorithms / main feature / pre-processing combinations were attempted.

PCA Title Random Forest
PCA Title XGBoost
PCA Content Random Forest
PCA Content XGBoost
LSA Title Random Forest
LSA Title XGBoost
LSA Content Random Forest
LSA Content XGBoost
NMF Title Random Forest
NMF Title XGBoost
NMF Content Random Forest
NMF Content XGBoost
LDA Content Random Forest
LDA Content XGBoost
PCA Content Random Forest w/ K-Means clustering
PCA Content XGBoost w/ K-Means clustering
LSA Content Random Forest w/ K-Means clustering
LSA Content XGBoost w/ K-Means clustering
NMF Content Random Forest w/ K-Means clustering
NMF Content XGBoost w/ K-Means clustering

The best algorithm turned out to be PCA Content Random Forest with 97.5% accuracy and 90.6% recall.  

Tools

Tools used included pandas, scikit-learn, XGBoost, matplotlib, seaborn, nltk, SpaCy, and scattertext.  Almost all of the work for this project was done in python jupyter notebooks.  The data itself was downloaded manually through the kaggle website.


Communication

Slides and visuals presented included data and the pre-processing as well as the scores of the final used model and some examples of false negatives.  A Scatter Text chart is also included.



