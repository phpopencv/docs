# 图像的基本操作

## 目标
学会：
- 访问像素值并修改它们
- 访问图像属性
- 设置感兴趣区域（ROI）
- 拆分和合并图像

## 访问和修改像素值

我们先加载彩色图像：

```php
use function CV\{
    imread
};

$img = imread('messi5.jpg');
```