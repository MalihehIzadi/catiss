# CatIss

<strong>Good news!!! CatIss is the winner of the NLBSE'22 tool competition!</strong> &#x1F3C6; &#127881; &#x1F38A;


This repository contains the source code, notebooks, model, and datasets used 
for training <em>CatIss</em>, 
an intelligent tool for automatic categorization of issue reports 
based on the RoBERTa model.
I first deduplicated, cleaned and truncated 
the datasets provided for the NLBSE 2022 Tool Competition
(<a href="https://nlbse2022.github.io/">The First International Workshop 
    on Natural Language-based Software Engineering</a>) [1], 
then fine-tuned RoBERTa for four epochs on the cleaned training set. 
CatIss is able to achieve an <em>87.2% F1-score</em> (micro average) 
on the provided test set.


## Shared Model and Data

The saved model and cleaned datasets are shared publicly on Google Drive:

```
https://drive.google.com/drive/folders/1jgV4U41-2acctpc6jH5DWL3fF5V6bKF8?usp=sharing
```

## System Information

Experiments are conducted on a machine
equipped with Ubuntu 16.04, 64-bit as the operating system,
two GeForce RTX 2080 GPU cards,
AMD Ryzen Threadripper 1920X CPU, and 64G RAM.
Training lasts for four hours and 20 minutes.
Note that preprocessing the datasets 
significantly reduces the training cost, 
while maintaining the accuracy of predictions.


## Tool Paper Abstract

This paper describes CatIss, 
an automatic <b>Cat</b>egorizer of <b>Iss</b>ue reports
which is built upon the Transformer-based pre-trained RoBERTa model. 
CatIss classifies issue reports into three main categories of 
bug report, enhancement/feature request, and question.
First, the datasets provided for the NLBSE tool competition 
are cleaned and preprocessed.
Then, the pre-trained RoBERTa model 
is fine-tuned on the preprocessed dataset.
Evaluating CatIss on more than 
80 thousand issue reports from GitHub,
indicates that it performs very well 
surpassing the competition baseline, TiketTagger [2, 3],
TicketTagger, 
and achieving 87.2% F1-score (micro average).
Additionally, as CatIss is trained on a wide set of repositories,
it is a generic prediction model, 
hence applicable for any unseen software project 
or projects with little historical data.
Scripts for cleaning the datasets, 
training CatIss 
and evaluating the model 
are publicly available.
CatIss is based on our recent work 
published by Empirical Software Engineering Journal <b>(EMSE)</b>, 
which I will also be presenting 
at the 44th International Conference on Software Engineering <b>(ICSE'22)</b> Conference 
in the <i>Journal First Track</i> [4].


## References

[1] Kallis, R., Chaparro, O., Di Sorbo, A., and Panichella, S., 
NLBSE'22 Tool Competition, 
Proceedings of The 1st International Workshop on Natural Language-based Software Engineering (NLBSE'22)

[2] Kallis, R., Di Sorbo, A., Canfora, G., & Panichella, S. (2019, September). 
Ticket tagger: Machine learning driven issue classification. 
In 2019 IEEE International Conference on Software Maintenance and Evolution (ICSME) (pp. 406-409). IEEE.

[3] Kallis, R., Di Sorbo, A., Canfora, G., & Panichella, S. (2021). 
Predicting issue types on GitHub. Science of Computer Programming, 205, 102598.

[4] Izadi, M., Akbari, K., & Heydarnoori, A. (2022). 
<a href = "https://link.springer.com/article/10.1007/s10664-021-10085-3">
    Predicting the objective and priority of issue reports in software repositories.</a> 
Empirical Software Engineering, 27(2), 1-37.


## How to Cite

If you use CatIss in your work, please cite as following:

```
Izadi, M., CatIss: An Intelligent Tool for Categorizing Issues Reports using Transformers, In Proceedings of The 1st International Workshop on Natural
Language-based Software Engineering (NLBSE’22), page (to appear), 2022.
``` 
