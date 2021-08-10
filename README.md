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
