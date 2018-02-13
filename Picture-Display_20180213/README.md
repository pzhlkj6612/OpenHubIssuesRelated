# 图片显示问题

记录于2018/2/13

## 基本信息

Device: Redmi 3S

ROM: MIUI 9.2.1.0 (MALCNEK)

Android: 6.0.1

OpenHub: 2.7.1

## 问题

### 图片变形（解决的话可能会较困难）

位置：[Xamarin.Forms/README.md at master · xamarin/Xamarin.Forms](https://github.com/xamarin/Xamarin.Forms/blob/master/README.md)

示例：
``` html
<img src="banner.png" alt="Xamarin.Forms banner" height="145" >
```
<img src="https://github.com/xamarin/Xamarin.Forms/blob/master/banner.png" alt="Xamarin.Forms banner" height="145" >

由于原图是1600x256，我手机的分辨率是1280x720，横竖都不够，所以图片被强制拉伸，变形了；当然，单独查看图片时没有问题。

截图：

&nbsp; | &nbsp;
------------ | -------------
![](https://github.com/pzhlkj6612/OpenHubIssuesRelated/blob/master/Picture-Display_20180213/20180213111358_com.thirtydegreesray.openhub_Repo_Vertical.png) | ![](https://github.com/pzhlkj6612/OpenHubIssuesRelated/blob/master/Picture-Display_20180213/20180213111413_com.thirtydegreesray.openhub_README_Vertical.png)
![](https://github.com/pzhlkj6612/OpenHubIssuesRelated/blob/master/Picture-Display_20180213/20180213114234_com.thirtydegreesray.openhub_Repo_Horizontal.png) | ![](https://github.com/pzhlkj6612/OpenHubIssuesRelated/blob/master/Picture-Display_20180213/20180213114239_com.thirtydegreesray.openhub_Standalone_Horizontal.png)

----

### 单独查看图片相关问题

#### 单独查看图片时不能双击放大缩小

可以的话就加上这一套功能？

----

#### 单独查看图片时会重新加载

位置：[ZhihuPaper-31567795/md4GitHub.md at master · pzhlkj6612/ZhihuPaper-31567795](https://github.com/pzhlkj6612/ZhihuPaper-31567795/blob/master/md4GitHub.md)

这个md里有大量的图片（包括GIF），如果打开某图片后再次加载，势必会浪费时间和数据流量，如果能直接用缓存里的，就好得多呢。

刚试了下，长按图片复制到的链接和打开图片复制到的链接是相同的，所以在原理上这应该是能做到的。
