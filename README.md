# Category
 使用分类为类添加方法
 
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



