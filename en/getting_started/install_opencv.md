# Install OpenCV

First need to install OpenCV when installing PHPOpenCV

## Method 1: Use docker (`*Recommended`)
For developers who are not familiar with OpenCV, installing OpenCV is cumbersome and can be used directly with the OpenCV docker image I provided.
It contains the `opencv_contrib` module (extended function module such as face recognition), which is only 300M in size. So it is recommended to install this method.

```bash
docker pull hihozhou/opencv
```


## Method 2: Compile and install OpenCV

This method is a traditional compilation and installation, although the steps are cumbersome, but can be more customized installation.

### Preparation before installation

``` bash
$ sudo apt-get install gcc-4.8 g++-4.8
$ sudo apt-get install build-essential
$ sudo apt-get install cmake git libgtk2.0-dev pkg-config libavcodec-dev libavformat-dev libswscale-dev
$ sudo apt-get install libtbb2 libtbb-dev libjpeg-dev libpng-dev libtiff-dev libjasper-dev libdc1394-22-dev
```

### Download the opencv_contrib module

This module is mainly used for extended functions such as face recognition.

``` bash
$ git clone https://github.com/opencv/opencv_contrib.git
$ cd opencv_contrib
$ cd ..
```

### Download opencv

``` bash
$ git clone https://github.com/opencv/opencv.git
$ cd opencv

```

### Compile and install opencv
```bash
$ mkdir build
$ cd build
$ cmake -D CMAKE_BUILD_TYPE=RELEASE -D CMAKE_INSTALL_PREFIX=/usr/local -D WITH_TBB=ON -D BUILD_NEW_PYTHON_SUPPORT=ON -D WITH_V4L=ON -D INSTALL_C_EXAMPLES=ON -D INSTALL_PYTHON_EXAMPLES=ON -D BUILD_EXAMPLES=ON -D WITH_QT=ON -D WITH_OPENGL=ON -D OPENCV_EXTRA_MODULES_PATH=../../opencv_contrib/modules ..
$ make -j6
$ sudo make install
$ sudo sh -c 'echo "/usr/local/lib" > /etc/ld.so.conf.d/opencv.conf'
$ sudo ldconfig
```

## Window system installation

pending upgrade

## Detection

After compiling and installing, you can use pkg-config to check whether the installation is successful.
```bash
$ pkg-config --libs opencv4
```