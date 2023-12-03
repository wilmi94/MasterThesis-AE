# Master Thesis Aerospace Engineering
> This repository is part of the Master Thesis *Predicting Coronal Mass Ejections using Machine Learning methods* by Wilmar Ender, FH Wiener Neustadt, 2023.

**Abstract**

This Master’s thesis examines the potential of Convolutional Neural Networks and Recurrent Neural
Networks for predicting solar phenomena like Coronal Mass Ejections and Solar Flares in the context
of Space Weather forecasting. The focus is on refining prediction accuracy by encompassing both
spatial and temporal characteristics.
The study addresses several objectives. Firstly, optimal satellites and instruments for data acquisition
are identified, and data sufficiency for effective model training is evaluated. Subsequently, RNNs are
introduced to model temporal solar activity patterns. Advanced Data Science and Machine Learning
techniques are employed following the CRISP-DM methodology.
The research culminates in applying ConvLSTM prediction models, using only full-disk image data
from the Solar Dynamics Observatory’s Atmospheric Imaging Assembly instrument. The model
captures spatial and temporal dynamics, thereby supporting the precision of CME predictions.


The repository is structured the following way:
## data
The following sub-folders hold the essential CSV files from Liu et. al 2020, containing the event lists.

### bin_class
*all_cme_events.csv* - the ''base-list'' contains all the considered CME events and non-events.

*sample.csv* - sample of the above list

### conv_lstm
*all_cme_events.csv* - same lsit as above

*normalized_testing_12.csv* - based on the ''base-list'' the training list contains all the samples for a prediction window of 12hr before the CME happend.

*normalized_training_12.csv* - equivalent list, just for training.

## docs
Master_Thesis_ENDER.pdf

## notebooks
### *sdo_binclass.ipynb*

The notebook is addressed in section 4.3 in the thesis and aims to apply a binary classifier on the used SDO/AIA image dataset.

**Objectives:**

* perform data exploration and getting used to the dataset
* develop helper functions and code for the subsequent prediction model
* test and apply a binary classification model
* evaluate the models to get a baseline in terms of performance.

### *sdo_cli_tests.ipynb*
Little Test-notebook on how to work with *sdo-cli*.

### *sdo_data_exploration.ipynb*
This notebook aims to perform simple data exploration tasks on SDO/AIA dataset.

**Objectives:**

* perform data exploration and getting used to the dataset
* manually inspect the images
* create and illustrate sample sequances for different wavelength and time intervalls

### *sdo_ConvLSTM.ipynb*
This notebook is considered the prediction model of the thesis and is addressed in section 4.5 in thesis.

**Objective**:
* This notebook aims to perform the prediction of CMEs based on a given sequence of full-disk images from the SDO/AIA dataset.
* apply a ConvLSTM model on the dataset and
* Evaluate the ''reliability'' of such a pure black-box approach in terms of CME prediction.
