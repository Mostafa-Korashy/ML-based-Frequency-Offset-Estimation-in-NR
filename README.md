# ML-based Carrier-Frequency Offset Estimation in NR

This repo is for the dataset presented in the paper 

## CFO Problem Definition
Carrier frequency offset (CFO) arises from the intrinsic mismatch between the oscillators of a wireless transmitter and the corresponding receiver, as well as their relative motion (i.e., Doppler effect). Despite advances in CFO estimation and tracking techniques, estimation errors are still present. Residual CFO creates a time-varying phase error, which degrades the decoder’s performance by increasing the symbol error rate. The objective is estimate the CFO at a high-degree of accuracy using advanced machine learning techniques. 

## Dataset Description
It is of crucial importance to have a large and well-annotated dataset to build any predictive model. Although being at the heart of any communication system, this standardized publicly available dataset is not available for the problem of CFO estimation. This dataset is presented here in order to stimulate further studies in this area. We built a dataset to cover a wide range of SNRs, namely, from $SNR=-10$ db to $SNR=10$ db with a step of $2$ db. For each SNR $\in \{-10, -8, \dots, 10\}$ , we generated uniformly distributed frequency offsets (FO). We generated a file for each SNR separately. This facilitates designing a model for each SNR value. A larger collection of randomly generated FO with different SNR values has been also  generated that could be used for training a universal model that predicts the FO for any SNR value. The data has been formatted as comma-separated values (CSV) files. 

To motivate the community to further explore this interesting research direction, we released the dataset as an open-source. The dataset consists of 12 CSV files. Each SNR value has one file as well as one file for the aggregated data from different SNR. Providing the data of each SNR separately helps in building ensemble models with the help of a multiplexer to select the model corresponding to the estimated SNR. Table \ref{table:dataset_files} shows the details of each file.
