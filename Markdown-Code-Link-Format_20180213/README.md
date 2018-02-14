# Markdown解析 代码高亮 链接解析 格式问题

记录于2018/2/13

## 基本信息

Device: Redmi 3S

ROM: MIUI 9.2.1.0 (MALCNEK)

Android: 6.0.1

OpenHub: 2.7.1

## 问题

### 行内代码段不显示样式

位置：[Xamarin.Forms/README.md at master · xamarin/Xamarin.Forms](https://github.com/xamarin/Xamarin.Forms/blob/master/README.md)

示例：`I'm the code`

截图：

&nbsp; | &nbsp;
------------ | -------------
![](https://github.com/pzhlkj6612/OpenHubIssuesRelated/blob/master/Markdown-Code-Link-Format_20180213/20180213115121_com.thirtydegreesray.openhub_CodeStyle_F.png) | ![](https://github.com/pzhlkj6612/OpenHubIssuesRelated/blob/master/Markdown-Code-Link-Format_20180213/20180213115209_com.thirtydegreesray.openhub_CodeStyle_T.png)

----

### CSharp代码着色不全

位置：[MFC-StringTable-Generator-1/Program.cs at master · pzhlkj6612/MFC-StringTable-Generator-1](https://github.com/pzhlkj6612/MFC-StringTable-Generator-1/blob/master/MFC-StringTable-Generator-1/Program.cs)

示例：
``` CSharp
using System.IO;
```

截图：

![](https://github.com/pzhlkj6612/OpenHubIssuesRelated/blob/master/Markdown-Code-Link-Format_20180213/20180213115026_com.thirtydegreesray.openhub_CSharp-System_IO.png)

----

### 链接相关

#### 协议影响链接的解析

示例：
``` Markdown
[只有`//`](//github.com/pzhlkj6612/OpenHubIssuesRelated/tree/master/Markdown-Code-Link-Format_20180213)
```
[只有`//`](//github.com/pzhlkj6612/OpenHubIssuesRelated/tree/master/Markdown-Code-Link-Format_20180213)，会直接把链接拼接到当前目录后，最后就成了：
```
https://github.com/pzhlkj6612/OpenHubIssuesRelated/blob/master/Markdown-Code-Link-Format_20180213//github.com/pzhlkj6612/OpenHubIssuesRelated/tree/master/Markdown-Code-Link-Format_20180213
```
一般境况下，是一定会404的。

GitHub网页端，这种链接能够被正确解析。

截图：

![](https://github.com/pzhlkj6612/OpenHubIssuesRelated/blob/master/Markdown-Code-Link-Format_20180213/20180213134540_com.thirtydegreesray.openhub_404.png)

----

#### 2018-02-14更新

``` Markdown
[.](./OpenHubIssuesRelated/tree/master/Markdown-Code-Link-Format_20180213)
```
[只有一个.](.)，也会出现错误的拼接，看起来对于链接的处理还有较多的问题。

----

#### 当前文档内id属性跳转

示例：
``` Markdown
[CSharp代码着色不全](//github.com/pzhlkj6612/OpenHubIssuesRelated/tree/master/Markdown-Code-Link-Format_20180213#csharp%E4%BB%A3%E7%A0%81%E7%9D%80%E8%89%B2%E4%B8%8D%E5%85%A8)
```
[CSharp代码着色不全](//github.com/pzhlkj6612/OpenHubIssuesRelated/tree/master/Markdown-Code-Link-Format_20180213#csharp%E4%BB%A3%E7%A0%81%E7%9D%80%E8%89%B2%E4%B8%8D%E5%85%A8)

另外，我注意到[Issue #24](https://github.com/ThirtyDegreesRay/OpenHub/issues/24)提到的应该是类似的问题。
