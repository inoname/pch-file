# pch-file
定义了常用功能的pch文件

```
//项目中用到的常量
#import "KLConst.h"


//快速设置view的x、y、width、height......
#import "UIView+Extension.h"


//颜色与随机颜色
#define KLRGBColor(r, g, b) [UIColor colorWithRed:(r)/255.0 green:(g)/255.0 blue:(b)/255.0 alpha:1.0]
#define KLARGBColor(r, g, b, a) [UIColor colorWithRed:(r)/255.0 green:(g)/255.0 blue:(b)/255.0 alpha:(a)]
#define KLRandomColor KLRGBColor(arc4random_uniform(255), arc4random_uniform(255), arc4random_uniform(255))


//设备是否为竖屏状态
#define KLScreenIsPortrait ([UIScreen mainScreen].bounds.size.height>[UIScreen mainScreen].bounds.size.width)


//通知中心
#define KLNoteCenter [NSNotificationCenter defaultCenter]


//自定义log
#ifdef DEBUG  // 调试阶段
#define KLLog(...) NSLog(__VA_ARGS__)
#else // 发布阶段
#define KLLog(...)
#endif
```
