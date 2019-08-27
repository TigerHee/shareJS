## call, apply 与 bind

#### 1.call() 与 apply()

call或apply会自动执行对应的函数

```
fun.call(thisNew[, arg1[, arg2[, ...]]])
```

```
fun.apply(thisNew[, argsArray])
```

thisNew： fun函数运行时指定的this值，可能的值为：

- 不传，或者传null，undefined， this指向window对象
- 传递另一个函数的函数名fun2，this指向函数fun2的引用
- 值为原始值(数字，字符串，布尔值),this会指向该原始值的自动包装对象，如 String、Number、Boolean
- 传递一个对象，函数中的this指向这个对象

用例：

call:

```
function fn1() {
  // 将arguments转成数组
  return Array.prototype.slice.call(arguments);  
}
fn1(1,2,3,4);  // [1, 2, 3, 4]
```

apply:

```
Math.max.apply(null, [2, 3, 1, 4])
```

#### 2.bind()

bind()方法会创建一个新函数，称为绑定函数。bind是ES5新增的一个方法，不会执行对应的函数，而是返回对绑定函数的引用。

```
fun.bind(thisNew[, arg1[, arg2[, ...]]]);
```

用例：

```
var $ = document.querySelectorAll.bind(document)
```

#### 三者异同

相同：

- 改变函数体内 this 的指向

不同：

- call、apply的区别：接受参数的方式不一样

- bind不立即执行。而apply、call 立即执行
