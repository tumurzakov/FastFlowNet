# FastFlowNet: A Lightweight Network for Fast Optical Flow Estimation
The official PyTorch implementation of [FastFlowNet] (ICRA 2021).

Authors: [Lingtong Kong](https://dblp.org/pid/261/8152.html), [Chunhua Shen](https://cshen.github.io/), [Jie Yang](http://www.pami.sjtu.edu.cn/jieyang)

Dense optical flow estimation plays a key role in many robotic vision tasks. It has been predicted with satisfying accuracy than traditional methods with advent of deep learning. However, current networks often occupy large number of parameters and require heavy computation costs. These drawbacks have hindered applications on power- or memory-constrained mobile devices. To deal with these challenges, in this paper, we dive into designing efficient structure for fast and accurate optical flow prediction. Our proposed FastFlowNet works in the well-known coarse-to-fine manner with following innovations. First, a new head enhanced pooling pyramid (HEPP) feature extractor is employed to intensify high-resolution pyramid feature while reducing parameters. Second, we introduce a novel center dense dilated correlation (CDDC) layer for constructing compact cost volume that can keep large search radius with reduced computation burden. Third, an efficient shuffle block decoder (SBD) is implanted into each pyramid level to acclerate flow estimation with marginal drops in accuracy. Experiments on both synthetic Sintel and real-world KITTI datasets demonstrate the effectiveness of proposed approaches, which consumes only 1/10 computation of comparable networks to get 90\% of their performance. In particular, FastFlowNet only contains 1.37 M parameters and runs at 90 or 5.7 fps with one desktop NVIDIA GTX 1080 Ti or embedded Jetson TX2 GPU on Sintel resolution images.

![](./data/tx2_demo.gif)

