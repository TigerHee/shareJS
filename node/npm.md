## 常用 npm 包

- ### `decimal.js`

> 高精度计算库

- ### `WOW.js`

> 页面滚动时元素出现的动画库

[demo](https://www.delac.io/wow/)

- ### `object-path`

> js 可选链式调用之前的替代品，解决 `TypeError: Cannot read property ‘x’ of undefined`的问题

##### 用例：

```js
import objectPath from "object-path";

objectPath.get(obj, ["a.c.b"], "DEFAULT");
```

- ### `water-wave`

> 一个创建点击后产生水波纹效果的 React 组件

- ### `clsx`

> clsx 是一个小型工具集，用于有条件地从一个对象中构造 className 字符串，此对象的键是类字符串（class strings），而值是布尔值（booleans）

##### 用例：

```js
// 使用前：
<div className={`root ${disabled ? "disabled" : ""} ${selected ? "selected" : ""}`} />;

// 使用后
<div
  className={clsx("root", {
    disabled: disabled,
    selected: selected,
  })}
/>;
```

## package.json

- ### 锁死依赖包的依赖：

```js
{
  "dependencies": {},
  "resolutions": {
    "包名": "版本号"
  }
}
```
