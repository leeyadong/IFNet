
# IFNet: Imaging and Fousing Network for Handheld SAR

## Code repository for the paper: IFNet: Deep Imaging and Focusing for Handheld SAR with Millimeter-wave Signals, IEEE TMC, 2024.

Authors: [Yadong Li](https://yadongli.com), [Dongheng Zhang](http://staff.ustc.edu.cn/~dongheng/), Ruixu Geng, Jincheng Wu, Yang Hu, [Qibin Sun](https://ustc-ip-lab.github.io/authors/qibinsun/), and [Yan Chen](https://ustc-ip-lab.github.io/authors/yanchen/)

Affiliation: [Intelligent Perception Lab](https://ustc-ip-lab.github.io/), University of Science and Technology of China. [Paper Link](https://arxiv.org/pdf/2405.02023)
  
<div align=center>
    <img src="https://github.com/leeyadong/IFNet/blob/f9cfb7666bbdcf027150f05866e8c71b869427aa/figures/method_tmc.jpg" alt="method" width="900" />
</div>


## Introduction

- In this paper, we present IFNet, a novel deep unfolding network that combines the strengths of signal processing models and deep neural networks
to achieve robust imaging and focusing for handheld mmWave systems. 

- This repository includes code for training and testing IFNet.
  
- This repository provides the collected dataset for training the network.

<div align=center>
    <img src="https://github.com/leeyadong/IFNet/blob/23c1d7d95c5d7d9f073f19b08d7bae88ddc6d4af/figures/overview_ifnet_tmc.jpg" alt="method" width="400" />
</div>


## How to Access the Code

The [USTC IP Lab](https://ustc-ip-lab.github.io/) has particular protocols for releasing the code and dataset. To access the code, please sign the [code agreement](IPLabCodeAgreementIFNet.pdf), scan and send it to yadongli@uw.edu or yadongli@mail.ustc.edu.cn. A notification email that includes the code link will be sent within three days.

## Run Demo
### Requirements
```
pip3 install torch --index-url https://download.pytorch.org/whl/cu124
```
```
pip install cython
```
```
pip install torchbox numpy scipy dominate visdom
```
### Prepare the dataset
- Download the raw ADC data and handheld trajectory from the link given in the replied email.
- Put the raw ADC data in ./data/adc_data and the handheld trajectory in ./data/handheld_trajectory
- Run python prepare_dataset.py
### Train and test
Set the dataset path in ./options/base_options.py, then run
```
python train.py
```
```
python test.py
```

## Acknowledgments
Special thanks to the incredible [DelburGAN](https://github.com/KupynOrest/DeblurGAN) repository, which was the foundation for the training framework in this repository.

## Citing
If you find this code useful for your research, please consider citing the following paper:
```
@ARTICLE{ifnettmc,
  author={Li, Yadong and Zhang, Dongheng and Geng, Ruixu and Wu, Jincheng and Hu, Yang and Sun, Qibin and Chen, Yan},
  journal={IEEE Transactions on Mobile Computing}, 
  title={IFNet: Deep Imaging and Focusing for Handheld SAR With Millimeter-Wave Signals}, 
  year={2024},
  volume={},
  number={},
  pages={1-16},
  doi={10.1109/TMC.2024.3489641}}
}
```
```
@INPROCEEDINGS{ifneticassp,
  author={Li, Yadong and Zhang, Dongheng and Geng, Ruixu and Wu, Jincheng and Hu, Yang and Sun, Qibin and Chen, Yan},
  booktitle={ICASSP 2024 - 2024 IEEE International Conference on Acoustics, Speech and Signal Processing (ICASSP)}, 
  title={IFNet: Imaging and Focusing Network for handheld mmWave Devices}, 
  year={2024},
  volume={},
  number={},
  pages={2415-2419},
  doi={10.1109/ICASSP48485.2024.10447461}}

```
