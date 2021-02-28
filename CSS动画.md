# CSS动画

https://developer.mozilla.org/zh-CN/docs/Web/CSS/transform





---

## 一、浏览器如何渲染网页

**概述：浏览器渲染一共有五步**

1. 处理 `HTML` 并构建 `DOM` 树。
2. 处理 `CSS`构建 `CSSOM` 树。
3. 将 `DOM` 与 `CSSOM` 合并成一个渲染树`render tree`。
4. 根据渲染树来布局，计算每个节点的位置。（文档流、盒模型、计算大小和位置）
5. 绘制，合成图层，显示在屏幕上（边框颜色、文字颜色、阴影等）
6. Compose 合成（根据层叠关系展示画面）

**参考文章**

[渲染树构建、布局及绘制](https://developers.google.com/web/fundamentals/performance/critical-rendering-path/render-tree-construction)

[渲染性能](https://developers.google.com/web/fundamentals/performance/rendering/)

https://csstriggers.com/

![image-20210301015819780](https://i.loli.net/2021/03/01/uJAOGa65scPxzTj.png)

![image-20210301015830792](https://i.loli.net/2021/03/01/C2U83mHcZIQLWBF.png)

## transform

四个常用功能

+ 位移translate
+ 缩放scale
+ 旋转rotate
+ 倾斜skew

inline元素不支持transform，需要变成block

####  translate

+ transform: translate(x方向, y方向);
+ transform: translateX() x方向移动
+ 同理transform: translateY()
+ 有Z方向但要在父元素上添加``perspective:  1000px``

1000px是元素距离视图的距离，以像素计。

perspective：800px  意思就是，我在离屏幕800px 的地方观看这个元素。(这个属性，要设置在父元素上面)

![img](https://i.loli.net/2021/03/01/QKPGpESt6haDJXz.png)



### scale缩放

+ 同样支持xy 写法有
  + transform: scale()
  + transform: scale(x, y)



### rotate旋转

transform: rotate( deg);

默认沿着Z轴，也可以沿着x或者y



### skew倾斜









# ransition 过渡

https://developer.mozilla.org/zh-CN/docs/Web/CSS/transition

![image-20210301003149355](https://i.loli.net/2021/03/01/t3Q6RgPkvSLIdGs.png)

``transition: width 1s;`` 属性名 时长



不是所有的属性都有过度

![image-20210301011732980](https://i.loli.net/2021/03/01/fyNrjKWgadGzlDV.png)











# animation

![image-20210301013612956](https://i.loli.net/2021/03/01/mY9OBRcWifHPUL6.png)

声明关键帧

@keyframes

增加动画

[JSbin实例](http://js.jirengu.com/peran/1/edit?html,css,output)

~~~~css
#demo.start{
  animation: xxx 1.5s;
} 

关键帧xxx
@keyframes xxx {
  0% {
    transform: none;
  }
  66.66%{
    transform: translateX(200px);
  }
  100%{
    transform: translateX(200px) translateY(100px);
  }
}
~~~~





**如何让动画停在最后一帧**

搜索css animation stop at end

网友给出的答案是加个 **forwards**

``#demo.start{
  animation: xxx 1.5s forwards;
} ``



@keyframes 完整语法

https://developer.mozilla.org/zh-CN/docs/Web/CSS/@keyframes

![image-20210301013407794](https://i.loli.net/2021/03/01/Wbawhr2XNpTMFZ8.png)