--------------------------------------------------------------------------------------
### [**STAR**](https://ieeexplore.ieee.org/document/11063306)

- The implementation for "**STAR: A Unified Spatiotemporal Fusion Framework for Satellite Video Object Tracking**".
- IEEE Transactions on Geoscience and Remote Sensing, 2025.
<!--- IEEE Transactions on Geoscience and Remote Sensing, 2025.-->
--------------------------------------------------------------------------------------

:running:Keep updating:running::
- Trained model of [STAR](https://drive.google.com/drive/folders/1nIqG2FBt1fNbRThaO9s-fWoGV_O-DtJ7?hl=zh-cn) has been released.
- Pre-trained model of [STAR](https://drive.google.com/drive/folders/1xd7khcOqTOOtBykQIz2QxXidjKp1FvE6?hl=zh-cn) has been released.
- Training and testing codes of [STAR](https://github.com/YZCU/STAR/blob/main/training%20and%20testing%20codes%20of%20star.zip) have been released.
- Tracking result of [STAR](https://github.com/YZCU/STAR/blob/main/rect_result%20of%20star.zip) has been released.
--------------------------------------------------------------------------------------
| Benchmark | STAR (PR / SR / NPR)|
| ------------------------------ | ------------------- |
| [SatSOT](https://ieeexplore.ieee.org/document/9672083) |0.639 / 0.537 /|
| [SV248S](https://ieeexplore.ieee.org/document/9875020) |0.774 / 0.523 /|
| [OOTB](https://www.sciencedirect.com/science/article/pii/S0924271624000856) |0.846 / 0.678 / 0.826|

--------------------------------------------------------------------------------------
- Visual analysis, arranged from top to bottom: car_01 (SatSOT), car_61 (SatSOT), 03_000036 (SV248S), 04_000003 (SV248S), 05_000035 (SV248S), ship_10 (OOTB), and train_1 (OOTB).
![image](/fig/vis.jpg)
- Overlap curves and tracking samples of STAR in diverse scenarios. Red --> Our STAR. Blue --> Ground Truth.
![image](/fig/overlap_curve.jpg)
<!--
- Authors:
[Yuzeng Chen](https://yzcu.github.io/),
[Qiangqiang Yuan](http://qqyuan.users.sgg.whu.edu.cn/),
[Yuqi Tang](https://faculty.csu.edu.cn/yqtang/zh_CN/zdylm/66781/list/index.htm),
Xin Wang,
[Yi Xiao](https://github.com/XY-boy),
Jiang He,
Ziyang Lihe,
Xianyu Jin
--------------------------------------------------------------------------------------
-->
--------------------------------------------------------------------------------------
##  Install
```
git clone https://github.com/YZCU/STAR.git
```
--------------------------------------------------------------------------------------
## Environment
 > * CUDA 11.8
 > * Python 3.9.18
 > * PyTorch 2.0.0
 > * Torchvision 0.15.0
 > * numpy 1.25.0 
--------------------------------------------------------------------------------------
## Usage
- Training: Please download the satellite video training and testing sets: [SatSOT-train](https://ieeexplore.ieee.org/document/10756741),
  [SatSOT](https://ieeexplore.ieee.org/document/9672083),
  [SV248S](https://ieeexplore.ieee.org/document/9875020),
  [OOTB](https://www.sciencedirect.com/science/article/pii/S0924271624000856).

- Fast Training: Download the [pre-trained model](https://drive.google.com/drive/folders/1xd7khcOqTOOtBykQIz2QxXidjKp1FvE6?hl=zh-cn) of STAR. Put it into `<pretrained_models>`.
- Run `<tracking/train.py>` to train STAR.
- The well-trained STAR model is put into `<output/train/yzcu/yzcu-ep150-full-256/yzcu_ep0060.pth.tar>`.
- We have also released the well-trained [STAR](https://drive.google.com/drive/folders/1nIqG2FBt1fNbRThaO9s-fWoGV_O-DtJ7?hl=zh-cn) tracking models.
- Testing: Run `<tracking/test.py>` for testing, and results are saved in `<output/results/yzcu/yzcu-ep150-full-256>`.
- Evaluating: Please download the evaluation benchmark [Toolkit](http://cvlab.hanyang.ac.kr/tracker_benchmark/) and [vlfeat](http://www.vlfeat.org/index.html) for more accurate evaluation.
- Refer to the [Object Tracking Benchmark](https://ieeexplore.ieee.org/document/7001050) for detailed evaluations.
- Evaluation of the STAR tracker. Run `<tracker_benchmark_v1.0\perfPlot.m>`
--------------------------------------------------------------------------------------
<!--

## Citation
- If you find our work helpful in your research, kindly consider citing it. We appreciate your support！
```
@ARTICLE{11007172,
  author={Chen, Yuzeng and Yuan, Qiangqiang and Xie, Hong and Tang, Yuqi and Xiao, Yi and He, Jiang and Guan, Renxiang and Liu, Xinwang and Zhang, Liangpei},
  journal={IEEE Transactions on Image Processing}, 
  title={Hyperspectral Video Tracking with Spectral-Spatial Fusion and Memory Enhancement}, 
  year={2025},
  volume={},
  number={},
  pages={1-1},
  keywords={Feature extraction;Hyperspectral imaging;Photonic band gap;Foundation models;Visualization;Video tracking;Tracking;Training;Transformers;Imaging;Hyperspectral video tracking;Multi-modal video tracking;Parameter-efficient fine-tuning},
  doi={10.1109/TIP.2025.3569479}}

```
-->

## Contact
- If you have any questions or suggestions, feel free to contact me.  
- Email: yzchen1006@163.com

:heart:  :heart: We sincerely appreciate the insightful feedback provided by Editors and Reviewers. :heart:  :heart:

--------------------------------------------------------------------------------------
