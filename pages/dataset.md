---
title: Dataset
background: /assets/theme/images/bckg.png
permalink: /dataset/
---

&nbsp; 
### **<span style="color:#2B547E">SeizeIT2 Dataset</span>**

The SeizeIT2 project (clinicaltrials.gov: NCT04284072) is an international multicenter dataset with more than 350 patients suffering from epilepsy and recorded both in home and hospital environments (the first ever phase-4 clinical trial for a wearable for in-home monitoring for seizure detection). The data are acquired with the SD device and the current study is part of a larger multicenter trial with focus on clinical validation of the SD in people with typical absence, focal impaired awareness, and generalized tonic–clonic seizures. SeizeIT2 unites public and private stakeholders to address an unmet patient need. This is a continuation of [SeizeIT1](https://rdr.kuleuven.be/dataset.xhtml?persistentId=doi:10.48804/P5Q0OJ) ICON project, led by UCB, with partners from Un. de Navarra, Karolinska Institute, KU Leuven, RWTH Aachen, Universitäts klinikum Aachen, Centro Hospitalar e Universitário de Coimbra, Oxford University Hospitals NHS Foundation Trust and Stockholms Läns Landsting. The data collection started on January 10, 2020, and ended on June 30, 2022. The study was approved by the UZ Leuven ethics committee (approval ID: S63631, ClinicalTrials.gov, NCT04284072), anonymization and sharing of the data was also approved by the same committee (S67350 - amendment 1).
Patients underwent video-EEG monitoring using the standardized 25-electrode array of the International Federation of Clinical Neurophysiology. Two additional Ag/AgCl cup electrodes were attached on the mastoid bone for concomitant recording with the SD to measure behind-the-ear EEG (bte-EEG), the same electrode positions as the behind-the-ear EEG in SeizeIT1. The closest corresponding electrodes on 25-channel EEG were T7 and T8 for the top electrode and P9 and P10 for the lower electrode. The SD was attached on the upper back using a patch, and two bipolar channels were created by connecting the ipsilateral top and lower electrode. An additional SD sensor was placed on the left chest of patients with two electrodes measuring Electrocardiography data (ECG) and two electrodes on the left deltoid muscle measuring Electromypgraphy (EMG) data. Both SD modules contained accelerometers and gyroscopes, allowing movement to be monitored.

The **<span style="color:#2B547E">SeizeIT2 public dataset</span>** is a subset of the full project, where only patients with focal epilepsy were included. The dataset comprises 125 patients (51 female, 41%) from 5 different European EMUs: University Hospital Leuven (Belgium), Freiburg University Medical Center (Germany), RWTH University of Aachen (Germany), Karolinska University Hospital (Sweden) and Coimbra University Hospital (Portugal). The University Hospital Leuven was the only center that enrolled pediatric patients. The dataset includes only data from patients with focal epilepsy who experienced one or more seizure episodes during the monitoring period.

The complete dataset contains around 11 640 hours of wearable data. Four different modalities were recorded for most participants: bte-EEG, ECG, EMG and movement data. All participants' data within the dataset contain wearable bte-EEG. In 3% of the dataset, ECG, EMG and movement data were not included due to technical failures or errors in the setup. In total, 886 focal seizures were recorded with the wearable device. The mean duration of the recorded seizures was 58 seconds, ranging between 3 seconds and 16 minutes. The majority of the seizures were focal aware (FA) and focal impaired awareness (FIA), with 317 and 393 occurrences, respectively. From the remaining seizures, 55 were focal-to-bilateral tonic clinic (FBTC), 12 were focal with unclear awareness status, 2 were subclinical focal seizures and 93 had unknown or unreported onset. There was a predominance of seizures with onset on the left hemisphere (44%). In 12% of the seizures, the onset was located in the right hemisphere, 1% had a bilateral onset and in 43% of the seizures the onset was unclear. Regarding localization, the seizure onsets were distributed over the central, frontal, temporal, occipital, parietal and insula lobes, with a predominance of temporal lobe seizures (30%). Several seizures recorded could not be paired with a clear onset lobe (26%).

&nbsp;

#### Read the [**paper**](https://arxiv.org/abs/2502.01224) for more detailed information about the dataset.

&nbsp;

#### Download the dataset from the [OpenNeuro repository](https://openneuro.org/datasets/ds005873).

&nbsp;

Here’s the HTML content converted into Markdown:

---

**Acknowledgement:**  
Any published work using these resources (dataset and code) should use proper citation of the dataset paper and repositories:

- Bhagubai, M., Chatzichristos, C., Swinnen, L., Macea, J., Zhang, J., Lagae, L., Jansen, K., Schulze-Bonhage, A., Sales, F., Mahler, B., Weber, Y., Paesschen, W. V., & Vos, M. D. (2025). *SeizeIT2: Wearable Dataset Of Patients With Focal Epilepsy*. [https://doi.org/https://doi.org/10.48550/arXiv.2502.01224](https://doi.org/https://doi.org/10.48550/arXiv.2502.01224)

```
@misc{seizeit2_dataset_paper,
title={SeizeIT2: Wearable Dataset Of Patients With Focal Epilepsy}, 
author={Miguel Bhagubai and Christos Chatzichristos and Lauren Swinnen and Jaiver Macea and Jingwei Zhang and Lieven Lagae and Katrien Jansen and Andreas Schulze-Bonhage and Francisco Sales and Benno Mahler and Yvonne Weber and Wim Van Paesschen and Maarten De Vos},
year={2025},
eprint={2502.01224},
archivePrefix={arXiv},
primaryClass={eess.SP},
url={https://arxiv.org/abs/2502.01224},
doi={https://doi.org/10.48550/arXiv.2502.01224},
}
```

- Bhagubai, M. et al. *SeizeIT2*, doi: [10.18112/openneuro.ds005873.v1.0.1](https://doi.org/10.18112/openneuro.ds005873.v1.0.1)

```
@dataset{seizeit2_repository,
author = {Miguel Bhagubai and Christos Chatzichristos and Lauren Swinnen and Jaiver Macea and Jingwei Zhang and Lieven Lagae and Katrien Jansen and Andreas Schulze-Bonhage and Francisco Sales and Benno Mahler and Yvonne Weber and Wim Van Paesschen and Maarten De Vos },
title = {"SeizeIT2"},
year = {2025},
doi = {doi:10.18112/openneuro.ds005873.v1.0.1},
publisher = {OpenNeuro},
}
```

---

This markdown will keep the list and formatting with code blocks for the citations.
\
![seizeit2]({{ '/assets/theme/images/sz2_setup.png' | relative_url }}){: .rounded .float-end}

\
In the context of this challenge, the data was separated in a fixed training, validation and test sets. The training and validation sets are public and will be provided to participants, the test set is privately kept and used for the final evaluation.


