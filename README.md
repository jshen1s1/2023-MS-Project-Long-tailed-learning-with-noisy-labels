# 2023-MS-Project-Long-Tailed-Learning-with-Noisy-Labels

This repository contains the code for Jinghao Shen's MS Project

The framework comprises all the basic stages: feature extraction, training, inference and evaluation. After loading the CIFAR10/CIFAR100 dataset, a resnet baseline is trained and evaluated. The code also allows to test four noise-robust loss functions. 

## 1. Type of Long-tailed Learning

| Symbol | `Sampling`  |          `CSL`          |       `LA`       |       `TL`        |       `Aug`       |
| :----- | :---------: | :---------------------: | :--------------: | :---------------: | :---------------: |
| Type   | Re-sampling | Cost-sensitive Learning | Logit Adjustment | Transfer Learning | Data Augmentation |

| Symbol |          `RL`           |       `CD`        |        `DT`        |    `Ensemble`     |   `other`   |
| :----- | :---------------------: | :---------------: | :----------------: | :---------------: | :---------: |
| Type   | Representation Learning | Classifier Design | Decoupled Training | Ensemble Learning | Other Types |

## 2. Top-tier Conference Papers

### Noisy labels

| Title                                                        |  Venue  | Year |       Type       |                             Code                             |
| :----------------------------------------------------------- | :-----: | :--: | :--------------: | :----------------------------------------------------------: |
| [Learning with Instance-Dependent Label Noise: A Sample Sieve Approach](https://openreview.net/pdf?id=2VXyy9mIyU3) | ICLR | 2021 |  |    [Official](https://github.com/haochenglouis/cores)     |
| [Generalized Cross Entropy Loss for Training Deep Neural Networks with Noisy Labels](https://arxiv.org/pdf/1805.07836.pdf) | NeurIPS  | 2018 |         |    [Unofficial](https://github.com/edufonseca/icassp19/blob/master/losses.py)    |
| [L_DMI: A Novel Information-theoretic Loss Function for Training Deep Nets Robust to Label Noise](https://arxiv.org/pdf/1909.03388.pdf) |  NeurIPS   | 2019 |             |      [Official](https://github.com/Newbeeer/L_DMI)      |
| [Early-Learning Regularization Prevents Memorization of Noisy Labels](https://arxiv.org/pdf/2007.00151.pdf) |  NeurIPS   | 2020 |        |         [Official](https://github.com/shengliu66/ELR)          |
| [Dual T: Reducing Estimation Error for Transition Matrix in Label-noise Learning](https://arxiv.org/pdf/2006.07805.pdf) |  NeurIPS   | 2020 |         |    [Official](https://github.com/a5507203/dual-t-reducing-estimation-error-for-transition-matrix-in-label-noise-learning)    |
| [DualGraph: A graph-based method for reasoning about label noise](https://openaccess.thecvf.com/content/CVPR2021/papers/Zhang_DualGraph_A_Graph-Based_Method_for_Reasoning_About_Label_Noise_CVPR_2021_paper.pdf) |  CVPR   | 2021 |         |            |
| [DivideMix: Learning with Noisy Labels as Semi-supervised Learning](https://arxiv.org/pdf/2002.07394.pdf) |  ICLR   | 2020 |    |        [Official](https://github.com/LiJunnan1992/DivideMix)         |
| [How does Disagreement Help Generalization against Label Corruption?](https://arxiv.org/pdf/1901.04215.pdf) |  ICML   | 2019 |              | [Official](https://github.com/bhanML/coteaching_plus) |
| [Co-teaching: Robust Training of Deep Neural Networks with Extremely Noisy Labels](https://arxiv.org/pdf/1804.06872.pdf) |  NeurIPS   | 2018 |           |          [Official](https://github.com/bhanML/Co-teaching)           |
| [Peer Loss Functions: Learning from Noisy Labels without Knowing Noise Rates](https://arxiv.org/pdf/1910.03231.pdf) |  ICML   | 2020 |           |          [Unofficial](https://github.com/weijiaheng/Multi-class-Peer-Loss-functions)           |

### Long-tailed Learning

| Title                                                        |  Venue  | Year |       Type       |                             Code                             |
| :----------------------------------------------------------- | :-----: | :--: | :--------------: | :----------------------------------------------------------: |
| [Escaping Saddle Points for Effective Generalization on Class-Imbalanced Data](https://arxiv.org/pdf/2212.13827.pdf) |  NeurIPS   | 2022 |       | [Official](https://github.com/val-iisc/Saddle-LongTail) |
| [Label-Imbalanced and Group-Sensitive Classification under Overparameterization](https://openreview.net/pdf?id=UZm2IQhgIyB) | NeurIPS | 2021 |             `LA`             |      [Official](https://github.com/orparask/VS-Loss)      |
| [Balanced Knowledge Distillation for Long-tailed Learning](https://arxiv.org/pdf/2203.09081.pdf) | ArXiv | 2021 |        |       [Official](https://github.com/EricZsy/BalancedKnowledgeDistillation)         |
| [FASA: Feature augmentation and sampling adaptation for long-tailed instance segmentation](https://arxiv.org/pdf/2102.12867.pdf) |  ICCV   | 2021 |       `Sampling`,`CSL`       |     [Official](https://github.com/yuhangzang/FASA)      |
| [Disentangling label distribution for long-tailed visual recognition](https://openaccess.thecvf.com/content/CVPR2021/papers/Hong_Disentangling_Label_Distribution_for_Long-Tailed_Visual_Recognition_CVPR_2021_paper.pdf) |  CVPR   | 2021 |    `CSL`,`LA`    |       [Official](https://github.com/hyperconnect/LADE)       |
| [Influence-Balanced Loss for Imbalanced Visual Classification](https://arxiv.org/pdf/2110.02444.pdf) |  ICCV   | 2021 |            `CSL`             |        [Official](https://github.com/pseulki/IB-Loss)        |
| [Long-tail learning via logit adjustment](https://openreview.net/pdf?id=37nvvqkCo5) |  ICLR   | 2021 |             `LA`             | [Official](https://github.com/google-research/google-research/tree/master/logit_adjustment) |
| [Adjusting Decision Boundary for Class Imbalanced Learning](https://arxiv.org/pdf/1912.01857.pdf) | ArXiv | 2020 |  |    [Official](https://github.com/feidfoe/AdjustBnd4Imbalance)     |
| [To Balance or Not to Balance: A Simple-yet-Effective Approach for Learning with Long-Tailed Distributions](https://arxiv.org/pdf/1912.04486.pdf) |  CVPR   | 2020 |             |            |
| [Decoupling representation and classifier for long-tailed recognition](https://openreview.net/pdf?id=r1gRTCVFvB) |  ICLR   | 2020 | `Sampling`,`CSL`,`RL`,`CD`,`DT` | [Official](https://github.com/facebookresearch/classifier-balancing) |
| [Deep representation learning on long-tailed data: A learnable embedding augmentation perspective](https://openaccess.thecvf.com/content_CVPR_2020/papers/Liu_Deep_Representation_Learning_on_Long-Tailed_Data_A_Learnable_Embedding_Augmentation_CVPR_2020_paper.pdf) |  CVPR   | 2020 |         `TL`,`Aug`,`RL`         |                           |
| [Learning imbalanced datasets with label-distribution-aware margin loss](https://proceedings.neurips.cc/paper/2019/file/621461af90cadfdaf0e8d4cc25129f91-Paper.pdf) | NeurIPS | 2019 |   `CSL`    |        [Official](https://github.com/kaidic/LDAM-DRW)        |
| [Focal loss for dense object detection](https://openaccess.thecvf.com/content_ICCV_2017/papers/Lin_Focal_Loss_for_ICCV_2017_paper.pdf) |  ICCV   | 2017 | `CSL` |      |

### Long-Tailed Learning with Noisy Labels

| Title                                                        |  Venue  | Year |       Type       |                             Code                             |
| :----------------------------------------------------------- | :-----: | :--: | :--------------: | :----------------------------------------------------------: |
| [Identifying Hard Noise in Long-Tailed Sample Distribution](https://arxiv.org/pdf/2207.13378.pdf) |  ECCV   | 2022 |        |         [Official](https://github.com/yxymessi/H2E-Framework)          |
| [Combating Noisy Labels in Long-Tailed Image Classification](https://arxiv.org/pdf/2209.00273.pdf) |  ICLR   | 2022 |         |                                                              |
| [Learning from Long-Tailed Noisy Data with Sample Selection and Balanced Loss](https://arxiv.org/pdf/2211.10906.pdf) |  ArXiv   | 2022 |         |            |
| [Prototypical Classifier for Robust Class-Imbalanced Learning](https://arxiv.org/pdf/2110.11553.pdf) | ArXiv | 2021 |  |    [Official](https://github.com/Stomach-ache/PCL)     |
| [Robust Long-Tailed Learning Under Label Noise](https://arxiv.org/pdf/2108.11569.pdf) |  ArXiv   | 2021 |             |      [Unofficial](https://github.com/Stomach-ache/RoLT)      |
| [Learning From Long-Tailed Data With Noisy Labels](https://arxiv.org/pdf/2108.11096.pdf) |  ArXiv    | 2021 |   |                 |

### Benchmark Datasets

| Title                                                        |  Venue  | Year |       Type       |                             Code                             |
| :----------------------------------------------------------- | :-----: | :--: | :--------------: | :----------------------------------------------------------: |
| [A Benchmark of Long-tailed Instance Segmentation with Noisy Labels (Short Version)](https://arxiv.org/pdf/2211.13435.pdf) | ArXiv | 2022 |  |    [Official](https://github.com/GuanlinLee/Noisy-LVIS)     |

## 3. Our codebase
### Dependencies
This framework is tested on Ubuntu 20.04.5. To duplicate the environment:

`Under construction`
<!---`conda create --name <envname> --file requirements.txt`--->

### Usage
#### (0) Download the dataset:

Download CIFAR through the <a href="https://www.cs.toronto.edu/~kriz/cifar.html" target="_blank">dataset companion site</a>, unzip it and locate it in a given directory.

#### (1) Adjust parameters:

The goal is to define the parameters of the experiment. The most important parameters are: 
   
`noise_type`: type of noise 
`lt_type`: type of long-tailed distribution
`loss`: defines the loss function. To be decided among:
`dual_t`: apply dual T estimator or not

  - `cross_entropy`: cross entropy loss
  - `focal_loss`: 
  - `logits_adjustment`: 
  - `cores`: 
  - `gce`: 
  - `cb_ce`: 
  - `cb_focal`: 
  - `cores_no_select`: 
  - `cores_logits_adjustment`: 
  - `erl`:
  - `coteaching`: 
  - `coteaching_plus`: 
  - `cls`: 

The rest of the parameters should be rather intuitive.

#### (2) Execute the code by:
* CE:
  ```
  cd ./LT 
  Training: python main.py --dataset cifar100 --loss_type CE --train_rule None --lt_type exp --lt_rate 0.02 --noise_rate 0.3 --noise_type symmetric --epochs 200 --num_classes 100 --gpu 0

* CB_CE:
  ```
  cd ./LT 
  Training: python main.py --dataset cifar100 --loss_type CE --train_rule Reweight --lt_type exp --lt_rate 0.02 --noise_rate 0.3 --noise_type symmetric --epochs 200 --num_classes 100 --gpu 0

* Focal:
  ```
  cd ./LT 
  Training: python main.py --dataset cifar100 --loss_type Focal --train_rule None --lt_type exp --lt_rate 0.02 --noise_rate 0.3 --noise_type symmetric --epochs 200 --num_classes 100 --gpu 0

* LADE:
  ```
  cd ./LT 
  Training: python main.py --dataset cifar100 --loss_type LADE --train_rule None --lt_type exp --lt_rate 0.02 --noise_rate 0.3 --noise_type symmetric --epochs 200 --num_classes 100 --gpu 0

* LDAM:
  ```
  cd ./LT 
  Training: python main.py --dataset cifar100 --loss_type LDAM --train_rule DRW --lt_type exp --lt_rate 0.02 --noise_rate 0.3 --noise_type symmetric --epochs 200 --num_classes 100 --gpu 0

* IB:
  ```
  cd ./LT 
  Training: python main.py --dataset cifar100 --loss_type IB --train_rule IBReweight --lt_type exp --lt_rate 0.02 --noise_rate 0.3 --noise_type symmetric --epochs 200 --num_classes 100 --gpu 0

* IB_Focal:
  ```
  cd ./LT 
  Training: python main.py --dataset cifar100 --loss_type IBFocal --train_rule IBReweight --lt_type exp --lt_rate 0.02 --noise_rate 0.3 --noise_type symmetric --epochs 200 --num_classes 100 --gpu 0

* BKD:
  ```
  cd ./LT 
  Stage 1: python main.py --dataset cifar100 --loss_type BKD --train_rule None --lt_type exp --lt_rate 0.02 --noise_rate 0.3 --noise_type symmetric --epochs 200 --num_classes 100 --gpu 0
  Stage 2:

* VS:
  ```
  cd ./LT 
  Training: python main.py --dataset cifar100 --loss_type VS --train_rule None --lt_type exp --lt_rate 0.02 --noise_rate 0.3 --noise_type symmetric --epochs 200 --num_classes 100 --gpu 0

#### (3) See results:

You can check the `results/*.txt`. Results are shown in a table.

## 4. Survey References：
 
## 5. Contact

You are welcome to contact me privately should you have any question/suggestion or if you have any problems running the code at jshen30@ucsc.edu.