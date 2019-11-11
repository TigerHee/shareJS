- 小数取整：

```sh
  1.234 | 0
```

```sh
  ~~1.234
```

```sh
  1.234 >> 0
```

- 妙用隐式转换：

> 字符串转number:
```sh
  +'123'
```

> new Date转时间戳：
```sh
  +new Date()
```

> 数组/多维数组转为逗号分隔字符串(可用于多维数组转一维)：
```sh
  ""+[1, 2 , 3, 3, [2, 3, 4]]
```

- 解构：

> 交换a,b的值：
```sh
  var a=1;
  var b=2;
  [a, b] = [b, a];
  console.log(a, b);
```

- 扩展运算符：

> 取数组最大值/最小值：
```sh
  Math.max(...[1,2,3])
  Math.min(...[1,2,3])
```

> 生成时间：
```sh
  new Date(...[2018,6,4])
```

> 字符串转数组：
```sh
  method 1: 
  [...'string']
  
  method 2: 
  Array.from('string')
```

> 合并对象：
```sh
  let obj1 = {a:1, b:2};
  let obj2 = {b:3, c:4};

  {...obj1, ...obj2}
    等同于
  Object.assign(obj1, obj2)
```

- 常用方法：

> 数字前补0：
```sh
  function preFixNum(num, length) {
    return (Array(length).join('0') + num).slice(-length);
  }
```

> 数组元素为对象的去重：
```sh
  [...new Set(arr.map(v => JSON.stringify(v)))].map(v => JSON.parse(v))
```

> 数组求和：
```sh
  var arr = [1,2,3,4,5];
  
  method 1: 
  var sum = eval(arr.join('+'));
  
  method 2: 
  var sum = arr.reduce((prev,cur) => prev + cur);
```

> 金钱格式化(千分)：
```sh
  let money = 11111;
  
  method 1: 
  money.toLocaleString('en-US');
  
  method 2: 
  Intl.NumberFormat().format(money);
  
  method 3: 
  String(money).replace(/\B(?=(\d{3})+(?!\d))/g, ',');
```

> 短路逻辑代替if：
```sh
  isTrue && console.log(1);
```

> RGB to Hex：
```sh
  function RGBtoHEX(rgb){
    return ((1<<24) + (rgb.r<<16) + (rgb.g<<8) + rgb.b).toString(16).substr(1);
  }
```

> 延时函数:
```
const delay = ms => new Promise(resolve => setTimeout(resolve, ms))
```

> 生成指定长度数组：
```sh
  Array.from(new Array(10).keys());
```
- 正则进阶：

> 捕获括号：
```sh
  匹配 'tigerHee' 并且记住匹配项
  /(tigerHee)/
```

> 非捕获括号：
```sh
  匹配 'tigerHee' 但是不记住匹配项
  /(?:tigerHee)/
```

> 先行断言：
```sh
  匹配'tiger'仅仅当'tiger'后面跟着'Hee'
  /tiger(?=Hee)/
```

> 后行断言：
```sh
  匹配'Hee'仅仅当'Hee'前面是'tiger'
  /(?<=tiger)Hee/
```

> 正向否定查找：
```sh
  匹配'tiger'仅仅当'tiger'后面不跟着'java'
  /tiger(?!java)/
```



