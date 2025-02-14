---
title: Regulations
background: /assets/theme/images/bckg.png
permalink: /regulations/
---

&nbsp; 
### **<span style="color:#2B547E">Rules</span>**
\
Participants are subject to the following rules:

- Participants must register via the [registration form]({{ '/registration/' | relative_url }}).

- The participation of groups is encouraged. Each group/participant can submit only as an individual or as a team. It is not possible to participate both individually and as a team.

- After registration, participants will receive an email containing detailed steps and useful resources:
    - Register on the CodaBench platform and enrol on the [**CodaBench competition page**](https://www.codabench.org/competitions/5512).
    - Follow the participation and submission [guidelines](https://www.codabench.org/competitions/5512/#/pages-tab), you will find all the instructions and resources needed to submit your models.

- The intellectual property (IP) is not transferred to the challenge organizers, i.e., the participants remain the owners of the code shared (when the code is made publicly available, an appropriate license should be added).


&nbsp;  

### **<span style="color:#2B547E">Evaluation Criteria</span>**
\
Researchers in ML typically report performance in terms of sensitivity and specificity. Seizure detection is usually a problem with a high imbalance between classes, since seizure events are rare within the datasets. In these cases, False Alarm (FA) rate is commonly used instead of specificity. FA rate is simply the number of false positives divided by the total duration of the recordings and normalized to one hour (FA/h).

In the current use case scenario, in which we use the automatic seizure detection for automated seizure diaries, sensitivity is important, and none of the seizure events should be missed. Hence, the sensitivity will be measured on an event basis which does not consider individual windows. To compute sensitivity, the any-overlap method (OVLP) [1] will be employed. True Positives (TPs) are counted when the hypothesis has any overlap with the corresponding event in the ground truth annotation. False Positives (FPs) or FAs correspond to situations in which a hypothesis does not overlap with the corresponding event in the reference. OVLP is a more permissive metric and tends to produce higher sensitivities and lower FAs rates. The metric ignores the duration of the term in the provided annotation; hence, longer events will provide better scores. 

Accounting for the under-reporting of FAs by the OVLP method, we will combine two methods in our scoring formula. Sensitivity will be computed based on OVLP, as mentioned, and FAs rate will be based on epoch-based scoring. EPOCH [1] treats the reference and hypothesis as time series. These signals are sampled at a fixed window length (epoch duration). The corresponding label in the reference is compared to the hypothesis for each epoch. Any possible substitutions, deletions, or insertion errors are tabulated with an equal weight of 1.0 for each type of error. A weighting factor of 0.4 will be used in order to balance sensitivity and FA rate and provide the scoring points.
\
![Scoring]({{ '/assets/theme/images/score.png' | relative_url }})



&nbsp;  

#### References

[1] Ziyabari, S., et al., "Objective evaluation metrics for automatic classification of EEG events", 2017. arXiv preprint arXiv:1712.10107.
