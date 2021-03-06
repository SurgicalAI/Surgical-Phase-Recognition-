# Surgical-Phase-Recognition-
Deep Temporal Model for Surgical Phase Recognition

Demo notebook for laparoscopic cholecystectomy phase recognition using a CNN-biLSTM-CRF.

Learning from a tiny dataset of manual annotations: a teacher/student approach for surgical phase recognition (IPCAI 2019)

Tong Yu, Didier Mutter, Jacques Marescaux, Nicolas Padoy

arXiv colab

Description
Laparoscopic cholecystectomy is a surgical procedure for removing a patient's gallbladder. As a minimally invasive procedure it is video-monitored via endoscopic cameras.

Our algorithm analyzes the video recordings from those cameras to automatically identify the 7 surgical phases making up the procedure:

Preparation
Calot triangle dissection
Clipping and cutting
Gallbladder dissection
Gallbladder retraction
Cleaning and coagulation
Gallbladder packaging
The underlying deep neural network is a stack of:

Resnet-50
Bidirectional LSTM
Linear-chain CRF
model

Training was performed on 80 videos from cholec120, a superset of the publicly released cholec80 dataset available here.

On a test set of 30 videos from cholec120, accuracy reaches 89.5%. Average F1 score over all 7 phases reaches 82.5%.

Requirements
Python 3
Tensorflow 1.14
numpy
opencv 3.4
matplotlib
ruamel_yaml
Developer configuration info:

Ubuntu 20.04
CUDA 10.1
NVIDIA GTX1080Ti GPU
TF-Cholec80
TF-Cholec80 provides a user-friendly interface for manipulating a dataset of cholecystectomy recordings we previously released. A phase recognition demo using it is available in this repo: (phase_recognition_demo_tfc.ipynb).

Citation
@inproceedings{yu2019surgicalphase,
title = {Learning from a tiny dataset of manual annotations: a teacher/student approach for surgical phase recognition},
author = {Tong Yu, Didier Mutter, Jacques Marescaux, Nicolas Padoy},
booktitle = {International Conference on Information Processing in Computer-Assisted Interventions},
year = {2019}
}
License
This code may be used for non-commercial scientific research purposes as defined by Creative Commons 4.0. By downloading and using this code you agree to the terms in the LICENSE. Third-party codes are subject to their respective licenses.
