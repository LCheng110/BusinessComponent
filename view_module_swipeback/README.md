# view_module_swipeback

### 介绍
无需继承和实现，侧滑只需一步，0接入成本，已适配Android 9P ，透明主题。

#### 特性
- 自动检索是否第一个Activity
- 两种方式配置不需要侧滑Activity，使用 SwipeOptions 集中配置，或 Activity 实现接口 ISwipeBack 接口
- 已适配 9P 和 windowIsTranslucent 透明主题

#### 预览
<div width="100%" align="center"><img src="ezgif.com-video-to-gif.gif"  width="280px"/></div>

#### 使用
1.引入 Module 或 gradle
```
  implementation 'com.from.view.swipeback:view_module_swipeback:1.0.2'
```

2.在 Application 初始化
```
  SwipeBackHelper.init(this);
```
3.配置项目
```
     SwipeOptions options = SwipeOptions.builder()
            .exclude(exclude) // 排除不需要侧滑的类
//             以下默认值
//            .isWeChatStyle(true)  //  是否是微信滑动返回样式
//            .isTrackingLeftEdge(true)     // 是否仅仅跟踪左侧边缘的滑动返回
//            .isShadowAlphaGradient(true)     // 阴影区域的透明度是否根据滑动的距离渐变
//            .isNavigationBarOverlap(false)     // 底部导航条是否悬浮在内容上
//            .isNeedShowShadow(true) // 否显示滑动返回的阴影效果
//            .shadowResId() // 阴影资源 id
            .build();
```

值得注意的是，初始化之后你所使用的依赖库中的 Activity 也会拥有侧滑的能力.
不过你可使用 option 剔除，如你正好需要也可以保留








