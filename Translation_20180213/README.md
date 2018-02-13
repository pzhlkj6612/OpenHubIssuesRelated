# 翻译相关问题

记录于2018/2/13

## 基本信息

Device: Redmi 3S

ROM: MIUI 9.2.1.0 (MALCNEK)

Android: 6.0.1

OpenHub: 2.7.1

## 问题

### 检查更新翻译对应有错&用词

截图：

&nbsp; | &nbsp;
------------ | -------------
![](https://github.com/pzhlkj6612/OpenHubIssuesRelated/blob/master/Translation_20180213/20180212225718_com.thirtydegreesray.openhub_Checking-upgrade.png) | ![](https://github.com/pzhlkj6612/OpenHubIssuesRelated/blob/master/Translation_20180213/20180213172533_com.thirtydegreesray.openhub_Checking-upgrade_Chinese.png)

第一，对应的string有问题；

第二，这种更新应该是“update”吧。我查了下资料（[Difference Between Update and Upgrade | Difference Between](http://www.differencebetween.net/technology/difference-between-update-and-upgrade/)），对于产品的更新，在词义上，“upgrade”的意思更贴切，但是有这么一句：

> Updates are always free as they are not distinct software but are only meant to modify a pre-existing installation. On the other hand, upgrades are distinct and do not need the older software to function.

所以可能“update”更好一些。

----

### 版本库中的“分支”应该为“分叉”

截图：

&nbsp; | &nbsp;
------------ | -------------
![](https://github.com/pzhlkj6612/OpenHubIssuesRelated/blob/master/Translation_20180213/20180213145831_com.thirtydegreesray.openhub_Forks_Out.png) | ![](https://github.com/pzhlkj6612/OpenHubIssuesRelated/blob/master/Translation_20180213/20180213145835_com.thirtydegreesray.openhub_Forks_In.png)

首先，这是“Forks”，英文界面翻译没问题，再结合[issuecomment-360036095 - Repo README-cn.md 小问题 · Issue #46 · ThirtyDegreesRay/OpenHub](https://github.com/ThirtyDegreesRay/OpenHub/issues/46#issuecomment-360036095)，就应该是“分叉”；

另外，从实际情况上讲，“fork”的确是创建了一条当前项目的“branch”，但也只是这么理解，以“版本库分支”来命名还是不太妥；

再说了，右上角就有“分支”的按钮，对吧。

----

### News页面翻译问题

截图：

![](https://github.com/pzhlkj6612/OpenHubIssuesRelated/blob/master/Translation_20180213/20180204161045_com.thirtydegreesray.openhub_SomethingHappenedInARepo.png)

其它的就摘录过来：
> 发表评论在问题x **user/repo**<br/>
> <br/>
> 创建标签tag<br/>
> 关闭问题num在**user/repo**<br/>
> 发布版本ver在**user/repo**<br/>
> 提交到分支branch在**user/repo**<br/>
> 发表评论在**user/repo**的提交中<br/>
> ...

* 状语该前置就前置嘛，虽然大家都能读懂，但是不舒服啊；
* 第一条的顺序完全混乱了，英文是“Created comment on Issue x in **user/repo**”；
* 我估计在其它显示了动态的地方，这个翻译也是这样的，所以你要注意检查。
