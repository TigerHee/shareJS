## call, apply 与 bind

#### 1.call() 与 apply()

call或apply会自动执行对应的函数

```js
fun.call(thisNew[, arg1[, arg2[, ...]]])
```

```js
fun.apply(thisNew[, argsArray])
```

thisNew： fun函数运行时指定的this值，可能的值为：

- 不传，或者传null，undefined， this指向window对象
- 传递另一个函数的函数名fun2，this指向函数fun2的引用
- 值为原始值(数字，字符串，布尔值),this会指向该原始值的自动包装对象，如 String、Number、Boolean
- 传递一个对象，函数中的this指向这个对象

用例：

call:

```js
window.name = 'windowName'
var obj = {
  name: 'objName'
}
function getName(p1, p2) {
  console.log('name === ', this.name)
  console.log('p1 === ', p1)
  console.log('p2 === ', p2)
}
getName('str1', 'str2')
getName.call(obj, 'str1', 'str2')
```

apply:

```js
Math.max.apply(null, [2, 3, 1, 4])
```

#### 2.bind()

bind()方法会创建一个新函数，称为绑定函数。bind是ES5新增的一个方法，不会执行对应的函数，而是返回对绑定函数的引用。

```js
fun.bind(thisNew[, arg1[, arg2[, ...]]]);
```

用例：

```js
var $ = document.querySelectorAll.bind(document)
```

#### 3.三者异同

相同：

- 改变函数体内 this 的指向

不同：

- call、apply的区别：接受参数的方式不一样

- bind不立即执行。而apply、call 立即执行

#### 4.模拟实现

call:

```js
Function.prototype.customCall = function () {
  if (typeof this !== 'function') {
    throw new TypeError('error!')
  }
  let context = arguments[0] || window
  context.fn = this
  let args = [...arguments].slice(1)
  let result = context.fn(...args)
  delete context.fn
  return result
}
```

apply:

```js
Function.prototype.customApply = function () {
  if (typeof this !== 'function') {
    throw new TypeError('error!')
  }
  let context = arguments[0] || window
  context.fn = this
  let result = !!arguments[1] ? context.fn(...arguments[1]) : context.fn()
  delete context.fn
  return result
}
```

bind:

```js
Function.prototype.customBind = function () {
  if (typeof this !== 'function') {
    throw new TypeError('error!')
  }
  const that = this
  let context = arguments[0] || window
  const args = [...arguments].slice(1)
  return function() {
    return that.apply(context, args.concat([...arguments]))
  }
}
```
