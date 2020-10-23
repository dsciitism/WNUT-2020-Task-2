# RoBERTa
A pretrained model, introduced by Facebook, which uses robustly optimized techniques upon bert. The main difference between Bert and Roberta which makes Roberta perform well is dynamic masking technique and removal of next sentence prediction (NSP). Also, Roberta is trained on a larger set of data than Bert.

# W-NUT Shared Task 2
The challenge is to differentiate the informative and uninformative tweets collected basing on current topic Covid-19. A tweet is labelled as informative if it contains any information regarding new or suspicious cases and uninformative in rest of the cases.

## Dataset
The given dataset consists of train set and valid set, each containing 7000 and 1000 tweets respectively. The unlabelled test dataset of 12000 tweets was also released as a part of Codalab competition organized by W-NUT 2020 - Shared Task 2. We have secured 35th position in the competition.



#### Following are the steps performed to detect the label of Covid19 tweets - 

1. Cleaning the dataset.
2. Analyzing the dataset.
3. Applying supervised Conventional approaches.
4. Applying transformer based approaches.
5. Analyzing the results of all approaches.


## Conventional Approaches ( Tf-IDf and Count Vectors )
1. Logistic Regression
2. SVM
3. Naive Bayes
4. Random Forest Classifier
5. 2-layered MLP

## Transformer Based Approaches
1. BERT ( Pretrained model - bert-base-uncased )
2. RoBERTa ( Pretrained model - roberta-base )
3. DistilBERT ( Pretrained model - distilbert-base-uncased )
4. Albert ( Pretrained model - albert-base-v1 )

## Results

Roberta outperformed all methods in both approaches after considering the average of F1 scores obtained after several times of execution.






