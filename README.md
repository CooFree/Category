## Category

* 有两方面局限性：<br>
  * 无法向类中添加新的实例变量，类别没有位置容纳实例变量。<br>
  * 名称冲突，即当类别中的方法与原始类方法名称冲突时，类别具有更高的优先级。类别方法将完全取代初始方法从而无法再使用初始方法。
* 主要有3个作用：<br>
  * 可以将类的实现分散到多个不同文件或多个不同框架中，方便代码管理。也可以对框架提供类的扩展（没有源码，不能修改）。<br>
  * 创建对私有方法的前向引用：如果其他类中的方法未实现，在你访问其他类的私有方法时编译器报错这时使用类别，在类别中声明这些方法（不必提供方法实现），编译器就不会再产生警告<br>
  * 向对象添加非正式协议：创建一个NSObject的类别称为“创建一个非正式协议”，因为可以作为任何类的委托对象使用。

## Extension

* Extension常被称为是匿名的Category(比如：在字符串中类扩展extension,添加的属性str1和show方法都是私有的,只能在String类中可以访问得到
)
* 用于给类添加新方法，但只作用于原始类，不作用于subclass
* 只能对有implementation源代码的类写Extension，对于没有implementation源代码的类，比如framework class，是不可以的<br>
  Extension可以给原始类添加新方法，以及新属性

### 他们的主要区别是：
1.  形式上来看，extension是匿名的category。<br>
2.  extension里声明的方法需要在mainimplementation中实现，category不强制要求。<br>
3.  extension可以添加属性（变量），category不可以。

 
## <a name="index"/>目录

*  [CAAnimation](#CAAnimation)
*  [UIView](#UIView)
*  [UIScrollView](#UIScrollView)
*  [UIImage](#UIImage)
*  [UILabel](#UILabel)


## <a name = "CAAnimation">CAAnimation
 
|类名|功能|实现|
|:--:|:--:|--|
|CAAnimation+CooFree|动画|[self.iconImageV.layer addAnimation:[CAAnimation rotationAnim] forKey:@"rotationAnim"];//翻转<br>[self.layer addAnimation:[CAAnimation rotaAnim] forKey:@"rotaAnim"];//旋转<br>[self.iconImageV.layer addAnimation:[CAAnimation shakeAnim] forKey:@"shakeAnim"];//抖动|

## <a name = "UIView">UIView 

|类名|功能|实现|
|:--:|:--:|--|
|UIView+CFAnimation|动画效果|//淡入<br>- (void)fadeInWithTime:(NSTimeInterval)time;<br>//淡出<br>- (void)fadeOutWithTime:(NSTimeInterval)time;<br>//缩放<br>- (void)scalingWithTime:(NSTimeInterval)time andscal:(CGFloat)scal;<br>//旋转<br>- (void)RevolvingWithTime:(NSTimeInterval)time andDelta:(CGFloat)delta;|


## <a name = "UIScrollView">UIScrollView

|类名|功能|实现|
|:--:|:--:|--|
|UIScrollView+CFParallaxHeader|tableView头部放大|[self.tableView addParallaxHeadView:self.topView];|


## <a name = "UIImage">UIImage

|类名|功能|实现|
|:--:|:--:|--|
|UIImage+ImageEffects|模糊透明背景图|UIImage*blurSnapshotImage=[image applyBlurWithRadius:5.0f tintColor:[UIColor colorWithWhite:0.2f alpha:0.7f] saturationDeltaFactor:1.8f maskImage:nil];|



## <a name = "UILabel">UILabel

|类名|功能|实现|
|:--:|:--:|--|
|UILabel+Addition|一句代码创建|+ (instancetype)labelWithFont:(UIFont*)font               <br>textColor:(UIColor*)textColor           <br>textAlignment:(NSTextAlignment)textAlignment;|



