## 强大的 Array.reduce

它可以返回任意值，它的功能就是将一个数组的内容聚合成单个值

#### 语法：

```js
arr.reduce(callback(accumulator, currentValue[, index[, array]])[, initialValue])
```

#### 参数说明：

- callback - 执行数组中每个值 (如果没有提供 initialValue 则第一个值除外)的函数
  - accumulator - 累计器累计回调的返回值; 它是上一次调用回调时返回的累积值，或 initialValue
  - currentValue - 数组中正在处理的元素
  - index - 数组中正在处理的当前元素的索引。 如果提供了 initialValue，则起始索引号为 0，否则从索引 1 起始
  - array - 调用 reduce()的数组
- initialValue - 作为第一次调用 callback 函数时的第一个参数的值。 如果没有提供初始值，则将使用数组中的第一个元素。 在没有初始值的空数组上调用 reduce 将报错

#### 注意：

如果数组为空且没有提供 initialValue，会抛出 TypeError 。如果数组仅有一个元素（无论位置如何）并且没有提供 initialValue， 或者有提供 initialValue 但是数组为空，那么此唯一值将被返回并且 callback 不会被执行。

#### 使用场景：

##### 数组求和

```js
[ 1, 2, 3 ].reduce(( acc, cur ) => acc + cur, 0)
```

##### 累加对象数组里的值

```js
[{x: 1}, {x:2}, {x:3}].reduce(function (acc, cur) {
    return acc + cur.x;
}, 0)
```

##### 按序执行 Promise

在不想用 async await 的时，同样可以处理 promise 回调链的问题

```js
function p1(a) {
  return new Promise((resolve, reject) => {
    resolve(a * 2);
  });
}
function p2(a) {
  return new Promise((resolve, reject) => {
    resolve(a * 3);
  });
}
function p3(a) {
  return new Promise((resolve, reject) => {
    resolve(a * 4);
  });
}
let initVal = 1;
[p1, p2, p3].reduce(
  (promiseChain, currentFunction) => promiseChain.then(currentFunction),
  Promise.resolve(initVal)
).then(res=>console.log(res))
```

##### 二维数组转一维数组

```js
[[0, 1], [2, 3], [4, 5]].reduce(( acc, cur ) => acc.concat(cur), [])
```

##### 统计数组中每个元素出现的次数

```js
['aa', 'bb', 'aa', 'cc', 'aa', 'bb'].reduce((allNames, name) => {
  if (name in allNames) {
    allNames[name]++;
  }
  else {
    allNames[name] = 1;
  }
  return allNames;
}, {})
```

##### 数组去重

```js
[1, 2, 3, 4, 4, 1].reduce((acc, cur) => {
  if (acc.includes(cur)) {
    return acc
  } else {
    return [...acc, cur]
  }
}, [])
```
