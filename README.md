# ConstructPeer
This repository contains dataset and code of the "ConstructPeer: A Dataset for Estimating the Constructiveness of Peer Review Comments" Authors: Prabhat Kumar Bharti, Tirthankar Ghoshal, Mayank Agrawal, Asif Ekbal Affiliation: Indian Institute of Technology, Patna, India


### Folders in main repository:
- **[datasets](https://github.com/PrabhatkrBharti/ConstructPeer/tree/main/datasets) :** <br />
    - contains the [review dataset csv file](https://github.com/PrabhatkrBharti/ConstructPeer/blob/main/datasets/Final_review_dataset.csv) that we will be using to train our models 
    - contains the readymade [toxicbert features csv file](https://github.com/PrabhatkrBharti/ConstructPeer/blob/main/datasets/toxicbert.csv) for our convenience (since creating this takes at least 1 hour time).<br />
- **[graphs](https://github.com/PrabhatkrBharti/ConstructPeer/tree/main/graphs) :**<br />
    - contains the graphs and other pictorial charts obtained from the codes.
    
------

### Files in main repository:
- **[model hyperparameters textfile](https://github.com/PrabhatkrBharti/ConstructPeer/blob/main/model_hyperparameters.txt) :**<br />
  - model hyperparameters textfile talks about the ML/DL models used and also their hyperparameters, which can be adjusted according to our dataset, to obtain best results. <br />
- **[feature analysis notebook](https://github.com/PrabhatkrBharti/ConstructPeer/blob/main/features_review.ipynb) :**<br />
  - feature analysis notebook contains the codes that provide a detailed analysis of the 16 features (other than word embeddings) that we have used for creating the models. This can give us a basic idea how the features such as review length, linguistic features, sentiment and harshness of reviews varies for constructive (C) and non-constructive (N) reviews.<br />
- **[model prediction notebook](https://github.com/PrabhatkrBharti/ConstructPeer/blob/main/CN_baseline_ML.ipynb) :**<br />
  - model prediction notebook contains the codes with detailed guiding comments, that create each of the three models we have used, prepare the embedding and labels matrix from the features for training and testing, train the models, and then show the results of the training on the testing dataset (baseline).
  - **[interannotation agreement notebook](https://github.com/PrabhatkrBharti/ConstructPeer/blob/main/interannotation_agreement.ipynb) :**<br />
  - interannotation agreement notebook contains the codes with detailed guiding comments, for interannotation agreement between annotator.

## Dataset
[Review Data](https://github.com/PrabhatkrBharti/ConstructPeer/blob/main/datasets/Final_review_dataset.csv) is a comma-separated csv file containing 1496 peer-review comments  were obtained from two
independent sources: 1) shitmyreviewerssay, 2)Openreview and manually annotated by two human annotations on the basis two labels: Constructive(C) and Non-constructive(N). The dataset has 749 Constructive reviews and 747 Non-constructive reviews, with 880 reviews from shitmyreviewerssay website, 412 constructive reviews from ICLR, and 204 non-constructive reviews from other open access interdisciplinary sources.

------

### Models we use for experiments:

- **SVC :** Support Vector Classifier <br />
  **Link:** https://scikit-learn.org/stable/modules/generated/sklearn.svm.SVC.html

- **MNB :** Multinomial Naive Bayes Classifier <br />
  **Link:** https://scikit-learn.org/stable/modules/generated/sklearn.naive_bayes.MultinomialNB.html
  
- **XGBoost :** XGBoost <br />
  **Link:** https://github.com/dmlc/xgboost

------

### Models we use for extracting features:

- **tfidf :** Tfidf Vectorizer <br />
  **Link:** https://scikit-learn.org/stable/modules/generated/sklearn.feature_extraction.text.TfidfVectorizer.html
  
- **Linguistic features :** POS tag features <br />
  **Link:** https://www.nltk.org/_modules/nltk/tag.html

  
- **toxicBERT :** ToxicBERT toxicity score <br />
  **Link:** https://huggingface.co/unitary/toxic-bert
  
------
