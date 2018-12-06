# 结构

## CV命名空间

首先PHPOpenCV扩展所有的类、方法以及常量都在CV命名空间下，如：

``` php
use CV\Mat;
use const CV\{CV_8UC1};
use function CV\{imread, imwrite};

//doing something...

```


## 模块

虽然所有的类、方法和常量都在CV命名空间下，但是如果以功能划分，可以以下模块：

- `core`    —— 核心功能模块
- `imgproc` —— Image和Processing这两个单词的缩写组合。图像处理模块
- `calib3d` —— 其实就是就是Calibration（校准）加3D这两个词的组合缩写。这个模块主要是相机校准和三维重建相关的内容。基本的多视角几何算法，单个立体摄像头标定，物体姿态估计，立体相似性算法，3D信息的重建等等
- `contrib` —— 也就是Contributed/Experimental Stuf的缩写， 该模块包含有新型人脸识别，立体匹配，人工视网膜模型等技术
- `features2d` —— 也就是Features2D， 2D功能框架
- `flann` —— Fast Library for Approximate Nearest Neighbors，高维的近似近邻快速搜索算法库
- `gpu` —— 运用GPU加速的计算机视觉模块
- `highgui` —— 也就是high gui，高层GUI图形用户界面，包含媒体的I / O输入输出，视频捕捉、图像和视频的编码解码、图形交互界面的接口等内容
- `legacy` —— 一些已经废弃的代码库，保留下来作为向下兼容
- `ml` —— Machine Learning，机器学习模块， 基本上是统计模型和分类算法
- `nonfree` —— 一些具有专利的算法模块 ，包含特征检测和GPU相关的内容。最好不要商用
- `objdetect` —— 目标检测模块，包含Cascade Classification（级联分类）和Latent SVM这两个部分
- `ocl` —— 即OpenCL-accelerated Computer Vision，运用OpenCL加速的计算机视觉组件模块
- `photo` —— 也就是Computational Photography，包含图像修复和图像去噪两部分
- `stitching` —— images stitching，图像拼接模块
- `superres` —— SuperResolution，超分辨率技术的相关功能模块
- `video` —— 视频分析组件，该模块包括运动估计，背景分离，对象跟踪等视频处理相关内容。
- `Videostab` —— Video stabilization，视频稳定相关的组件，官方文档中没有多作介绍，不管它了。