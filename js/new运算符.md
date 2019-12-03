#### new 运算符创建一个用户定义的对象类型的实例或具有构造函数的内置对象的实例。

---
new进行了如下操作：
  - 创建一个新对象obj
  - 把obj的__proto__指向构造函数的prototype对象 实现继承
  - 将步骤1新创建的对象obj作为this的上下文 
  - 返回创建的对象obj（如果该函数没有返回对象，则返回this）
---

##### *自己实现一个new：*

```js
function _new(...args) {
  const [constructor, ...otherArgs] = args;
  
  if(typeof constructor !== 'function') {
      throw new TypeError('constructor is not a function');
  };

  // 1~2 步骤简单写法 const obj = Object.create(constructor.prototype);
  
  // 1.创建一个空的简单JavaScript对象（即{}）；
  const obj = {};   

  // 2.链接该对象（即设置该对象的构造函数）到另一个对象 ；
  Object.setPrototypeOf(obj, constructor.prototype)

  // 3.将步骤1新创建的对象作为this的上下文
  const result = constructor.apply(obj, otherArgs);

  // 4.如果该函数没有返回对象，则返回this。
  return isPrimitive(result) ? obj : result
}

function isPrimitive(value) {
  return value == null || ['string', 'number', 'boolean', 'symbol'].includes(typeof(value))
}

function Test(x, y) {
  this.x = x;
  this.y = y;
}

var testObj = _new(Test, 1, 2)
```
