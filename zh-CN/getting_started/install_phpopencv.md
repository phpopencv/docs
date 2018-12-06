# 安装PHPOpenCV扩展

## 编译安装PHPOpenCV扩展

> 注意：安装PHPOpenCV扩展的前提是你电脑上已经安装了OpenCV，如果没有安装可以参考上一章`安装OpenCV`


### 下载并安装PHPOpenCV扩展库

```bash
$ git clone https://github.com/hihozhou/php-opencv.git
$ cd php-opencv
$ phpize
$ ./configure --with-php-config=/your/php-config --enable-debug
$ make && make install
```

### 配置php.ini

```
extension="opencv.so path"
```


## window安装

待更新


