# RoBERTa
A pretrained model, introduced by Facebook, which uses robustly optimized techniques upon bert. The main difference between Bert and Roberta which makes Roberta perform well is dynamic masking technique and removal of next sentence prediction (NSP). Also, Roberta is trained on a larger set of data than Bert.

# W-NUT Shared Task 2
The challenge is to differentiate the informative and uninformative tweets collected basing on current topic Covid-19. A tweet is labelled as informative if it contains any information regarding new or suspicious cases and uninformative in rest of the cases.

## Dataset
The given dataset consists of train set and valid set, each containing 7000 and 1000 tweets respectively. The unlabelled test dataset of 12000 tweets was also released as a part of Codalab competition organized by W-NUT 2020 - Shared Task 2. We have secured 35th position in the competition.



#### Following are the steps performed to detect the label of Covid19 tweets - 

1. Identifying sentences in tsv files and storing them in reliable table format.
2. Cleaning the dataset 
3. Analyzing the dataset
4. Applying supervised Conventional approaches
5. Applying transformer based approaches
6. Analyzing the results of all approaches


## Conventional Approaches
1. Logistic Regression


## Transformer Based Approaches

## Results






