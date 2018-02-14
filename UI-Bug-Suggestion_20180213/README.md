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

录屏（实际上录屏是看不到的，这是用合成软件做的，跟我看到的差不多）：

![](https://github.com/pzhlkj6612/OpenHubIssuesRelated/blob/master/UI-Bug-Suggestion_20180213/20180213211800_com.thirtydegreesray.openhub_BrightnessShake.gif)

这个图片在[图片变形（解决的话可能会较困难） - OpenHubIssuesRelated/Picture-Display_20180213 at master · pzhlkj6612/OpenHubIssuesRelated](https://github.com/pzhlkj6612/OpenHubIssuesRelated/tree/master/Picture-Display_20180213#%E5%9B%BE%E7%89%87%E5%8F%98%E5%BD%A2%E8%A7%A3%E5%86%B3%E7%9A%84%E8%AF%9D%E5%8F%AF%E8%83%BD%E4%BC%9A%E8%BE%83%E5%9B%B0%E9%9A%BE)提到过，不知道是不是`<img>`引起的。

----

##### Issue里过长的Label显示不完整

截图：

![](https://github.com/pzhlkj6612/OpenHubIssuesRelated/blob/master/UI-Bug-Suggestion_20180213/20180204161229_com.thirtydegreesray.openhub_TooLongLabel.png)

要不就换个行？

其它地方的Label也去检查下嘛。

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

录屏：

![](https://github.com/pzhlkj6612/OpenHubIssuesRelated/blob/master/UI-Bug-Suggestion_20180213/20180213193100_com.thirtydegreesray.openhub_ContextMenu-ListSlide.gif)

News页面、个人/团队的Activities页面，长按某一项不松手，出现菜单后依然能滑动列表；

其它页面可能也有这样的情况，要细细检查。

----

#### 有能够被长按控件的（可能）所有的页面会对屏幕显示范围以外的触摸事件进行反馈

录屏：

&nbsp; | &nbsp;
------------ | -------------
![](https://github.com/pzhlkj6612/OpenHubIssuesRelated/blob/master/UI-Bug-Suggestion_20180213/20180213234400_com.thirtydegreesray.openhub_IncorrctReact_1.gif) | ![](https://github.com/pzhlkj6612/OpenHubIssuesRelated/blob/master/UI-Bug-Suggestion_20180213/20180213234401_com.thirtydegreesray.openhub_IncorrctReact_2.gif)

看图吧。

----

### Suggestions

#### Search

历史搜索不能被清空。

----

#### Repo

##### 无法手动更新首页的README

README更新后，重新进入Repo首页不更新（有缓存），也无法手动更新。

----

##### 无法手动更新任何单独打开的文档

无论是代码还是图片，都无法手动刷新；当然，**这个也可以不做**，意义不大。

----

##### 首页的README的加载条没有文档内的加载条明显

其实还好，因为这个加载的状态不怎么影响阅读。

----

#### 文档加载完成后会回到顶部

这个问题有一个矛盾：

* 在加载完当前文档之前，是否允许用户浏览文档内容

如果文档内含有大量图片，那就会有很差的阅读体验；但如果用户在看加载中的文档，突然又回到顶部，这可能也会不舒服。所以能否在加载方式上做工作呢？

----

#### 上划（下滑）加载内容观感不太好

1. 加载的转圈动画在下方显示，比较好；
2. 上划（下滑）到底时，整个列表会很钝地停在末尾，也没有一个多出的“空白”来“告诉”用户接下来还有内容;
3. 因为上边的转圈动画并不是很显眼（在News里看来），所以即使接下来的内容加载好了，用户也有可能不知道，只能试着再往下滑，这体验不太好。

----

#### 能通过设备的菜单键和右上角菜单按钮打开的菜单不统一

截图：

&nbsp; | &nbsp;
------------ | -------------
![](https://github.com/pzhlkj6612/OpenHubIssuesRelated/blob/master/UI-Bug-Suggestion_20180213/20180214001502_com.thirtydegreesray.openhub_ContextMenuDisplay_1.png) | ![](https://github.com/pzhlkj6612/OpenHubIssuesRelated/blob/master/UI-Bug-Suggestion_20180213/20180214001502_com.thirtydegreesray.openhub_ContextMenuDisplay_2.png)

其实可以全部统一到右上角去，就像微信那样。

----

#### 左侧右滑菜单

##### 外观：顶部空余太大

截图及处理后的样子：

&nbsp; | &nbsp;
------------ | -------------
![](https://github.com/pzhlkj6612/OpenHubIssuesRelated/blob/master/UI-Bug-Suggestion_20180213/20180214091639_com.thirtydegreesray.openhub_MainMenu_1.png) | ![](https://github.com/pzhlkj6612/OpenHubIssuesRelated/blob/master/UI-Bug-Suggestion_20180213/20180214091639_com.thirtydegreesray.openhub_MainMenu_2.png)

1. 把“profile”合到头像名字那里去，点那儿就是进个人简介（这个设计上可能会复杂一些吧）；
2. 如果这样调整布局的话，多的空间就省出来了。“logout”和“add account”可以挪到菜单最下边了，不搞那个小三角按钮了。

----

##### 逻辑：“以它为底”

`News`、`My Repos`、`Starred Repos`、`Bookmarks`、`Trace`、`Repo Collections`、`Featured Topics`、`Global News`，当用户在这些页面时，按系统的“返回”键，就会直接回到上一应用/桌面。

怎么说呢，那么长时间了，我是一直没习惯这种，会猝不及防地“被”退出OpenHub，很难受。

不如这样吧，在这些个页面按返回时，就滑出主菜单，代表我访问到“根节点”了，这样或许好一些呢。

这种处理的话比我之前想的“再按一次退出OpenHub”要美观得多。

----

##### 记忆上次的停留位置

按习惯来讲，主菜单做这个，没必要嘛。你都已经把最贴近用户内容的`Profile`、`My Repo`啥的放最上边了，那就让菜单每次被打开时，正常显示就好了嘛。

----

#### “关于”页面

截图及处理后的样子：

&nbsp; | &nbsp;
------------ | -------------
![](https://github.com/pzhlkj6612/OpenHubIssuesRelated/blob/master/UI-Bug-Suggestion_20180213/20180212225927_com.thirtydegreesray.openhub_About-App_1.png) | ![](https://github.com/pzhlkj6612/OpenHubIssuesRelated/blob/master/UI-Bug-Suggestion_20180213/20180212225927_com.thirtydegreesray.openhub_About-App_2.png)
![](https://github.com/pzhlkj6612/OpenHubIssuesRelated/blob/master/UI-Bug-Suggestion_20180213/20180212225927_com.thirtydegreesray.openhub_About-Author_1.png) | ![](https://github.com/pzhlkj6612/OpenHubIssuesRelated/blob/master/UI-Bug-Suggestion_20180213/20180212225927_com.thirtydegreesray.openhub_About-Author_2.png)

1. “App信息”那里功能可以合并，上边是“检查更新”，下边是进Repo；
2. “作者信息”，上边是进你的GitHub主页，下边是你的邮箱。
