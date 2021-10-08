## call、apply、bind

这里总结一下 call、apply、bind 的区别，call、apply 的第一个参数都是相同的，call从第二个参数开始就是函数的参数，apply第二个参数则是数组，bind的使用和call一样，区别是bind返回的的是一个函数，不会立即执行，需要调用才会执行。