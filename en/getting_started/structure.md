# Structure

## CV namespace

First of all, PHPOpenCV extends all classes, methods, and constants in the CV namespace, e.g:

``` php
use CV\Mat;
use const CV\{CV_8UC1};
use function CV\{imread, imwrite};

//doing something...

```


## Module

Although all classes, methods, and constants are in the CV namespace, if divided by function, the following modules are available:

- `core` —— core function module
- `imgproc` —— an abbreviated combination of the two words Image and Processing. Image processing module
- `calib3d` —— In fact, it is the combination abbreviation of the two words Calibration and 3D. This module is mainly related to camera calibration and 3D reconstruction. Basic multi-view geometry algorithm, single stereo camera calibration, object pose estimation, stereo similarity algorithm, 3D information reconstruction, etc.
- `contrib` —— short for Contributed/Experimental Stuf, which includes new face recognition, stereo matching, artificial retina models, etc.
- `features2d` —— that is, Features2D, 2D functional framework
- `flann` —— Fast Library for Approximate Nearest Neighbors, high-dimensional approximate neighbor fast search algorithm library
- `gpu` —— GPU-accelerated computer vision module
- `highgui` —— high gui, high-level GUI graphical user interface, including media I / O input and output, video capture, image and video encoding and decoding, graphical interface interface, etc.
- `legacy` —— some deprecated codebases, reserved for backward compatibility
- `ml` —— Machine Learning, machine learning module, basically statistical model and classification algorithm
- `nonfree` —— some patented algorithm modules that include feature detection and GPU-related content. Best not to be commercial
- `objdetect` —— the target detection module, which includes the Cascade Classification and Latent SVM
- `ocl` —— OpenCL-accelerated Computer Vision, computer vision component module accelerated with OpenCL
- `photo` —— that is, Computational Photography, which includes image restoration and image denoising
- `stitching` —— images stitching, image stitching module
- `superres` —— SuperResolution, related function modules for super-resolution technology
- `video` —— a video analysis component that includes video processing related content such as motion estimation, background separation, and object tracking.
- `Videostab` —— Video stabilization, video stabilization related components, no more in the official documentation, no matter it.