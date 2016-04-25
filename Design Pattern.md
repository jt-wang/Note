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
- 尽量在交互对象之间使用松耦合设计

## OO 模式
### 策略模式（Strategy Pattern）
定义算法族，分别封装起来，让它们之间可以相互替换，此模式让算法的变化独立于使用算法的客户。

### 观察者模式（Observer Pattern）
![Observer Pattern](/Design Pattern/Observer Pattern.png)

定义了对象之间的一对多依赖，这样一来，当一个对象改变状态时，它的所有依赖者都会收到通知并自动更新。</br>
#### Java 中的观察者模式
- java.util package 中包含 Observer 接口和 Observable 类
- `notifyObservers(Object arg)` 可以设置使用 push 或 pull（无参数）的方式传送数据
- 在调用`notifyObservers()`之前，要先调用`setChanged()`来指示状态已经改变
- Swing 大量使用观察者模式
