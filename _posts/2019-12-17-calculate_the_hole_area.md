---
title: 识别图像中空洞，并计算面积
tags:
- matlab
- image identification
- calculate hole area
desc: calculate the hole area in the image via matlab
layout: post
---

受人委托需要帮着识别图像中空洞，并计算空洞面积。编程我也是个半吊子，感谢伟大的互联网与背后乐于分享的人，最后勉强搞定。

主要用到的函数有：

1. imcomplement(image) 因为原始图像只有孔洞边缘是黑色的，其他区域都是白色的，而matlab中默认计算都是***白色区域***，因此对原始图像进行反色运算。
2. imclose()/imopen()，即闭运算和开运算，闭运算是指先膨胀，后腐蚀，使得一些区域闭合；开运算是指先腐蚀后膨胀，用于消除一些小的干扰像素。
3. imfill，图像填充，将闭合区域填充成白色，这样方便计算面积。
4. im2bw,图像二值化，方便后续计算，我想计算孔洞面积，直接适用sum函数所有像素和即可，是不是很方面。
5. [L,num]=bwlabel(bw,n)，对二值图像中的闭合区域进行标注，L即为保存闭合区域的矩阵，num是闭合区域个数。
6. regionprops,用于度量图像区域属性，如周长，面积，离心率等，接受bwlabel传过来的参数。是的，用这个函数计算孔洞面积也是可以的。

整个的代码如下：

    clc; clear;

    I = imread('d:\1814.png');
    %灰度处理
    I1 = rgb2gray(I);
    %黑白交换颜色
    I2 = imcomplement(I1);

    %imclose:闭运算，先膨胀后腐蚀，闭合图形
    %imopen:开运算，先腐蚀后膨胀，清楚非边缘细小点的影像
    %https://blog.csdn.net/zhengalen/article/details/51446791
    %strel:构造结构元素，用于膨胀和腐蚀
    se = strel('disk',4);
    I3 = imclose(I2,se);
    %I3 = imopen(I2,se);

    %填充空洞
    I4 = imfill(I3,'holes');

    %自动计算阈值，并对灰度图像二值化
    thresh = graythresh(I4);
    I5 = im2bw(I4,thresh);

    %计算空洞的面积
    %图像总面积
    total_area = 1000;
    %sum:二值化后计算各像素值的和，即为空洞面积
    %numel:图像的总像素个数
    %area_prop:计算空洞占图像总面积的比例
    area_prop = sum(I5(:))/numel(I5);
    %计算空洞的面积
    hole_area = area_prop*total_area;
    fprintf('the prop of hole area is %f\n',area_prop);
    fprintf('the hole area is %f\n',hole_area);

    %上边的代码已可以计算空洞面积
    %下边是用来检查二值化后的图像是否正确
    %the function 'regionprops' is very great
    %https://blog.csdn.net/qq_38376586/article/details/90216424
    [labelpic,num] = bwlabel(I5,8);
    status = regionprops(labelpic,'BoundingBox');
    centroid = regionprops(labelpic,'Centroid');
    figure;
    imshow(labelpic);
    %对每个空洞添加矩形框，并用数字标注
    for i = 1:num
    rectangle('position',status(i).BoundingBox,'edgecolor','r');
    text(centroid(i,1).Centroid(1,1)-15,centroid(i,1).Centroid(1,2)-15,num2str(i),'Color','r')
    end

参考文献：

1. https://blog.csdn.net/qq_38376586/article/details/90216424
2. https://zhuanlan.zhihu.com/p/76974326
3. https://www.ilovematlab.cn/thread-325236-1-1.html
4. https://blog.csdn.net/zhengalen/article/details/51446791