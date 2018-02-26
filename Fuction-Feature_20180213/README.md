# 功能与特性

记录于2018/2/13

## 基本信息

Device: Redmi 3S

ROM: MIUI 9.2.1.0 (MALCNEK)

Android: 6.0.1

OpenHub: 2.7.1

## 问题

### 分享

截图：

&nbsp; | &nbsp;
------------ | -------------
![](https://github.com/pzhlkj6612/OpenHubIssuesRelated/blob/master/Fuction-Feature_20180213/20180209001939_com.thirtydegreesray.openhub_Share.png) | ![](https://github.com/pzhlkj6612/OpenHubIssuesRelated/blob/master/Fuction-Feature_20180213/20180209001957_com.thirtydegreesray.openhub_Shared.png)

1. “未安装邮件客户端”，这个提示所在位置，英文版是“Share to”，是不是代码有问题；
2. “返回第三方工具”，这个没写好；
3. 这个分享，最终就是把链接直接发过去了，仅仅是在菜单 -`复制链接`这个操作上做了一点延伸。我的建议是，带上当前页面的标题，然后跟链接一起分享过去，就像这样：
```
Issues · ThirtyDegreesRay/OpenHub
https://github.com/ThirtyDegreesRay/OpenHub/issues
```

----

### Pull Request相关的翻译以及功能缺失

截图：

![](https://github.com/pzhlkj6612/OpenHubIssuesRelated/blob/master/Fuction-Feature_20180213/20180204161045_com.thirtydegreesray.openhub_PR.png)

1. 所有PR相关的活动，点进去都是直接到Repo主页，这个功能应该是还不完整的；
2. [issuecomment-361462934 - News页面语言混乱显示问题 · Issue #49 · ThirtyDegreesRay/OpenHub](https://github.com/ThirtyDegreesRay/OpenHub/issues/49#issuecomment-361462934)提到的翻译问题依然没有解决。

另外，以后完善PR期间，可以试试能否正确处理[这个PR](https://github.com/kelseyhightower/nocode/pull/1532)的标题啥的。

----

### Commit相关功能的入口覆盖不完全

截图：

&nbsp; | &nbsp; | &nbsp;
------------ | ------------- | -------------
![](https://github.com/pzhlkj6612/OpenHubIssuesRelated/blob/master/Fuction-Feature_20180213/20180213163847_com.thirtydegreesray.openhub_1_Mousedown.png) | ![](https://github.com/pzhlkj6612/OpenHubIssuesRelated/blob/master/Fuction-Feature_20180213/20180213163939_com.thirtydegreesray.openhub_1_Menu.png) | ![](https://github.com/pzhlkj6612/OpenHubIssuesRelated/blob/master/Fuction-Feature_20180213/20180213163947_com.thirtydegreesray.openhub_1_Result.png)
![](https://github.com/pzhlkj6612/OpenHubIssuesRelated/blob/master/Fuction-Feature_20180213/20180213163957_com.thirtydegreesray.openhub_2_Mousedown.png) | ![](https://github.com/pzhlkj6612/OpenHubIssuesRelated/blob/master/Fuction-Feature_20180213/20180213164050_com.thirtydegreesray.openhub_2_Menu.png) | ![](https://github.com/pzhlkj6612/OpenHubIssuesRelated/blob/master/Fuction-Feature_20180213/20180213164057_com.thirtydegreesray.openhub_2_Result.png)

1. “Commit”的评论显示不出来；
2. 如果的确是没做功能，那也可以尽量多地提供信息，第二种情况下，至少可以链接到对应的“Commit”上去。

----

### 检查新版本

截图：

![](https://github.com/pzhlkj6612/OpenHubIssuesRelated/blob/master/Fuction-Feature_20180213/20180203003405_com.thirtydegreesray.openhub_NoNewerVersion.png)

当时2.6.0已经出了，但检查不到新版本（小米应用商店当时只有2.5.0），这里的代码如果直接用[GitHub的API](https://developer.github.com/v3/repos/releases/)可能会好一些吧？不懂这个，你检查一下。

----

### ClosedIssues列表不加判断，抓入PR

截图：

![](https://github.com/pzhlkj6612/OpenHubIssuesRelated/blob/master/Fuction-Feature_20180213/20180213112500_com.thirtydegreesray.openhub_IssuesIncludePR.png)

这个可能得好好折腾下了，因为现在好像还不能浏览某个Repo的PR。
