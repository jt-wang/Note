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
- 对扩展开放，对修改关闭
- 依赖倒置原则（Dependency Inversion Principle）：要依赖抽象，不要依赖具体类

## OO 模式
### 策略模式（Strategy Pattern）
定义算法族，分别封装起来，让它们之间可以相互替换，此模式让算法的变化独立于使用算法的客户。

### 观察者模式（Observer Pattern）
定义了对象之间的一对多依赖，这样一来，当一个对象改变状态时，它的所有依赖者都会收到通知并自动更新。<br>
![Observer Pattern](/Design Pattern/Observer Pattern.png)
#### Java 中的观察者模式
- java.util package 中包含 Observer 接口和 Observable 类
- `notifyObservers(Object arg)` 可以设置使用 push 或 pull（无参数）的方式传送数据
- 在调用`notifyObservers()`之前，要先调用`setChanged()`来指示状态已经改变
- Swing 大量使用观察者模式

### 装饰者模式（Decorator Pattern）
动态地将责任附加到对象上。若要扩展功能，装饰者提供了比继承更有弹性的替代方案。<br>
利用装饰者模式，常常造成设计中有大量的小类。<br>
![Decorator Pattern](/Design Pattern/Decorator Pattern.png)
#### Java I/O
![Java I/O](/Design Pattern/Java I_O.png)

### 工厂模式（Factory Pattern）
所有的工厂都是用来封装对象的创建
#### 简单工厂（Simple Factory）
![Simple Factory](/Design Pattern/Simple Factory.png)
#### 工厂方法模式（Factory Method Pattern）
定义了一个创建对象的接口，但由子类决定要实例化的类是哪一个。工厂方法让类把实例化推迟到子类。<br>
![Factory Method Pattern](/Design Pattern/Factory Method Pattern.png)
#### 抽象工厂模式（Abstract Factory Pattern）
提供一个接口，用于创建相关或依赖对象的家族，而不需要明确指定具体类。<br>
![Abstract Factory Pattern](/Design Pattern/Abstract Factory Pattern.png)
