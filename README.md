# DeepLearning: OcularDisease
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

## Model Architecture and Performance:
This section details the models implemented and their performance on the ODIR dataset for cataract classification.

Models: VGG16 and VGG19 convolutional neural networks (CNNs) were employed.
Transfer Learning: Pre-trained weights from these models were used for efficiency and performance.
Hyperparameter Tuning: Batch size, epochs, and learning rate were optimized.
Activation Functions: ReLU and SeLU functions were adopted for non-linearity.
Cost Function: Binary cross-entropy was employed for loss calculation.
Gradient Descent: ADAM optimizer was used for training.

## Results:

VGG16: Achieved an accuracy of 0.9068 on the test set.
VGG19: Achieved an accuracy of 0.718 on the test set.
Visualization: EDA and plot accuracy graphs were generated.

## Dependencies

Python
TensorFlow/Keras
OpenCV
Pandas
NumPy
Matplotlib
Seaborn

```markdown
## Dependencies

pip install tensorflow keras opencv-python pandas numpy matplotlib seaborn

```bash


## Usage Instructions

Install required libraries.
Download and pre-process the ODIR dataset.
Run the notebook cells sequentially.
Analyze the results and visualizations.

## Future Work

Explore other deep-learning architectures for classification.
Investigate techniques for handling imbalanced datasets.
Integrate the model into a web application for real-time predictions.

