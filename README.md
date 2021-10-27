# S5-Assignment
Reach 99.4 plus test accuracy with less than 10k parameters in 15 epochs

## Step 1 : ##

  ### Target : ###
  Set up a basic skeleton model, train it for 15 epochs to achieve 99.4 test accuracy

  ### Results : ###
  1. Paramteres : 19.6k
  2. Best train accuracy : 99.67
  3. Best test accuracy : 99.02

  ### Analysis : ###
  1. Model is overfitting. Requires regularization
  2. Number of parameters are large

## Step 2 : ##

  ### Target : ###
  1. Make the model lighter i.e. less than 10k
  3. Add regularization by Batchnormalization and Dropout

  ### Results : ###
  1. Paramteres : 9.9k
  2. After Batchnormalization :
     1. Best train accuracy : 99.64
     2. Best test accuracy : 99.25
  3. After Batchnormalization and Dropout
     1. Best train accuracy : 99.40
     2. Best test accuracy : 99.31

  ### Analysis : ###
  1. Difference between train accuracy and test accuracy has lessened
  2. Number of parameters are less than 10k
  3. Test accuracy needs to increase and hit 99.4 or above consistently
  4. GAP needs to be introduced
  
## Step 3 : ## 

  ### Target : ###
  1. Add a GAP layer
  2. Add data augmentation
  3. Experiment with Learning Rate (LR) using LR Scheduler
  
  ### Results : ###
  1. Paramteres : 9.9k
  2. After GAP layer :
     1. Best train accuracy : 99.47
     2. Best test accuracy : 99.43 (once above 99.4)
  3. After GAP and data augmentation
     1. Best train accuracy : 99.19
     2. Best test accuracy : 99.41 (3 times above 99.4)
  4. After GAP , data augmentation and LR experiments
     1. Best train accuracy : 99.20
     2. Best test accuracy : 99.48 (6 times >= 99.4 out of last 9 epochs )
  
  ### Analysis : ###
  1. All factors contribute to increase test accuracy
  2. Data augmentation of random rotation applied
  3. LR scheduler is used to fine tune the LR
  
## Step 4 : ## 

  ### Target : ###
  1. Reduce number of parameters to less than 8k and achieve 99.4 plus test accuracy in 15 epochs
  
  ### Results : ###
  1. Paramteres : 7.9k
  2. Best train accuracy : 99.14
  3. Best test accuracy : 99.53 (last 6 epochs are 99.4 above)
  
  ### Analysis : ###
  1. Number of network parameters reduced by decresing number of channels in CNN pipeline
  2. Model was underfitting, hence dropout layers removed from all layers
  3. Gamma of LR scheduler has been experimented with to achieve 99.4 above

