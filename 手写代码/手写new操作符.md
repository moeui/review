[new操作符干了什么](../JS-ES6/15.new操作符干了什么.md)

```js
  function myNew(fn, ...args) {
    //  创建一个新对象
    const obj = {};
    // 新对象原型指向构造函数原型对象
    obj.__proto__ = fn.prototype;
    // 将构建函数的this指向新对象
    const result = fn.apply(obj, args)
    // 根据返回值判断返回哪个
    return result instanceof Object ? result : obj
  }
```