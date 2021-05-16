# Offensive Tweet Classification

Employing an annotated OLID dataset for offensive tweets, I used python and Keras a deep learning framework to build a deep learning model to complete two tasks -

* **Task 1:** Binary classification of tweets as Offensive and Not Offensive
* **Task 2:** Multiclassifiaction for Subtasks A-C combined, treating this as one single multi-class problem. There are 5 possible classes: NOT, OFF-UNT, OFF-TIN-IND, OFF-TIN-GRP, OFF-TIN-OTH

Dataset - OLID (https://sites.google.com/site/offensevalsharedtask/olid)

**Competition link - OffensEval 2019 (https://sites.google.com/site/offensevalsharedtask/offenseval2019)



## Task 1:


The test data was split into 3 label files and 3 data files for 3 subtasks. The training data was contained in one file with all labels. I implemented the steps below to build the classifier and evaluate it on test data -


    Use pandas dataframe to read dataset and label files for training and test

    -	Read the 3 subtask labels from training dataset file into 3 different lists

    -	Start preprocessing the tweets for both training and test dataset -

       Convert emojis to text, Tokenize using whitespace, 
    
       Remove punctuations, empty, strings, digits, stop words, and the words ‘user’,’url’ and ‘maga’

    -	Created word to index and index to word dictionary out of all possible words in the training data

    -	Converted words in every tweet to IDs that can me mapped back to words using the dictionaries above

    -	Converted test dataset tweets to IDs using the same dictionary and assign a fixed ID to words that are not in the training dataset

    -	Encode string labels to number

    -	Padded each sentence in the pre-processed training and test dataset with zeros for a fixed length

    -	Split training data to training and validation. 3000 samples for validation and rest for training

    -	Fed prepared data into model and obtain training and validation loss and accuracies by training over a fixed number of epochs

    -	Evaluated trained model on trained dataset



## Task 2:

For building the multiclassifier for subtasks A-C which combined 5 specified classes the following steps implemented–
se pandas dataframe to read dataset and label files for training and test

    -	Concatenated the labels for both test and training datasets. 
    
    -	Each entry in the dataset will have one of the labels - NOT, OFF-UNT, OFF-TIN-IND, OFF-TIN-GRP, OFF-TIN-OTH,

    -	Used the same pre-processed training and testing data

    -	Created one hot vector representation for the label data

    -	Changed the hyperparameters and model architecture to adapt to the multi class classification problems
