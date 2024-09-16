
# Video Anomaly Detection using a Siamese Network with Pseudo Anomalies

A brief description of what this project does and who it's for


## Authors



Liang Zhang
, Shifeng Li 
, Yan Cheng
, Xi Luo
, Xiaoru Liu
Corresponding author: Shifeng Li limax 2008@outlook.com
## Description
This work introduces a novel method for detecting abnormal events in video sequences using a Siamese network. Traditional autoencoders (AEs) often face challenges in distinguishing between normal and abnormal samples, as they can effectively reconstruct both types. To address this issue, we propose integrating pseudo-anomalous samples into the Siamese network framework. Our method begins with a pseudo-anomaly synthesizer that creates synthetic anomalies from normal data. These normal and pseudo-anomalous samples are processed by a Siamese network comprising one encoder and two decoders, which are designed to reconstruct normal and pseudo-anomalous samples, respectively. The network is trained to maximize reconstruction loss for pseudo-anomalous samples while minimizing it for normal samples. Additionally, we introduce two loss functions—feature loss and output loss—that enhance the separation between normal and abnormal representations. These loss functions utilize $L_1$ distance and Kullback-Leibler Divergence (KLD) to distinguish between numerical values and data distributions. Experimental results on public datasets validate the effectiveness of our approach for video anomaly detection. 
## Training/Inference
Train and evaluate the model.

```bash
python T3.py
```
