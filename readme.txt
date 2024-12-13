The repository contains the dataset - bank-full.csv and the jupyter notebook term_deposit_prediction.ipynb for the code.
Both these files can be uploaded on AWS and run. For reference, I have created a jupyter notebook instance Amazon Sagemaker with the ml.t3.xlarge instance.
The notebook contains some EDA, data preprocessing and implementation of 4 classification models.

When run, the user will be prompted twice for an input: 1. Selecting a method to handle class imbalance(SMOTE/undersampling) during the preprocessing stage 
and finally 2. Selecting a classification model. User needs to enter the desired selection as prompted for the code implementation to proceed.
