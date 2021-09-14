## 设计模式

- [观察者模式和发布订阅者模式](./设计模式/观察者模式和发布订阅者模式.md)
- [工厂模式和策略模式](./设计模式/工厂模式和策略模式.md)
- [单例模式](./设计模式/单例模式.md)
- [代理模式](./设计模式/代理模式.md)
- [迭代器模式](./设计模式/迭代器模式.md)
- [建造者模式](./设计模式/建造者模式.md)
- [命令模式](./设计模式/命令模式.md)
- [外观模式](./设计模式/外观模式.md)
- [享元模式](./设计模式/享元模式.md)
- [职责链模式](./设计模式/职责链模式.md)
- [中介者模式](./设计模式/中介者模式.md)
- [装饰者模式](./设计模式/装饰者模式.md)
- [组合模式](./设计模式/组合模式.md)

## 手写代码
- [EventBus](./手写代码/实现EventBus.md)

### 其他

简述中介者模式，代理模式，外观模式区别与联系

三者的区别与联系：
- 1，中介者模式：A，B之间的对话通过C来传达。A,B可以互相不认识（减少了A和B对象间的耦合）
- 2，代理模式：A要送B礼物，A,B互相不认识，那么A可以找C来帮它实现送礼物的愿望（封装了A对象）
- 3，外观模式：A和B都要实现送花，送巧克力的方法，那么我可以通过一个抽象类C实现送花送巧克力的方法（A和B都继承C）。（封装了A，B子类）
代理模式和外观者模式这两种模式主要不同就是代理模式针对的是单个对象，而外观模式针对的是所有子类。

### 参考

- [JavaScript中常见的十五种设计模式](https://www.cnblogs.com/imwtr/p/9451129.html#o13)
- [设计模式这样学也太简单了吧！](https://juejin.cn/post/6953423646664687652#heading-47)



