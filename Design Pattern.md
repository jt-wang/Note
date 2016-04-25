# Design Pattern

笔记基于 [Head First Design Patterns](http://www.headfirstlabs.com/books/hfdp/)

## OO 基础
- 抽象
- 封装
- 多态
- 继承

## OO 原则
- 封装变化
- 多用组合，少用继承
- 针对接口编程，不针对实现编程

## OO 模式
### 策略模式
定义算法族，分别封装起来，让它们之间可以相互替换，此模式让算法的变化独立于使用算法的客户。

### 观察者模式
![Observer Pattern](/Design Pattern/Observer Pattern.png)
定义了对象之间的一对多依赖，这样一来，当一个对象改变状态时，它的所有依赖者都会收到通知并自动更新。</br>
