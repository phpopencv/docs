# Install the PHPOpenCV extension

## Compile and install PHPOpenCV extension

> Note: The prerequisite for installing the PHPOpenCV extension is that OpenCV is already installed on your computer. If it is not installed, please refer to the previous chapter `Installing OpenCV`.


### Download and install the PHPOpenCV extension

```bash
$ git clone https://github.com/hihozhou/php-opencv.git
$ cd php-opencv
$ phpize
$ ./configure --with-php-config=/your/php-config --enable-debug
$ make && make install
```

### Configure php.ini

```
extension="opencv.so path"
```


## Window installation

pending upgrade...


