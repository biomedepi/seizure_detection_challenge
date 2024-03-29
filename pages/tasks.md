---
title: Tasks
background: /assets/theme/images/bckg.png
permalink: /tasks/
---

### **<span style="color:#2B547E">Task 1 - Seizure detection</span>**
\
The first task of this challenge involves developing a ML model for detecting seizures in the wearable SD data. As training set the contestants will be able to use the full SeizeIT1 dataset (vEEG, bhe-EEG, ECG), while the test set will contain data captured with the wearable SD device (bhe-EEG and ECG, no vEEG). The contestants are allowed, but not obliged, to use (in a transfer learning-scheme) the information of the full scalp EEG (vEEG) in the training set. As a baseline method, for comparison purposes, the approach presented in Vandecasteele et. al [1] can be used.

![alt text]({{ '/assets/theme/images/task1.png' | relative_url }})
A pretrained model (either in Python or in Matlab) must be submitted. Additionally, the routines used for pre- and post-processing should be included. The models must provide a vector of zeros (non-seizure) and ones (seizure) as an output with length equal to the number of seconds of a recording. The framework should receive as input the wearable EEG data from the SD device (2-channel EEG time series) and/or the wearable single-channel ECG data (in case the model was developed with both modalities - see [2] for a study on seizure detection with multimodal data).

&nbsp;  

### **<span style="color:#2B547E">Task 2 - Data centric seizure detection</span>**
\
![alt text]({{ '/assets/theme/images/task2.png' | relative_url }}){: .rounded .float-end}
Data is the main ingredient for developing automated classifiers. Most researchers have focused on developing state-of -the-art AI architectures in order to achieve better classification performance in many diverse tasks. Recently, the concept of ‘data-centric AI’ has risen as a promising option for achieving higher and better performances in hard classification problems.

Usually, training a model with high volumes of data tends to aid its robustness and reliability. Deep neural network schemas exhibit low bias along with high variance; the common approach of handling the variance problem is the employment of extra data. However, it is also known that data quality highly impacts the behavior of ML models. Poor performances are seen in out-of-distribution data instances and within heterogeneous regions of in-distribution data. Furthermore, datasets may contain labeling inconsistencies which can cause deceptions when training automated models for certain tasks. In the epilepsy use case, datasets suffer from a high imbalance between classes, where seizure events are short and rare when compared to the overall recordings.

We argue that by focusing on the quality of the data and by including representative cases in the training set, it is possible to achieve optimal performances within seizure detection frameworks. In contrast to task 1, the objective of task 2 is to apply data manipulation techniques in order to obtain the best performance (in terms of robustness and generalizability) of the provided model for wearable seizure detection.

In this task, participants will have access to the same training set as in task 1 and provided with a Deep Learning model. The model is an adapted version of the ChronoNet [3], a mixed convolutional and recurrent neural network composed of 1-D convolutional layers followed by a stack of gated recurrent units with skip connections. This framework was originally developed for abnormal EEG identification and has been adapted and optimized by the organizers for seizure detection. Participants are encouraged to apply any pre-processing techniques, data-augmentation, subsampling strategies, etc., in order to build a training set to feed the model.

The input segment size of the model is fixed at 2 second 2-channel EEG windows resampled at a sampling frequency of 200 Hz [400 samples x 2 channels]. The model’s architecture will be shared and the training routine cannot be changed by the participants. The model was implemented in python, with the use of the Keras API.
The output should be a vector of zeros (non-seizure) and ones (seizure) for each consecutive 2 second EEG segment. Both the **data processing and manipulation pipeline** and the **trained model’s weights** (serialize weights in HDF5 format) have to be submitted.

As a baseline, the metrics were computed with a model trained using all bhe-EEG seizure data segments of SeizeIT1 and randomly selected non-seizure data segments with a balancing factor of 10. The performance obtained was 58.22% sensitivity with a 117.12 false alarm rate (false alarms per hour).

&nbsp;  

#### References

[1] K. Vandecasteele et al., "Visual seizure annotation and automated seizure detection using behind-the-ear elec- troencephalographic channels", Epilepsia, vol. 61, no. 4, pp. 766–775, 2020.

[2] K. Vandecasteele, et al., "The power of ECG in multimodal patient-specific seizure monitoring: Added value to an EEG-based detector using limited channels", Epilepsia. 2021; 62: 2333– 2343.

[3] S. Roy et al., "Chrononet: A deep recurrent neural net- work for abnormal eeg identification", Artificial Intelligence in Medicine. 2019, pp. 47–56.