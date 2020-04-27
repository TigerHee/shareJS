## Observer API

> 友情提示：兼容性还不是很友好

### 1. ResizeObserver

ResizeObserver 接口可以监听到 Element 的内容区域或 SVGElement的边界框改变。内容区域则需要减去内边距padding。

- #### 构造器：

  - `ResizeObserver()`
  
    创建并返回一个ResizeObserver对象。

- #### 方法：

  - `ResizeObserver.observe()`

    开始观察指定的 Element或 SVGElement。

  - `ResizeObserver.disconnect()`

    取消和结束目标对象上所有对 Element或 SVGElement 观察。

  - `ResizeObserver.unobserve()`

    结束观察指定的Element或 SVGElement。

- #### 示例：

  监听body的size变化:

  ```js
  const resizeObserver = new ResizeObserver(entries => {
    for (let entry of entries) {
      console.log(entry)
    }
  });
  resizeObserver.observe(document.querySelector('body'));
  ```

### 2. IntersectionObserver

Intersection Observer API提供了一种异步观察目标元素与祖先元素或顶级文档viewport的交集中的变化的方法。

- 可能使用到的场景：
  - 当页面滚动时，懒加载图片或其他内容
  - 实现“可无限滚动”网站，也就是当用户滚动网页时直接加载更多内容，无需翻页
  - 根据用户是否已滚动到相应区域来灵活开始执行任务或动画

Intersection Observer API 允许你配置一个回调函数，每当目标(target)元素与设备视窗或者其他指定元素发生交集的时候执行。设备视窗或者其他元素我们称它为根元素或根(root)。通常，您需要关注文档最接近的可滚动祖先元素的交集更改，如果元素不是可滚动元素的后代，则默认为设备视窗。如果要观察相对于根(root)元素的交集，请指定根(root)元素为null。

目标(target)元素与根(root)元素之间的交叉度是交叉比(intersection ratio)。这是目标(target)元素相对于根(root)的交集百分比的表示，它的取值在0.0和1.0之间。

- #### 构造器：

  - `IntersectionObserver(callback, options)`

  ##### `callback`接收参数： 

  - IntersectionObserverEntry对象

  - 观察者的列表

  ##### `options`对象属性：

  - root：

    指定根(root)元素，用于检查目标的可见性。必须是目标元素的父级元素。如果未指定或者为null，则默认为浏览器视窗。

  - rootMargin：

    root元素的外边距。该属性值是用作root元素和target发生交集时候的计算交集的区域范围，使用该属性可以控制root元素每一边的收缩或者扩张。默认值为0。

  - threshold：

    可以是单一的number (eg: 0.5) 或是number数组 (eg: [0, 0.25, 0.5, 0.75, 1])，target元素和root元素相交程度达到该值的时候IntersectionObserver注册的回调函数将会被执行。

  ##### `IntersectionObserverEntry`对象属性：

    - time：

      可见性发生变化的时间，是一个高精度时间戳

    - target：

      被观察的目标元素，是一个 DOM 节点对象

    - rootBounds：

      根元素的矩形区域的信息，getBoundingClientRect()方法的返回值，如果没有根元素（即直接相对于视口滚动），则返回null

    - boundingClientRect：

      目标元素的矩形区域的信息

    - intersectionRect：

      目标元素与视口（或根元素）的交叉区域的信息

    - intersectionRatio：

      目标元素的可见比例，即intersectionRect占boundingClientRect的比例，完全可见时为1，完全不可见时小于等于0

- #### 示例：

  - 无限滚动：

    在无限滚动的底部放一个footer，监听footer的可见否来实现无限滚动

    ```js
    let Observer = new IntersectionObserver((entries) => {
      // 如果footer不可见，就返回
      if (entries[0].intersectionRatio <= 0) return;
      // 加载更多
      loadMore();
    });

    // 开始观察
    Observer.observe(
      document.querySelector('.scrollerFooter')
    );
    ```