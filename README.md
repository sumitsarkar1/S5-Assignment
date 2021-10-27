# S5-Assignment
Reach 99.4 plus test accuracy with less than 10k parameters in 15 epochs

Step 1 : 

  Target :
  Set up a basic skeleton model, train it for 15 epochs to achieve 99.4 test accuracy

  Results :
  a.) Paramteres : 19.6k
  b.) Best train accuracy : 99.67
  c.) Best test accuracy : 99.02

  Analysis :
  a.) Model is overfitting. Requires regularization.
  b.) Number of parameters are large

Step 2 :

  Target :
  a.) Make the model lighter i.e. less than 10k
  b.) Add regularization by Batchnormalization and Dropout

  Results :
  a.) Paramteres : 9.9k

  --------------------------After Batchnormalization-------------------------
  a.) Best train accuracy : 99.64
  b.) Best test accuracy : 99.25

  -------------------- After Batchnormalization and Dropout------------
  a.) Best train accuracy : 99.40
  b.) Best test accuracy : 99.31

  Analysis :
  a.) Difference between train accuracy and test accuracy has lessened
  b.) Number of parameters are less than 10k
  c.) Test accuracy needs to increase and hit 99.4 or above consistently
  d.) GAP needs to be introduced
  
Step 3 : 

  Target :
  a.) Add a GAP layer
  b.) Add data augmentation
  c.) Experiment with Learning Rate (LR) using LR Scheduler
  
  Results :
  a.) Paramteres : 9.9k
  
  --------------------------After GAP layer------------------------------------------
  a.) Best train accuracy : 99.47
  b.) Best test accuracy : 99.43 (once above 99.4)
  
  -------------------- After GAP and data augmentation----------------------
  a.) Best train accuracy : 99.19
  b.) Best test accuracy : 99.41 (3 times above 99.4)
  
  -----------After GAP , data augmentation and LR experiments-------
  a.) Best train accuracy : 99.20
  b.) Best test accuracy : 99.48 (6 times >= 99.4 out of last 9 epochs )
  
  Analysis :
  a.) All factors contribute to increase test accuracy
  b.) data augmentation of random rotation applied
  b.) LR scheduler is used to fine tune the LR
  
Step 4 : 

  Target :
  a.) Reduce number of parameters to less than 8k and achieve 99.4 plus test accuracy in 15 epochs
  
  Results :
  a.) Paramteres : 7.9k
  b.) Best train accuracy : 99.14
  c.) Best test accuracy : 99.53 (last 6 epochs are 99.4 above)
  
  Analysis :
  a.) Number of network parameters reduced by decresing number of channels in CNN pipeline
  b.) Model was underfitting, hence dropout layers removed from all layers
  c.) gamma of LR scheduler has been experimented with to achieve 99.4 above

