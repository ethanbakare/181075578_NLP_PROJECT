# 181075578_NLP_PROJECT
Final year project QMUL


The dataset folder contains:
The test, train and validation data samples required to run the code

Test = test_data_hs

Train = train_data_hs

Validation = val_data_hs


%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%
%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%

Easy data augmentation techniques for for hate speech classifcation.
These are a set of data augmentation techniques that are easy to implement

Synonym Replacement (SR): Randomly choose n words from the sentence that are not stop words. Replace each of these words with one of its synonyms chosen at random.
Random Insertion (RI): Find a random synonym of a random word in the sentence that is not a stop word. Insert that synonym into a random position in the sentence. Do this n times.
Random Swap (RS): Randomly choose two words in the sentence and swap their positions. Do this n times.
Random Deletion (RD): For each word in the sentence, randomly remove it with probability p.


%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%
%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%


There are 15 concatenated combinations made on these techniques as such we have 15 augmented training dataset 

To run them open the data set file shown in the github link, download them, then proceed to change the address 
in the second line of code for the file titled: 000_DA_HS

the github repo
Open the code file 
