# UI

记录于2018/2/13

## 基本信息

Device: Redmi 3S

ROM: MIUI 9.2.1.0 (MALCNEK)

Android: 6.0.1

OpenHub: 2.7.1

## 问题

### Bugs

#### Repo

##### 首页上README表格滑动体验差

截图：

![](https://github.com/pzhlkj6612/OpenHubIssuesRelated/blob/master/UI-Bug-Suggestion_20180213/20180213174606_com.thirtydegreesray.openhub_SlideTable.png)

直接左滑会滑动Repo首页的选项卡，当然，表格也会动一下（跟早些时候知乎答案里的代码块一样）。

----

##### 滑动会导致首页的某种图片闪烁

截图：

![](https://github.com/pzhlkj6612/OpenHubIssuesRelated/blob/master/UI-Bug-Suggestion_20180213/20180213211800_com.thirtydegreesray.openhub_BrightnessShake.gif)

这个图片在[图片变形（解决的话可能会较困难） - OpenHubIssuesRelated/Picture-Display_20180213 at master · pzhlkj6612/OpenHubIssuesRelated](https://github.com/pzhlkj6612/OpenHubIssuesRelated/tree/master/Picture-Display_20180213#%E5%9B%BE%E7%89%87%E5%8F%98%E5%BD%A2%E8%A7%A3%E5%86%B3%E7%9A%84%E8%AF%9D%E5%8F%AF%E8%83%BD%E4%BC%9A%E8%BE%83%E5%9B%B0%E9%9A%BE)提到过，不知道是不是`<img>`引起的。

----

##### Issue里过长的Label显示不完整

截图：

![](https://github.com/pzhlkj6612/OpenHubIssuesRelated/blob/master/UI-Bug-Suggestion_20180213/20180204161229_com.thirtydegreesray.openhub_TooLongLabel.png)

要不就换个行？

其它地方的Comment也去检查下嘛。

----

##### Issue的Comment的编辑按钮位置问题

截图：

&nbsp; | &nbsp;
------------ | -------------
![](https://github.com/pzhlkj6612/OpenHubIssuesRelated/blob/master/UI-Bug-Suggestion_20180213/20180212224601_com.thirtydegreesray.openhub_CommentOfIssue_1.png) | ![](https://github.com/pzhlkj6612/OpenHubIssuesRelated/blob/master/UI-Bug-Suggestion_20180213/20180213112710_com.thirtydegreesray.openhub_CommentOfIssue_2.png)

1. 挡住时间/日期了;
2. 不只是第一条Comment能编辑，但每个Comment都来一个大按钮，就很奇怪；
3. 可能你应该做Issue标题的编辑？然后把编辑按钮与发表评论的按钮合一起，用的时候分开成俩（不知道怎么描述），如果当前用户是Issue作者，就有俩选项，否则就只能发表评论；
4. 标题能编辑了，Comment的编辑功能也不能缺，你可以在每一条属于当前用户的Comment上，弄上下文菜单（现在是，第一条Comment只有Share，无论作者是谁）；
5. 进入某条Comment后，也应该有完整的菜单（现在菜单按钮都没有）。

----

#### Activity的上下文菜单

![](https://github.com/pzhlkj6612/OpenHubIssuesRelated/blob/master/UI-Bug-Suggestion_20180213/20180213193100_com.thirtydegreesray.openhub_ContextMenu-ListSlide.gif)

News页面、个人/团队的Activities页面，长按某一项不松手，出现菜单后依然能滑动列表；

其它页面可能也有这样的情况，要细细检查。

----

#### 有能够被长按控件的（可能）所有的页面会对屏幕显示范围以外的触摸事件进行反馈

截图：

&nbsp; | &nbsp;
------------ | -------------
![](https://github.com/pzhlkj6612/OpenHubIssuesRelated/blob/master/UI-Bug-Suggestion_20180213/20180213234400_com.thirtydegreesray.openhub_IncorrctReact_1.gif) | ![](https://github.com/pzhlkj6612/OpenHubIssuesRelated/blob/master/UI-Bug-Suggestion_20180213/20180213234401_com.thirtydegreesray.openhub_IncorrctReact_2.gif)

看图吧。

----

### Suggestions

#### Repo

##### 无法手动更新Repo首页内容

README更新后，重新进入Repo首页不更新（有缓存），也无法手动更新。

----

##### 无法手动更新任何单独打开的文档

无论是代码还是图片，都无法手动刷新；当然，**这个也可以不做**，意义不大。

----

#### 文档加载完成后会回到