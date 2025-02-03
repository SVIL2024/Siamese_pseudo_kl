
# Distance-augmented Deep Autoencoder with a Siamese Architecture for Video Anomaly Detection

This paper is submited to The Visual Computer.


## Authors



Liang Zhang
, Shifeng Li 
, Yan Cheng
, Xi Luo
, Xiaoru Liu
Corresponding author: Shifeng Li limax_2008@outlook.com
## Description
Video anomaly detection (VAD) the task of identifying anomalous events in video sequence, where anomalous events refer to unanticipated actions. Unanticipated actions rely on scene, what is unusual in one scene may be normal in another.This work introduces a new approach to recognize abnormal events in video sequences. Traditional auto-encoders (AEs) can reconstruct normal samples and abnormal samples well. To tackle this issue, we employ a pseudo anomaly synthesizer to generate synthetic anomalies from normal data and design two decoders to reconstruct normal and pseudo anomaly samples, respectively. We train the model to maximize the reconstruction loss on pseudo anomalies while minimizing it on normal data. To further distinguish between normal and abnormal representations, we implement L1 distance and Kullback-Leibler divergence (KLD) to enhance the distinction in numerical value and data distribution. Additionally, KLD is used to distinguish the outputs of two decoders.
## Training/Inference
Train and evaluate the model in file "T3.py".

```bash
python T3.py
```
## Points

#### Datasets
To validate and benchmark our method against the state of the art, we conduct experiments on several diverse datasets:[ UCSD Ped2](http://www.svcl.ucsd.edu/projects/anomaly), [ CUHK Avenue](http://www.cse.cuhk.edu.hk/leojia/projects/detectabnormal/dataset.html), [ShanghaiTech](https://svip-lab.github.io/dataset/campus_dataset.html).

#### Anomalies
We simulate anomalous behavior by incorporating both motion and appearance information. The pseudo-anomalies in video sequences consist of two distinct phases: skip frames and adding noise. We limit the pseudo-anomaly data in the model by probability p. The skip frames is architected by "Reconstruction3DDataLoaderJump" in file "data.py" and noise is added by "gaussian" in file "utils.py".

#### Our loss for siamese architected model
The loss for siamese architected model include feature loss and output loss. We utilize the KLD loss and L1 loss capture capture the differences between normal and abnormal latent representations in terms of both value and distribution. Only L1 loss is implemented to increase the distance of normal and abnormal reconstructed outputs. They are used in training phase. These loss functions are "kl_fea" and "loss_feas" in file "T3.py".
