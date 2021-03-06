![(logo)](http://images.cnitblog.com/blog2015/497279/201505/051004492043385.png)
## MJRefresh
* The easiest way to use pull-to-refresh
* 用法最简单的下拉刷新框架：一行代码搞定

## Contents
* Getting Started
    * [Features【支持哪些控件的刷新】](#支持哪些控件的刷新)
    * [Installation【如何使用MJRefresh】](#如何使用MJRefresh)
    * [Who's using【已经超过上百个App正在使用MJRefresh】](#已经超过上百个App正在使用MJRefresh)
    * [Classes【MJRefresh类结构图】](#MJRefresh类结构图)
* Examples
    * [Reference【参考】](#参考)
    * [Header Refresh 01 - Default【下拉刷新01-默认】](#下拉刷新01-默认)
    * [Header Refresh 02 - With GIF【下拉刷新02-动画图片】](#下拉刷新02-动画图片)
    * [Header Refresh 03 - Hide Update Time【下拉刷新03-隐藏时间】](#下拉刷新03-隐藏时间)
    * [Header Refresh 04 - Hide Refreshing Text and Time【下拉刷新04-隐藏状态和时间】](#下拉刷新04-隐藏状态和时间)
    * [Header Refresh 05 - Customize Refreshing Text【下拉刷新05-自定义文字】](#下拉刷新05-自定义文字)
    * [Header Refresh 06 - Customize Refreshing Header【下拉刷新06-自定义刷新控件】](#下拉刷新06-自定义刷新控件)
    * [Footer Refresh 01 - Default【上拉刷新01-默认】](#上拉刷新01-默认)
    * [Footer Refresh 02 - With GIF【上拉刷新02-动画图片】](#上拉刷新02-动画图片)
    * [Footer Refresh 03 - Customize Refreshing Text【上拉刷新03-隐藏刷新状态的文字】](#上拉刷新03-隐藏刷新状态的文字)
    * [Footer Refresh 04 - Display "Load Complete"【上拉刷新04-全部加载完毕】](#上拉刷新04-全部加载完毕)
    * [Footer Refresh 05 - Customize Refreshing Text【上拉刷新05-自定义文字】](#上拉刷新05-自定义文字)
    * [Footer Refresh 06 - Hide After Finish Refresh【上拉刷新06-加载后隐藏】](#上拉刷新06-加载后隐藏)
    * [Footer Refresh 07 - Bouncing Refresh01【上拉刷新07-自动回弹的上拉01】](#上拉刷新07-自动回弹的上拉01)
    * [Footer Refresh 08 - Bouncing Refresh02【上拉刷新08-自动回弹的上拉02】](#上拉刷新08-自动回弹的上拉02)
    * [Footer Refresh 09 - Customize Refreshing Footer(Release To Refresh)【上拉刷新09-自定义刷新控件(自动刷新)】](#上拉刷新09-自定义刷新控件(自动刷新))
    * [Footer Refresh 10 - Customize Refreshing Footer(Bouncing Refresh)【上拉刷新10-自定义刷新控件(自动回弹)】](#上拉刷新10-自定义刷新控件(自动回弹))
    * [UICollectionView01-Refresh on Header and Footer【UICollectionView01-上下拉刷新】](#UICollectionView01-上下拉刷新)
    * [UIWebView01- Header Refresh【UIWebView01-下拉刷新】](#UIWebView01-下拉刷新)
* [期待](#期待)

## <a id="支持哪些控件的刷新"></a>What are supported【支持哪些控件的刷新】
* `UIScrollView`、`UITableView`、`UICollectionView`、`UIWebView`

## <a id="如何使用MJRefresh"></a>How to use MJRefresh如何使用MJRefresh】
* cocoapods：`pod 'MJRefresh'`
* 手动导入：
    * 将`MJRefresh`文件夹中的所有文件拽入项目中
    * 导入主头文件：`#import "MJRefresh.h"`

```objc
Base                        Custom
MJRefresh.bundle            MJRefresh.h
MJRefreshConst.h            MJRefreshConst.m
UIScrollView+MJExtension.h  UIScrollView+MJExtension.m
UIScrollView+MJRefresh.h    UIScrollView+MJRefresh.m
UIView+MJExtension.h        UIView+MJExtension.m
```

## <a id="已经超过上百个App正在使用MJRefresh"></a>There are more than 100 apps are using MJRefresh【已经超过上百个App正在使用MJRefresh】
<img src="http://images0.cnblogs.com/blog2015/497279/201506/141212365041650.png" width="200" height="300">
* 更多App信息可以关注：[M了个J-博客园](http://www.cnblogs.com/mjios/p/4409853.html)

## <a id="MJRefresh类结构图"></a>MJRefresh Class Diagram【MJRefresh类结构图】
![](http://images0.cnblogs.com/blog2015/497279/201506/132232456139177.png)
- 图中`红色文字的类`：可以直接拿来用
    - 下拉刷新控件的种类
        - 默认（Normal）：`MJRefreshNormalHeader`
        - 动图（Gif）：`MJRefreshGifHeader`
    - 上拉刷新控件的种类
        - 自动刷新（Auto）
            - 默认（Normal）：`MJRefreshAutoNormalFooter`
            - 动图（Gif）：`MJRefreshAutoGifFooter`
        - 自动回弹（Back）
            - 默认（Normal）：`MJRefreshBackNormalFooter`
            - 动图（Gif）：`MJRefreshBackGifFooter`
- 图中`非红色文字的类`：拿来继承，用于自定义刷新控件
- 关于如何自定义刷新控件，可以参考下图的类<br>
<img src="http://images0.cnblogs.com/blog2015/497279/201506/141358159107893.png" width="30%" height="30%">

## <a id="参考"></a>参考
```objc
* 由于这个框架的功能较多，就不写具体文字描述其用法
* 大家可以直接参考示例中的MJTableViewController、MJCollectionViewController、MJWebViewController，更为直观快速
```
<img src="http://images0.cnblogs.com/blog2015/497279/201506/141345470048120.png" width="30%" height="30%">

## <a id="下拉刷新01-默认"></a>Header Refresh 01 - Default【下拉刷新01-默认】
```objc
self.tableView.header = [MJRefreshNormalHeader headerWithRefreshingBlock:^{
   // Call the block when go into the refreshing state【进入刷新状态后会自动调用这个block】
}];
或
// Set call back【设置回调（一旦进入刷新状态，就调用target的action，也就是调用self的loadNewData方法）】
self.tableView.header = [MJRefreshNormalHeader headerWithRefreshingTarget:self refreshingAction:@selector(loadNewData)];

// Directly go into the refreshing mode【马上进入刷新状态】
[self.tableView.header beginRefreshing];
```
![(下拉刷新01-普通)](http://images0.cnblogs.com/blog2015/497279/201506/141204343486151.gif)

## <a id="下拉刷新02-动画图片"></a>Header Refresh 02 - With GIF【下拉刷新02-动画图片】
```objc
// 设置回调（一旦进入刷新状态，就调用target的action，也就是调用self的loadNewData方法）
MJRefreshGifHeader *header = [MJRefreshGifHeader headerWithRefreshingTarget:self refreshingAction:@selector(loadNewData)];
// 设置普通状态的动画图片
[header setImages:idleImages forState:MJRefreshStateIdle];
// 设置即将刷新状态的动画图片（一松开就会刷新的状态）
[header setImages:pullingImages forState:MJRefreshStatePulling];
// 设置正在刷新状态的动画图片
[header setImages:refreshingImages forState:MJRefreshStateRefreshing];
// 设置header
self.tableView.header = header;
```
![(下拉刷新02-动画图片)](http://images0.cnblogs.com/blog2015/497279/201506/141204402238389.gif)

## <a id="下拉刷新03-隐藏时间"></a>Header Refresh 03 - Hide Update Time【下拉刷新03-隐藏时间】
```objc
// Hide Time【隐藏时间】
header.lastUpdatedTimeLabel.hidden = YES;
```
![(下拉刷新03-隐藏时间)](http://images0.cnblogs.com/blog2015/497279/201506/141204456132944.gif)

## <a id="下拉刷新04-隐藏状态和时间"></a>Header Refresh 04 - Hide Refreshing Text and Time【下拉刷新04-隐藏状态和时间】
```objc
// Hide Time【隐藏时间】
header.lastUpdatedTimeLabel.hidden = YES;

// Hide State【隐藏状态】
header.stateLabel.hidden = YES;
```
![(下拉刷新04-隐藏状态和时间0)](http://images0.cnblogs.com/blog2015/497279/201506/141204508639539.gif)

## <a id="下拉刷新05-自定义文字"></a>Header Refresh 05 - Customize Refreshing Text【下拉刷新05-自定义文字】
```objc
// 设置文字
[header setTitle:@"Pull down to refresh" forState:MJRefreshStateIdle];
[header setTitle:@"Release to refresh" forState:MJRefreshStatePulling];
[header setTitle:@"Loading ..." forState:MJRefreshStateRefreshing];

// 设置字体
header.stateLabel.font = [UIFont systemFontOfSize:15];
header.lastUpdatedTimeLabel.font = [UIFont systemFontOfSize:14];

// 设置颜色
header.stateLabel.textColor = [UIColor redColor];
header.lastUpdatedTimeLabel.textColor = [UIColor blueColor];
```
![(下拉刷新05-自定义文字)](http://images0.cnblogs.com/blog2015/497279/201506/141204563633593.gif)

## <a id="下拉刷新06-自定义刷新控件"></a>Header Refresh 06 - Customize Refreshing Header【下拉刷新06-自定义刷新控件】
```objc
self.tableView.header = [MJDIYHeader headerWithRefreshingTarget:self refreshingAction:@selector(loadNewData)];
// 具体实现参考MJDIYHeader.h和MJDIYHeader.m
```
![(下拉刷新06-自定义刷新控件)](http://images0.cnblogs.com/blog2015/497279/201506/141205019261159.gif)

## <a id="上拉刷新01-默认"></a>Footer Refresh 01 - Default【上拉刷新01-默认】
```objc
self.tableView.footer = [MJRefreshAutoNormalFooter footerWithRefreshingBlock:^{
   // 进入刷新状态后会自动调用这个block
}];
或
// 设置回调（一旦进入刷新状态，就调用target的action，也就是调用self的loadMoreData方法）
self.tableView.footer = [MJRefreshAutoNormalFooter footerWithRefreshingTarget:self refreshingAction:@selector(loadMoreData)];
```
![(上拉刷新01-默认)](http://images0.cnblogs.com/blog2015/497279/201506/141205090047696.gif)

## <a id="上拉刷新02-动画图片"></a>Footer Refresh 02 - With GIF【上拉刷新02-动画图片】
```objc
// 设置回调（一旦进入刷新状态，就调用target的action，也就是调用self的loadMoreData方法）
MJRefreshAutoGifFooter *footer = [MJRefreshAutoGifFooter footerWithRefreshingTarget:self refreshingAction:@selector(loadMoreData)];

// 设置刷新图片
[footer setImages:refreshingImages forState:MJRefreshStateRefreshing];

// 设置尾部
self.tableView.footer = footer;
```
![(上拉刷新02-动画图片)](http://images0.cnblogs.com/blog2015/497279/201506/141205141445793.gif)

## <a id="上拉刷新03-隐藏刷新状态的文字"></a>Footer Refresh 03 - Customize Refreshing Text【上拉刷新03-隐藏刷新状态的文字】
```objc
// 隐藏刷新状态的文字
footer.refreshingTitleHidden = YES;
// 如果没有上面的方法，就用footer.stateLabel.hidden = YES;
```
![(上拉刷新03-隐藏刷新状态的文字)](http://images0.cnblogs.com/blog2015/497279/201506/141205200985774.gif)

## <a id="上拉刷新04-全部加载完毕"></a>Footer Refresh 04 - Display "Load Complete"【上拉刷新04-全部加载完毕】
```objc
// 变为没有更多数据的状态
[footer noticeNoMoreData];
```
![(上拉刷新04-全部加载完毕)](http://images0.cnblogs.com/blog2015/497279/201506/141205248634686.gif)

## <a id="上拉刷新05-自定义文字"></a>Footer Refresh 05 - Customize Refreshing Text【上拉刷新05-自定义文字】
```objc
// 设置文字
[footer setTitle:@"Click or drag up to refresh" forState:MJRefreshStateIdle];
[footer setTitle:@"Loading more ..." forState:MJRefreshStateRefreshing];
[footer setTitle:@"No more data" forState:MJRefreshStateNoMoreData];

// 设置字体
footer.stateLabel.font = [UIFont systemFontOfSize:17];

// 设置颜色
footer.stateLabel.textColor = [UIColor blueColor];
```
![(上拉刷新05-自定义文字)](http://images0.cnblogs.com/blog2015/497279/201506/141205295511153.gif)

## <a id="上拉刷新06-加载后隐藏"></a>Footer Refresh 06 - Hide After Finish Refresh【上拉刷新06-加载后隐藏】
```objc
// 隐藏当前的上拉刷新控件
self.tableView.footer.hidden = YES;
```
![(上拉刷新06-加载后隐藏)](http://images0.cnblogs.com/blog2015/497279/201506/141205343481821.gif)

## <a id="上拉刷新07-自动回弹的上拉01"></a>Footer Refresh 07 - Bouncing Refresh01【上拉刷新07-自动回弹的上拉01】
```objc
self.tableView.footer = [MJRefreshBackNormalFooter footerWithRefreshingTarget:self refreshingAction:@selector(loadMoreData)];
```
![(上拉刷新07-自动回弹的上拉01)](http://images0.cnblogs.com/blog2015/497279/201506/141205392239231.gif)

## <a id="上拉刷新08-自动回弹的上拉02"></a>Footer Refresh 08 - Bouncing Refresh02【上拉刷新08-自动回弹的上拉02】
```objc
MJRefreshBackGifFooter *footer = [MJRefreshBackGifFooter footerWithRefreshingTarget:self refreshingAction:@selector(loadMoreData)];

// 设置普通状态的动画图片
[footer setImages:idleImages forState:MJRefreshStateIdle];
// 设置即将刷新状态的动画图片（一松开就会刷新的状态）
[footer setImages:pullingImages forState:MJRefreshStatePulling];
// 设置正在刷新状态的动画图片
[footer setImages:refreshingImages forState:MJRefreshStateRefreshing];

// 设置尾部
self.tableView.footer = footer;
```
![(上拉刷新07-自动回弹的上拉02)](http://images0.cnblogs.com/blog2015/497279/201506/141205441443628.gif)

## <a id="上拉刷新09-自定义刷新控件(自动刷新)"></a>Footer Refresh 09 - Customize Refreshing Footer(Release To Refresh)【上拉刷新09-自定义刷新控件(自动刷新)】
```objc
self.tableView.footer = [MJDIYAutoFooter footerWithRefreshingTarget:self refreshingAction:@selector(loadMoreData)];
// 具体实现参考MJDIYAutoFooter.h和MJDIYAutoFooter.m
```
![(上拉刷新09-自定义刷新控件(自动刷新))](http://images0.cnblogs.com/blog2015/497279/201506/141205500195866.gif)

## <a id="上拉刷新10-自定义刷新控件(自动回弹)"></a>Footer Refresh 10 - Customize Refreshing Footer(Bouncing Refresh)【上拉刷新10-自定义刷新控件(自动回弹)】
```objc
self.tableView.footer = [MJDIYBackFooter footerWithRefreshingTarget:self refreshingAction:@selector(loadMoreData)];
// 具体实现参考MJDIYBackFooter.h和MJDIYBackFooter.m
```
![(上拉刷新10-自定义刷新控件(自动回弹))](http://images0.cnblogs.com/blog2015/497279/201506/141205560666819.gif)

## <a id="UICollectionView01-上下拉刷新"></a>UICollectionView01-Refresh on Header and Footer【UICollectionView01-上下拉刷新】
```objc
// 下拉刷新
self.collectionView.header = [MJRefreshNormalHeader headerWithRefreshingBlock:^{
   // 进入刷新状态后会自动调用这个block
}];

// 上拉刷新
self.collectionView.footer = [MJRefreshAutoNormalFooter footerWithRefreshingBlock:^{
   // 进入刷新状态后会自动调用这个block
}];
```
![(UICollectionView01-上下拉刷新)](http://images0.cnblogs.com/blog2015/497279/201506/141206021603758.gif)

## <a id="UIWebView01-下拉刷新"></a>UIWebView01- Header Refresh【UIWebView01-下拉刷新】
```objc
// 添加下拉刷新控件
self.webView.scrollView.header = [MJRefreshNormalHeader headerWithRefreshingBlock:^{
   // 进入刷新状态后会自动调用这个block
}];
```
![(UICollectionView01-上下拉刷新)](http://images0.cnblogs.com/blog2015/497279/201506/141206080514524.gif)

## 提醒
* 本框架纯ARC，兼容的系统>=iOS6.0、iPhone\iPad横竖屏

## <a id="期待"></a>期待
* 如果在使用过程中遇到BUG，希望你能Issues我，谢谢（或者尝试下载最新的框架代码看看BUG修复没有）
* 如果在使用过程中发现功能不够用，希望你能Issues我，我非常想为这个框架增加更多好用的功能，谢谢
* 如果你想为MJRefresh输出代码，请拼命Pull Requests我
* 一起携手打造天朝乃至世界最好用的刷新框架，做天朝程序员的骄傲
* 如果你开发的应用中用到了MJRefresh，希望你能到[CocoaControls](https://www.cocoacontrols.com/controls/mjrefresh)添加你应用的iTunes路径，我将会安装使用你的应用，并且根据众多应用的使用情况，对MJRefresh进行一个更好的设计和完善，提供更多好用的功能，谢谢
   * 步骤01（微信是举个例子，百度“你的应用名称 itunes”）
![(step01)](http://ww4.sinaimg.cn/mw1024/800cdf9ctw1eq0viiv5rsj20sm0ea41t.jpg)
   * 步骤02
![(step02)](http://ww2.sinaimg.cn/mw1024/800cdf9ctw1eq0vilejxlj20tu0me7a0.jpg)
   * 步骤03
![(step03)](http://ww1.sinaimg.cn/mw1024/800cdf9ctw1eq0viocpo5j20wc0dc0un.jpg)
   * 步骤04
![(step04)](http://ww3.sinaimg.cn/mw1024/800cdf9ctw1eq0vir137xj20si0gewgu.jpg)
