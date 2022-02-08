# KJLoadingDemo

基于CALayer封装加载等待动画  
陆陆续续后续还会添加更多数据源，部分数据来源于网络    

----------------------------------------

### Cocoapods Install
```
pod 'KJLoading'
pod 'KJLoading/KJProgressHUD'
```

### 自定义动画
- 重载方法
```ruby
- (void)kj_setAnimationFromLayer:(CALayer *)layer Size:(CGSize)size Color:(UIColor *)tintColor
```

### 自定义素材使用方法
```ruby
KJLoadingDeploy *loadingConfig = [KJLoadingDeploy kj_defaultLoadingDeploy];
loadingConfig.class_name = @"KJCustom";  /// 继承的动画素材类名
loadingConfig.kType = KJLoadingAnimationTypeCustom;
[KJLoading kLoadingAnimationStartAnimatingWithView:self.view Configuration:loadingConfig];
```
---
### 问题总结
##### 1、xib布局，如果遇见视图显示错位，并不在父视图中心位置。
###### 解决方案：重置父视图frame

---

#### <a id="更新日志"></a>更新日志
```
- 版本更新日志：
Add 1.2.5
1.UIView+KJLoading 封装

Add 1.2.4
1.重新整理，规范方法名

Add 1.2.0
1.新增属性 kDismiss 和 kDismissTime 是否开启消失动画和消失时间

Add 1.1.1
1.新增时间沙漏加载动画、错位旋转、渐变蛇 三种素材

Add 1.1.0
1.优化调整，去除不必要的代码工作

Add 1.0.2
1.新增三种加载动画(写文字/画爱心/心电图)    
2.播放指定图片    

Add 1.0.0
KJLoading 内含 7 种加载动画，多种属性自定义调整    
同样可以自定义，自定义动画素材需要继承自 KJLoadingDeploy   
```
