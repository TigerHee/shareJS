- 小数取整：

```js
  1.234 | 0
```

```js
  ~~1.234
```

```js
  1.234 >> 0
```

- 妙用隐式转换：

> 字符串转number:
```js
  +'123'
```

> new Date转时间戳：
```js
  +new Date()
```

> 数组/多维数组转为逗号分隔字符串(可用于多维数组转一维)：
```js
  ""+[1, 2 , 3, 3, [2, 3, 4]]
```

- 解构：

> 交换a,b的值：
```js
  var a=1;
  var b=2;
  [a, b] = [b, a];
  console.log(a, b);
```

- 扩展运算符：

> 取数组最大值/最小值：
```js
  Math.max(...[1,2,3])
  Math.min(...[1,2,3])
```

> 生成时间：
```js
  new Date(...[2018,6,4])
```

> 字符串转数组：
```js
  method 1: 
  [...'string']
  
  method 2: 
  Array.from('string')
```

> 合并对象：
```js
  let obj1 = {a:1, b:2};
  let obj2 = {b:3, c:4};

  {...obj1, ...obj2}
    等同于
  Object.assign(obj1, obj2)
```

- 常用方法：

> 数字前补0：
```js
  function preFixNum(num, length) {
    return (Array(length).join('0') + num).slice(-length);
  }
```

> 数组元素为对象的去重：
```js
  [...new Set(arr.map(v => JSON.stringify(v)))].map(v => JSON.parse(v))
```

> 数组求和：
```js
  var arr = [1,2,3,4,5];
  
  method 1: 
  var sum = eval(arr.join('+'));
  
  method 2: 
  var sum = arr.reduce((prev,cur) => prev + cur);
```

> 金钱格式化(千分)：
```js
  let money = 11111;
  
  method 1: 
  money.toLocaleString('en-US');
  
  method 2: 
  Intl.NumberFormat().format(money);
  
  method 3: 
  String(money).replace(/\B(?=(\d{3})+(?!\d))/g, ',');
```

> 短路逻辑代替if：
```js
  isTrue && console.log(1);
```

> RGB to Hex：
```js
  function RGBtoHEX(rgb){
    return ((1<<24) + (rgb.r<<16) + (rgb.g<<8) + rgb.b).toString(16).substr(1);
  }
```

> 延时函数:
```js
const delay = ms => new Promise(resolve => setTimeout(resolve, ms))
```

> 生成指定长度数组：
```js
  Array.from(new Array(10).keys());
```

> 快速创建a标签：
```js
  let a = '超链接'.link('https://github.com/TigerHee/shareJS');
  console.log('a === ', a)
```

- 正则进阶：

> 捕获括号：
```js
  匹配 'tigerHee' 并且记住匹配项
  /(tigerHee)/
```

> 非捕获括号：
```js
  匹配 'tigerHee' 但是不记住匹配项
  /(?:tigerHee)/
```

> 先行断言：
```js
  匹配'tiger'仅仅当'tiger'后面跟着'Hee'
  /tiger(?=Hee)/
```

> 后行断言：
```js
  匹配'Hee'仅仅当'Hee'前面是'tiger'
  /(?<=tiger)Hee/
```

> 正向否定查找：
```js
  匹配'tiger'仅仅当'tiger'后面不跟着'java'
  /tiger(?!java)/
```



