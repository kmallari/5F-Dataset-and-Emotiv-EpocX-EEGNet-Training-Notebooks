
# 5F-Dataset and Emotiv EpocX EEGNet Training Notebooks
This repository contains the Jupyter notebooks used by Neil Limbaga, Kevin Mallari, and Nathan Yeung for their undergraduate thesis titled "Development of an EEG-based Brain-Controlled System for a Virtual Prosthetic Hand."

## Abstract of the Study
Meant to improve the overall quality of life for those with physical or motor impairments, this paper explores the use of EEG and its potential in controlling a prosthetic hand. EEG signals acquisition centered on oscillatory features through the sensory motor rhythm which can be obtained through motor-imagery (MI). The EEGNet, a convolutional neural network, is used for feature extraction and signal classification of five motor-imageries classes of a hand. A reinforced model through a transfer learning approach deemed to have the best cross-validation accuracy. A real-time debugging module for the virtual hand was implemented using MuJoCo HAPTIX, with an average operational time of 2.37± 0.39 seconds per motor-imagery.

## About the notebooks
The notebooks are used to ultimately train the 5F dataset from [the study of Kaya et al](https://figshare.com/collections/A_large_electroencephalographic_motor_imagery_dataset_for_electroencephalographic_brain_computer_interfaces/3917698) together with the researchers' own data gathered from their own BCI device, the [EMOTIV EPOC X.](https://www.emotiv.com/epoc-x/)
### Features
- Reading `.mat` files from the 5F dataset and converting them into pandas dataframes.
- Reading `.edf` and `.csv` files from our own gathered data and converting them into mne `raw` objects, and ultimately to pandas dataframes.
- Preprocessing the 5F dataset to reduce its number of channels.
- Preprocessing all the data using a bandpass filter and exponential moving standardization.
- Extracting the EEG signal data that only correspond to significant events for both the datasets.
- Epochs and windows the dataset to split into training and validation sets.
- Trains the [EEGNet](https://arxiv.org/abs/1611.08024) model in multiple ways. Either through cross-subject validation or within-subject validation. The notebook can also undergo transfer learning and fine tuning.

# Link to the study
Paper still in progress.
