
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
This work introduces a new approach to recognize abnormal events in video sequences. Traditional auto-encoders(AEs) can reconstruct normal samples and abnormal samples well. To tackle this issue, we employ a pseudo anomaly synthesizer to generate synthetic anomalies from normal data and design two decoders to reconstruct normal and pseudo anomaly samples,respectively. We train the
model to maximize the reconstruction loss on pseudo anomalies while minimizing it on normal data. To further distinguish between normal and abnormal representations, we implement L1 distance and Kullback-Leibler divergence (KLD) to enhance the distinction in numerical value and data distribution. Additionally, KLD is used to distinguish the outputs of two decoders.
## Training/Inference
Train and evaluate the model.

```bash
python T3.py
```
