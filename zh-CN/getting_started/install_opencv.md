# 安装OpenCV

在安装PHPOpenCV首先需要安装OpenCV

## 方法一：使用docker(`*推荐`)
对于不熟悉OpenCV的开发者来说，安装OpenCV是比较麻烦，可以直接使用我提供的OpenCV docker镜像，
里面包含了`opencv_contrib`模块（人脸识别等扩展功能模块），仅300M大小。所以推荐该方法安装。

```bash
docker pull hihozhou/opencv
```


## 方法二：编译安装OpenCV

该方法属于传统的编译安装，虽然步骤繁琐，但可以更加自定义化安装。

### 安装前准备

``` bash
$ sudo apt-get install gcc-4.8 g++-4.8
$ sudo apt-get install build-essential
$ sudo apt-get install cmake git libgtk2.0-dev pkg-config libavcodec-dev libavformat-dev libswscale-dev
$ sudo apt-get install libtbb2 libtbb-dev libjpeg-dev libpng-dev libtiff-dev libjasper-dev libdc1394-22-dev
```

### 下载opencv_contrib模块

该模块主要用于人脸识别等扩展功能。

``` bash
$ git clone https://github.com/opencv/opencv_contrib.git
$ cd opencv_contrib
$ cd ..
```

### 下载opencv

``` bash
$ git clone https://github.com/opencv/opencv.git
$ cd opencv

```

### 编译安装opencv
```bash
$ mkdir build
$ cd build
$ cmake -D CMAKE_BUILD_TYPE=RELEASE -D CMAKE_INSTALL_PREFIX=/usr/local -D WITH_TBB=ON -D BUILD_NEW_PYTHON_SUPPORT=ON -D WITH_V4L=ON -D INSTALL_C_EXAMPLES=ON -D INSTALL_PYTHON_EXAMPLES=ON -D BUILD_EXAMPLES=ON -D WITH_QT=ON -D WITH_OPENGL=ON -D OPENCV_EXTRA_MODULES_PATH=../../opencv_contrib/modules ..
$ make -j6
$ sudo make install
$ sudo sh -c 'echo "/usr/local/lib" > /etc/ld.so.conf.d/opencv.conf'
$ sudo ldconfig
```

## window系统安装

待更新

## 检测

编译安装完后，可以使用pkg-config来检测是否安装成功
```bash
$ pkg-config --libs opencv4
```