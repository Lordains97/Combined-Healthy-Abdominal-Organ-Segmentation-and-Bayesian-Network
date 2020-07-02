# Combined Healthy Abdominal Organ Segmentation

Segmentation of four abdominal organs from MRI data sets acquired with two different sequences and to filter out the different organs in order to find the descriptive features of each organ and to create a bayesian inference through those description

# Dataset Explanation

The link for the actual dataset has been uploaded in the folder **'CHAOS DATASET'** and also contains the sample scan file in it along with the ground truth value.

This is the train and testing dataset of Combined (CT-MR) Healthy Abdominal Organ Segmentation (CHAOS) Challenge. This data consists of images of Abdominal CT and MRI from different patients.

There are 20 training and 20 testing cases in the CT dataset. MRI dataset contains 20 training and 20 testing cases with T1-Dual and T2 SPIR sequences. Train data contains both DICOM images and their ground truth masks. The testing set only contains DICOM images. In CT cases only livers were annotated. In MRI cases, livers, left/right kidneys, and spleens were annotated. For further information about the data and challenge, please visit https://chaos.grand-challenge.org/ and read the CHAOS_Submission_Manual.pdf

All the extracted features are stored in the folder **'Extracted Feature Dataset'** that contains the following files

**CHAOS_FEATURE.csv** - Contains all the extracted features of all abdominal organs. 

*Segmented Label values*

0 - Liver  
1 - Spleen  
2 - Left Kidney  
3 - Right Kidney  

**LK.csv** - Contains all the extracted features of Left Kidney. 

*Segmented Label values*

0 - Not Left Kidney  
1 - Left Kidney  

**Liv.csv** - Contains all the extracted features of Liver. 

*Segmented Label values*

0 - Liver  
1 - Not Liver  

**RK.csv** - Contains all the extracted features of Right Kidney. 

*Segmented Label values*

0 - Not Right Kidney  
1 - Right Kidney  

**SP.csv** - Contains all the extracted features of Spleen. 

*Segmented Label values*

0 - Not Spleen  
1 - Spleen  

# Required Libraries for running the code 

numpy  
pandas  
pgmpy   
networkx  
IPython   
sklearn  
seaborn  
pydicom  
matplotlib  
plotly  
scipy  
os  
mpl_toolkits  
skimage  
glob  

# Image Segmentation and Feature Extraction  

1. **Pydicomread.ipynb** - Python notebook for visualising medical dicom images  

2. **pgmmodel.ipynb** - This notebook segements the organs in the original image and gives us the segmented output.  

3. **Contour-Extraction.ipynb** - The segmented output are then given as input to this notebook and the features are obtained. The extracted features are also available in this drive as **CHAOS_FEATURES.csv** file.

# Bayesian Implementation notebooks

1. **Bayesian_Learning_Entire_Dataset.ipynb** - The entire extracted features (chaos_features.csv) is given as input to created Bayesian model.  

2. **Bayesian_Learning_Organ_dataset.ipynb** - The chaos dataset had already been split into various datasets (Liv,LK,RK,SP) which is as input to the Bayesian model



**Note** The code had been successfully implemented in Google Colab as GPU was required for running the program. The code will run on a non-GPU system but it will take a lot of time to generate the model, which is some cases might lead to a non responsive notebook.  