---
title: "Uncertainty Reduction for Model Adaptation in Semantic Segmentation"
collection: publications
permalink: /publications/model_adaptation
# excerpt: 'This paper is about the number 1. The number 2 is left for future work.'
date: 2021-03-01
venue: 'IEEE/CVF Conference on Computer Vision and Pattern Recognition (CVPR)'
# paperurl: 'http://prabhuteja12.github.io/files/PrabhuTeja2013Ballistic.pdf'
# citation: 'Teja, S. Prabhu, and Anoop M. Namboodiri. "A ballistic stroke representation of online handwriting for recognition." In 2013 12th International Conference on Document Analysis and Recognition, pp. 857-861. IEEE, 2013.'
---
<!-- Download paper [here](../files/sivaprasad21a-cvpr.pdf) and the supplementary material [here](../files/sivaprasad21a-cvpr-supp.pdf) -->
Download paper [here](http://publications.idiap.ch/downloads/papers/2021/Sivaprasad_CVPR_2021.pdf){:target="_blank"}.

Code is available [here](https://github.com/idiap/model-uncertainty-for-adaptation){:target="_blank"}.

## Abstract 
Traditional methods for Unsupervised Domain Adaptation (UDA) targeting semantic segmentation exploit information common
to the source and target domains, using both labeled source data and unlabeled target data. In this paper, we
investigate a setting where the source data is unavailable, but the classifier trained on the source data is; hence
named ``model adaptation''. Such a scenario arises when data sharing is prohibited, for instance, because of privacy, or
Intellectual Property (IP) issues.

To tackle this problem, we propose a method that reduces the uncertainty of predictions on the target domain data. We
accomplish this in two ways: minimizing the entropy of the predicted posterior, and maximizing the noise robustness of
the feature representation. We show the efficacy of our method on the transfer of segmentation from computer generated
images to real-world driving images, and transfer between data collected in different cities, and surprisingly reach
performance comparable with that of the methods that have access to source data.