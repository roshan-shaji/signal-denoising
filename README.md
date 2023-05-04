**Team Name:** RAD


**Team Members:**

Dyuti Mangal 190101035 CSE BTech


S Roshan 190101079 CSE BTech 


Anuraag Mahajan 190101110 CSE BTech 


**Project Title:** Signal Denoising using RNN


**Objective:** The objective of this project is to train a recurrent neural network (RNN) to map noisy speech signals to clean speech signals. Further, we aim to test the network on an independent test set to measure its denoising performance and draw comparisons with different models.




**Background:**
The presence of noise can make it difficult to accurately analyze signals, and can affect the quality of the results obtained from further processing. For instance, in medical imaging, removing noise can improve the accuracy of diagnostic tests. Neural networks can learn to identify and remove noise even in complex or nonlinear signals. Traditional methods like smoothing, are often designed to work with specific types of noise or signal characteristics.Denoising using RNNs has been shown to be effective, particularly for removing longer-term noise patterns that occur over longer timescales.


**Methodology:** We will use a publically available dataset of subjects speaking short sentences along with a synthetic noise to be added to these to train and test our model. The dataset will be then preprocessed to obtain the STFT representation of the noisy and clean speech signals.
Using this the IBM matrix can be computed as the element-wise ratio of the STFT of the clean signal to the STFT 
of the noisy signal.
The architecture of the RNN will be using LSTM units, which is suitable for processing sequential data like speech 
signals. We will then train the RNN using the noisy STFT signal as inputand the IBM matrix as the target output. The performance of the trained RNN will be evaluated using a validation set and test it on an independent test set of noisy speech signals to measure its denoising performance.
Post-processing can be done on the denoised STFT signal to obtain a time-domain signal by applying the inverse STFT.




**Deliverables:** * A .ipynb notebook with the denoising RNN model * A GitHub repository containing the source code and documentation of the project. * An oral presentation in class.


**Dataset to be used:** We will be using the Mozilla common voice dataset. It is an open source multi-language dataset where each entry in the dataset consists of a unique 48kHz MP3 and corresponding text file. Many of the 27,142 recorded hours in the dataset also include demographic metadata like age, sex, and accent that can help train the accuracy of speech recognition engines. The dataset currently consists of 17,690 validated hours in 108 languages.


**Repository Description:**
1. ```gen_noisy_data.ipynb``` : Jupyter Notebook for generating noisy data
2. ```denoising_rnn.ipynb``` : Jupyter Notebook containing denoising model and results
