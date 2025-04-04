# Norm-Based Outlier Filtering and Consensus Aggregation for Robust Federated Learning

---

## Overview

Federated Learning (FL) is vulnerable to persistent backdoor attacks that remain effective even after malicious clients are removed. To address this, we propose NOFCA, a defense framework that filters norm-based outliers and enforces consensus-aligned aggregation. This dual-stage method effectively disrupts stealthy attacks such as IBA, while preserving clean model performance under diverse federated scenarios.

Our experiment pipeline is based on the official IBA implementation:  
[IBA: Towards Irreversible Backdoor Attacks in Federated Learning](https://github.com/sail-research/iba)  
which itself builds on the setup from [Attack of the Tails: Yes, You Really Can Backdoor Federated Learning](https://github.com/ksreenivasan/OOD_Federated_Learning).


---

## 1. Setup

1. Clone this repository and set up the Python environment:
```bash
git clone https://github.com/UnggiYeo/NOFCA.git
cd NOFCA
make install
```
2. MNIST and CIFAR-10 will be automatically download

## 2. Running the Experiments
To reproduce the main experiments from the paper:
```bash
./exps/mnist_freq.sh
./exps/cifar10_freq.sh 
```
These scripts run the IBA attack under various settings with and without NOFCA defense.

You can modify the following parameters to reproduce different scenarios:

- --dataset: Specify the dataset.
- --model: Select the model.
- --defense_method: Choose the defense method.
- --attack_method: Select the attack method.
- --attack_freq: Set the attack frequency.
- --attack_case: Specify the attack case.
- --model_replacement: Enable or disable model replacement.

Please refer to the paper for detailed results and additional configurations.

Please note that I have made some assumptions and corrections based on the given context. Make sure to review and adjust the changes if necessary.

Please cite the paper, as below, when using this repository:
```
@inproceedings{
    nguyen2023iba,
    title={{IBA}: Towards Irreversible Backdoor Attacks in Federated Learning},
    author={Dung Thuy Nguyen and Tuan Minh Nguyen and Anh Tuan Tran and Khoa D Doan and KOK-SENG WONG},
    booktitle={Thirty-seventh Conference on Neural Information Processing Systems},
    year={2023},
    url={https://openreview.net/forum?id=cemEOP8YoC}
}
```

