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

PROCESS STEPS: 
0. Install transformers
1. Import necessary libraries and Check out for GPU. 
2. Clean the data 
3. Tokenize the sentences/ tweets using respective pre-trained tokenizer and map them to unique Ids ( Be sure of applying a prefix space especially in case of Roberta )
4. Pad the input token ( Also, the sentences are truncated to 100 tokens )
5. Use attention masks to differentiate the padded Id and actual token Id
6. Split the training set into train and Dev (Choosen ratio 9:1)
7. Batch size is as 32 and the respective batches are loaded using dataloader
8. Choose an Optimizer ( AdamW is considered here )
9. Set torch seed and numpy seed as zero to maintain reproducibility
10. Now, its the time to train the train dataset using the pre-trained model
    - The train batches were trained with step size of 40 ( 40 datapoints at a time )
    - Choosen number of epochs is 4 
    - Perform a backward pass (Token-type-Ids are not considered in case of Distilbert)
    - Note the losses
    - evaluate the Dev set 
11. Visualize the training loss ( feel happey :) )
12. Preduct Labels for Valid dataset 
    - Split into batches and evaluate ( to reduce time of computation and execution )
    
## Results

Roberta outperformed all methods in both approaches after considering the average of F1 scores obtained after several times of execution.






