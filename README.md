# SRM Resting-state EEG Dataset

## Introduction
Welcome to the SRM Resting-state EEG dataset! This dataset contains resting-state EEG data obtained from the Stimulus-Selective Response Modulation (SRM) project at the Department of Psychology, University of Oslo, Norway. The data is recorded using a BioSemi ActiveTwo system with 64 electrodes following the positional scheme of the extended 10-20 system (10-10). Each data file consists of four minutes of uninterrupted EEG acquired while subjects rested with their eyes closed. The dataset includes EEG data from 111 healthy control subjects, referred to as the "t1" session. Some subjects have one associated EEG file, while others have two, as they underwent an additional EEG recording at a later date (the "t2" session).

## Disclaimer
Please note that the dataset is provided "as is." The authors of this dataset do not take responsibility for data quality. Users are solely responsible for ensuring that the data meet the required quality criteria for their publications or other use cases.

## The Data
### Raw Data Files
The raw EEG data signals are rereferenced to the average reference, and no other operations have been performed on the data. These files do not contain events; the entire continuous segment represents resting-state data. The data signals are unfiltered (recorded in Europe, with a line noise frequency of 50 Hz). The time points for the EEG recordings for each subject are listed in the *_scans.tsv file, which is particularly useful for subjects with two recordings. While most data files are of high quality, a few may be of lower quality. It is the user's responsibility to assess the quality of each individual data file.

### Cleaned Data
For convenience, we provide a cleaned dataset in the "/derivatives/cleaned_data" directory. The files in this derived dataset have been preprocessed with a basic, fully automated pipeline (refer to /code/s2_preprocess.m for details). The derived files are stored as EEGLAB .set files in a directory structure identical to that of the raw files. The *_channels.tsv files associated with the derived files have been updated with status information about each channel ("good" or "bad"). The "bad" channels are interpolated but are still present in the data. For some analyses, it may be advisable to remove these channels, as they do not contribute meaningful information to the EEG data. Please be aware that the employed pipeline is automatic and may not perform optimally on all data files. For publications, we recommend implementing a more sensitive cleaning pipeline.

### Demographic and Cognitive Test Data
The "participants.tsv" file in the root folder contains variables such as age, sex, and a range of cognitive test scores. You can find additional information about the behavioral measures in the sidecar "participants.json" file. Note that these measures were collected in connection with the "t1" session recording.

## How to Cite
If you use this dataset in your publication, please cite the following paper:

Hatlestad-Hall, C., Rygvold, T. W., & Andersson, S. (2022). BIDS-structured resting-state electroencephalography (EEG) data extracted from an experimental paradigm. Data in Brief, 45, 108647. [https://doi.org/10.1016/j.dib.2022.108647](https://doi.org/10.1016/j.dib.2022.108647)


