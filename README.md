# Phishing Website Detection by Machine Learning Techniques

## Objective
A phishing website is a common social engineering method that mimics trustful uniform resource locators (URLs) and webpages. The objective of this project is to train machine learning models and deep neural nets on the dataset created to predict phishing websites. Both phishing and benign URLs of websites are gathered to form a dataset and from them required URL and website content-based features are extracted. The performance level of each model is measures and compared.

## Data Collection
The set of phishing URLs are collected from opensource service called **PhishTank**. This service provide a set of phishing URLs in multiple formats like csv, json etc. that gets updated hourly. To download the data: https://www.phishtank.com/developer_info.php. From this dataset, 5000 random phishing URLs are collected to train the ML models.

The legitimate URLs are obatined from the open datasets of the University of New Brunswick, https://www.unb.ca/cic/datasets/url-2016.html. This dataset has a collection of benign, spam, phishing, malware & defacement URLs. Out of all these types, the benign url dataset is considered for this project. From this dataset, 5000 random legitimate URLs are collected to train the ML models.



## Feature Extraction
The below mentioned category of features are extracted from the URL data:

1.   Address Bar based Features <br>
          &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;In this category 9 features are extracted.
2.   Domain based Features<br>
          &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;In this category 4 features are extracted.
3.   HTML & Javascript based Features<br>
          &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;In this category 4 features are extracted.


## Models & Training

Before stating the ML model training, the data is split into 80-20 i.e., 8000 training samples & 2000 testing samples. From the dataset, it is clear that this is a supervised machine learning task. There are two major types of supervised machine learning problems, called classification and regression.

This data set comes under classification problem, as the input URL is classified as phishing (1) or legitimate (0). The supervised machine learning models (classification) considered to train the dataset in this project are:

* Decision Tree
* Random Forest
* Multilayer Perceptrons
* XGBoost
* Autoencoder Neural Network
* Support Vector Machines

All these models are trained on the dataset and evaluation of the model is done with the test dataset. The elaborate details of the models & its training are mentioned in [Phishing Website Detection_Models & Training.ipynb]
## Presentation


## End Results
From the obtained results of the above models, XGBoost Classifier has highest model performance of 86.4%. So the model is saved to the file '[XGBoostClassifier.pickle.dat]
### Next Steps

This project can be further extended to creation of browser extention or developed a GUI which takes the URL and predicts it's nature i.e., legitimate of phishing. *As of now, I am working towards the creation of browser extention for this project. And may even try the GUI option also.* The further developments will be updated at the earliest. 
