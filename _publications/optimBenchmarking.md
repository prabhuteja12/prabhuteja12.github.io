---
title: "Optimizer Benchmarking Needs to Account for Hyperparameter Tuning"
collection: publications
permalink: /publication/optimizer_benchmarking
venue: 'International Conference on Machine Learning'
date: 2020-02-01
# paperurl: 'http://prabhuteja12.github.io/files/sivaprasad20a.pdf'
# citation: 'Sivaprasad, Prabhu Teja, Florian Mai, Thijs Vogels, Martin Jaggi, and Francois Fleuret. "Optimizer benchmarking needs to account for hyperparameter tuning." In International Conference on Machine Learning, pp. 9036-9045. PMLR, 2020.'
---

[Download paper here](../files/sivaprasad20a.pdf) and the [Supplementary material](../files/sivaprasad20a-supp.pdf)

[Code here](https://github.com/idiap/hypaobp) and [Back-end](https://github.com/idiap/DeepOBS/tree/tuning_protocol)

### A brief explanation

Imagine two optimizers $A$ and $B$, each with its own hyperparameters. Lets say both the optimizers result in the same test performance for a some set of hyperparameter configurations. However, $A$'s optimizer takes far more tuning effort (say by an automated hyperparameter search method like Random Search). Specifically, the best performing configuration can be found for $A$ after a budget of 50, and a budget of 5 for $B$. Given this scenario, we say that $A$ & $B$ are different in spite of the existence of their best performing configurations as $B$ is probably far easy to obtain /good-enough/ performance. We call this idea *tunability*. We find that this perspective of optimizer evaluation hasn't been done before, and is quite important to truly comparing optimizers.

The results of our experiments support the hypothesis that adaptive gradient methods are easier to tune than non-adaptive methods: In a setting with low budget for hyperparameter tuning, tuning only Adam optimizer's learning rate is likely to be a very good choice; it doesn't guarantee the best possible performance, but it is evidently the easiest to find well-performing hyperparameter configurations for. While SGD yields the best performance in some cases, its best configuration is tedious to find, and Adam often performs close to it. Given a famous work named ['The Marginal Value of Adaptive Gradient Methods in Machine Learning'](https://papers.nips.cc/paper/7003-the-marginal-value-of-adaptive-gradient-methods-in-machine-learning.pdf) who show that Adam generalizes a little worse than SGD, while ignoring the tunability, we state that the substantial value of the adaptive gradient methods, specifically Adam, is its amenability to hyperparameter search. We hope that this paper encourages other researchers to conduct future studies on the performance of optimizers from a more holistic perspective, where the cost of the hyperparameter search is included.

Go through the rest of the paper for our full argument!

```{bibtex}
@inproceedings{sivaprasad2020optimizer,
  title={Optimizer benchmarking needs to account for hyperparameter tuning},
  author={Sivaprasad, Prabhu Teja and Mai, Florian and Vogels, Thijs and Jaggi, Martin and Fleuret, Francois},
  booktitle={International Conference on Machine Learning},
  pages={9036--9045},
  year={2020},
  organization={PMLR}
}
```
