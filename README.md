# DeepLearning_OcularDisease
This notebook explores the ODIR dataset, which contains information about 5,000 patients with age, color fundus photographs from left and right eyes, and doctors' diagnostic keywords. The goal is to classify the annotations (normal or cataract) based on image analysis.

Here's a breakdown of the key findings and steps performed in the notebook:

## Data Exploration:

The dataset contains information on patients' age, sex, fundus photographs (left and right), and diagnostic keywords for each eye.
Some diagnostic categories ("N", "D", "G", etc.) represent findings for both eyes, but the data doesn't specify which eye they belong to. This could be problematic for later analysis.
Exploratory data analysis (EDA) is performed to visualize the distribution of features like patient age, normal/cataract diagnosis, and patient sex.

## Data Preprocessing:

Columns containing diagnosis categories ("N", "D", "G", etc.) are excluded for this analysis because they provide ambiguous information about which eye the diagnosis refers to.
Separate DataFrames are created for left and right eye diagnoses with "cataract" based on keywords in the "Left-Diagnostic Keywords" and "Right-Diagnostic Keywords" columns.
The filenames of the cataract images (left and right eye) are combined into a single DataFrame.

## Image Exploration:

A sample of cataract images is displayed as a grid to visualize what cataracts look like in the dataset.
A similar process is followed to select and display a random sample of "normal" images.

## Note:
The notebook highlights a potential issue with the way diagnostic categories are encoded. This could be addressed in future analysis by finding alternative ways to represent diagnoses specific to each eye.
The selection of a random sample of "normal" images ensures a balanced dataset for training the classification model (equal number of cataracts and normal images).
