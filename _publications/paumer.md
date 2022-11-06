---
title: "PAUMER: Patch Pausing Transformer for Semantic Segmentation"
collection: publications
permalink: /publications/paumer
date: 2022-11-01
venue: 'British Machine Vision Conference (BMVC)'
---

Download paper [here](../files/courdierBMVC2022.pdf){:target="_blank"}.


## Abstract

We study the problem of improving the efficiency of segmentation transformers by using disparate amounts of computation
for different parts of the image. Our method, PAUMER, accomplishes this by pausing computation for patches that are
deemed to not need any more computation before the final decoder. We use the entropy of predictions computed from
intermediate activations as the pausing criterion, and find this aligns well with semantics of the image. Our method has
a unique advantage that a single network trained with the proposed strategy can be effortlessly adapted at inference to
various runtime requirements by modulating its pausing parameters. On two standard segmentation datasets, Cityscapes and
ADE20K, we show that our method operates with about a 50% higher throughput with an mIoU drop of about 0.65% and 4.6%
respectively.
