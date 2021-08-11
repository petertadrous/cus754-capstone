# Improving Facial Recognition Performance of Race Classification Using Bayesian Dropout on FairFace Model

## Requirements

The required packages are:
- numpy
- matplotlib
- tensorflow
- pytorch

Base model used was the pretrained resnet34 from [FairFace](https://github.com/dchen236/FairFace) research.  
ResNet34 tensorflow implementation was a modified version of [dmolony3's implementation](https://github.com/dmolony3/Torch_to_TF) with [this line](https://github.com/dmolony3/Torch_to_TF/blob/0685939c753c8ede67fd812b52b584bc2bfa59e9/ResNet/resnet.py#L69) commented out

## Abstract

Recent facial recognition techniques have tried to tackle the issue of imbalanced training data. Insufficient variability in training data has been shown to explain most of the reduction in performance when ResNet34 is presented with images balanced by race, and I will attempt to pinpoint exactly where any other biases may lie. There is significant performance improvement in models that are tasked with recognizing faces that are included in their training data, which is why it’s crucial to include all races in the training data. However, many widely used open source datasets are not very diverse, and as Dulhanty et al. notes, bias in training data begets bias in model performance. Algorithmic auditing of commercial face analysis applications has uncovered disparate performance for intersectional groups across several tasks. Poor performance for darker skinned females by commercial face analysis APIs has been reported, along with lower accuracy in face identification by commercial systems with respect to “lower skin reflectance”, i.e. darker skin, by researchers at the US Department of Homeland Security. Directly from LFW dataset’s website: “Many groups are not well represented in LFW. For example, there [is] … a relatively small proportion of women. In addition, many ethnicities have very minor representation or none at all.”

## References 

- Kärkkäinen, K. and Joo, J. 2019. *FairFace: Face Attribute Dataset for Balanced Race, Gender, and Age*.
- Chou, Hsin-Rung, Jia-Hong Lee, Yi-Ming Chan, and Chu-Song Chen. 2018. *Data-Specific Adaptive Threshold For Face Recognition And Authentication*.
- Deng, Jiankang, Jia Guo, Yuxiang Zhou, Jinke Yu, Irene Kotsia, and Stefanos Zafeiriou. 2019. *Retinaface: Single-Stage Dense Face Localisation In The Wild*.
- Deng, Jiankang, Jia Guo, Niannan Xue, and Stefanos Zafeiriou. 2018. *Arcface: Additive Angular Margin Loss For Deep Face Recognition*.
- Dulhanty, Chris, and Alexander Wong. 2020. *Investigating The Impact Of Inclusion In Face Recognition Training Data On Individual Face Identification*.
- Buolamwini, Joy and Gebru, Timnit. 2018. *Gender shades: Intersectional accuracy disparities in commercial gender classification*.
- Wu, Wenying and Protopapas, Pavlos and Yang, Zheng and Michalatos, Panagiotis. 2020. *Gender Classification and Bias Mitigation in Facial Images*.
- Gal, Yarin, and Zoubin Ghahramani. 2015. *Dropout As A Bayesian Approximation: Representing Model Uncertainty In Deep Learning*.

## Acknowledgements

- https://github.com/dchen236/FairFace
- https://github.com/dmolony3/Torch_to_TF
