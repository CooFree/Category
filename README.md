# Category
 使用分类为类添加方法

* UIScrollView

|类名|功能|实现|
|:--:|:--:|:--|
|UIScrollView+CFParallaxHeader|tableView头部放大|[self.tableView addParallaxHeadView:self.topView];|



* UIImage

|类名|功能|实现|
|:--:|:--:|:--|
|UIImage+CFImage|模糊透明背景图|(UIImage*)imageWithView(UIView*)view{<br>UIGraphicsBeginImageContextWithOptions(CGSizeMake(view.frame.size.width, view.frame.size.height), NO, [[UIScreen mainScreen] scale]);<br>[view.layer renderInContext:UIGraphicsGetCurrentContext()];<br>UIImage*image=UIGraphicsGetImageFromCurrentImageContext();<br>UIColor*tintColor=[UIColor colorWithWhite:0.95 alpha:0.78];<br>image = [image applyBlurWithRadius:15 tintColor:tintColor saturationDeltaFactor:1 maskImage:nil];<br>UIGraphicsEndImageContext();<br>return image;}<br>|



* UIView 

|类名|功能|实现|
|:--:|:--:|:--|
|UIView+CFAnimation|动画效果|//淡入<br>- (void)fadeInWithTime:(NSTimeInterval)time;<br>//淡出<br>- (void)fadeOutWithTime:(NSTimeInterval)time;<br>//缩放<br>- (void)scalingWithTime:(NSTimeInterval)time andscal:(CGFloat)scal;<br>//旋转<br>- (void)RevolvingWithTime:(NSTimeInterval)time andDelta:(CGFloat)delta;|




