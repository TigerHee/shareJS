# js常用小技巧 - javascript(js) commonly used skill - 谢谢star

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

>数字字符串转number:
```sh
  +'123'
```

> new Date转时间戳：
```sh
  +new Date()
```

> 数组/多维数组转逗号分隔字符串：
```sh
  ""+[1, 2 , 3, 3, [2, 3, 4]]
```

- 解构：

> 交换a,b的值：
```sh
  var a=1;
  var b=2;
  [a, b] = [b, a];
  console.log('a ===', a);
  console.log('b ===', b);
```

- 扩展运算符：

> 取数组最大值：
```sh
  Math.max(...[1,2,3])
```

> 生成时间：
```sh
  new Date(...[2018,6,4])
```

> 字符串转数组：
```sh
  [...'string']
    另： Array.from('string')
```

- 常用方法：

> 数字前补0：
```sh
  preFixNum(num, length) {
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
  console.log(eval(arr.join('+')))
```

> 金钱格式化：
```sh
  let money = 11111;
  money .toLocaleString('en-US');
```

> 短路逻辑代替if：
```sh
  isTrue && console.log(1);
```

*********************************************
 一起学习前端共同进步！
`qq群：635833997`
*********************************************
![718](https://user-images.githubusercontent.com/15956567/42858386-e5e2fcc2-8a80-11e8-8a06-8807517d9854.png)

