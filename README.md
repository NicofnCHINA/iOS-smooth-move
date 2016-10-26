# iOS_smooth_move
annotation移动及转向动画
-请先执行pod install --repo-update 安装依赖库
-查看Demo请打开.xcworkspace文件

### 使用教程

- 使用方法
```
/*!
 @brief 添加动画
 @param points 轨迹点串，每个轨迹点为TracingPoint类型
 @param duration 动画时长，包括从上一个动画的终止点过渡到新增动画起始点的时间
 */
- (void)addTrackingAnimationForPoints:(NSArray *)points duration:(CFTimeInterval)duration;
 ```
其中，轨迹点类型为：
 ```
@interface TracingPoint : NSObject
/*!
 @brief 轨迹经纬度
 */
@property (nonatomic) CLLocationCoordinate2D coordinate;
/*!
 @brief 方向，有效范围0~359.9度
 */
@property (nonatomic) CLLocationDirection course;
@end
```

注：多次调用添加动画接口，会按调用顺序依次执行添加的动画。


### 截图效果

![result](https://raw.githubusercontent.com/amap-demo/iOS-smooth-move/master/ios_movingAnnotation_demo_gif.gif)
