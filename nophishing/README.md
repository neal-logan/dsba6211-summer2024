# No Phishing: Detecting Malicious URLs
#### DSBA 6211 - Summer 2024 - Neal Logan

### Overview

This project covers the development of phishing URL detection models.  Given a set of features extracted from the URLs themselves, generated from the corresponding sites, or obtained from third parties, these models predict whether the URL in question is legitimate or used for phishing. 

### Table of Contents

[01 Exploratory Data Analysis](https://github.com/neal-logan/dsba6211-summer2024/blob/main/nophishing/01_exploratory_analysis.ipynb) - This notebook covers extensive exploratory analysis of the dataset, including some preliminary modeling used to identify the most relevant features.

[02 Modeling Notebook](https://github.com/neal-logan/dsba6211-summer2024/blob/main/nophishing/02_modeling.ipynb)
[Data](https://github.com/neal-logan/dsba6211-summer2024/tree/main/nophishing/data) - This notebook includes TODO

[03 Appendix: Additional Models and Risk Analysis]() - This notebook includes additional modeling approaches not included in the main notebook as well as a more exhaustive look at model risks.   

[04 Training Data]() - 

[05 Test Data]() -

[requirements.txt]() - This document identifies all libraries (including version) necessary to reproduce the project. 

### Reproducing Results

The results can be reproduced by simply running the notebook [02 Modeling](https://github.com/neal-logan/dsba6211-summer2024/blob/main/nophishing/02_modeling.ipynb).  This notebook will install and import the necessary packages of the correct versions, load and transform the [data](https://github.com/neal-logan/dsba6211-summer2024/tree/main/nophishing/data), run and evaluate the models, and finally explain key features of the models and the data itself.  The random seed is embedded in the notebook and used wherever necessary to obtain consistent results.

## Introduction

Malicious URLs are a common component of phishing attacks.  They are sometimes used to exploit technical vulnerabilities, executing malicious code  automatically when the message is presented to the target, when the target interacts with the message, or when the target follows the link to the malicious URL.  However, attacks relying primarily on social engineering present a more difficult challenge, for example by leading phishing targets to sites that appear entirely legitimate even to relatively vigilant and sophisticated internet users.  Detecting these malicious URLs provides us with several opportunities for defense, and is an important part of engineering secure systems.

Malicious URL detection can be used in several ways.  It can be used to provide suspected-phishing warnings to users, particularly in web browsers or email/messaging systems.  It can also be used by organizations, which can warn or block users from visiting suspected phishing sites.  And finally, malicious URL detection can be used by to identify or refer malicious sites for takedowns or to help direct law enforcement efforts against the threat actors behind the malicious sites.

## Literature Review

#### [Phishing URL Detection](https://github.com/pirocheto/phishing-url-detection) by Pirocheto


This repository contains a complete project for phishing URL detection using machine learning and MLOps practices. It uses a TF-IDF vectorizer using both character and word n-grams) with a linear SVM model. The code is designed to be lightweight and fast, suitable for embedding in applications, and can work offline, without an internet connection. The repository also includes instructions for reproducing the model and running the pipeline.

This project is relevant both for the subject matter and because of its relation to the dataset I'm using.

#### [PhishShield](https://github.com/praneeth-katuri/PhishShield) by Praneeth Katuri


This GitHub repository provides a comprehensive solution for detecting phishing websites using analytical models and custom transformers for preprocessing. It includes feature-based and text-based models, including random forest, LGBM, SVC, logistic regression, and Multinomial Naive Bayes, and takes advantage of grid-search with cross-validation. The repository also offers Flask deployment for real-time URL prediction and caching for performance improvement.

This project is relevant because it explores and compares a variety of techniques for detecting malicious URLs.

#### [Phishing Link Detection](https://github.com/Sayan-Maity-Code/Phishing-link-detection) by Sayan Maity

This project uses Multinomial Naive Bayes and Logistic Regression to detect malicious URLs. The model's preprocessing involves tokenization and TF-IDF vectorization. The project includes scripts for training and evaluating the model.

This project is relevant mainly in that it provides an additoinal perspective on the topic.


## Dataset

The data was obtained from [HuggingFace](https://huggingface.co/datasets/pirocheto/phishing-url).

The dataset is cleaned and partly preprocessed. In addition to the raw URL and binary phishing label, it contains 87 features, including:

* 56 features extracted from URL syntax and structure,
* 24 features generated from page content, and
* 7 features obtained from external services.

## EDA and Feature Selection



## Final Models and Evaluation



## Conclusions and Future Directions



## Additional Discussion
